# Gemini Model and Voice Update Findings

This document summarizes the research findings for updating the text-to-speech model and voices in the application.

## 1. Current Model and Voices

-   **Current Model:** `gemini-2.0-flash-exp`
-   **Current Voices:** A limited list of older voices (Puck, Charon, Kore, Fenrir, Aoede).

## 2. Latest Available Models

Based on the official Google documentation, the latest relevant models are:

-   **For REST API (Text-to-Speech focused):**
    -   `gemini-2.5-flash-preview-tts`
    -   `gemini-2.5-pro-preview-tts`
-   **For Live API (WebSocket Streaming - as used in this app):**
    -   The most recent model that supports the Live API is **`gemini-2.5-flash-native-audio-preview-09-2025`**.

## 3. Latest Available Voices

A new, extensive list of voices is available for the `Gemini-TTS` models (which use the REST API). The documentation does not explicitly confirm if these voices are compatible with the Live API model.

**New Voice List:**

*   Achernar (Female)
*   Achird (Male)
*   Algenib (Male)
*   Algieba (Male)
*   Alnilam (Male)
*   Aoede (Female)
*   Autonoe (Female)
*   Callirrhoe (Female)
*   Charon (Male)
*   Despina (Female)
*   Enceladus (Male)
*   Erinome (Female)
*   Fenrir (Male)
*   Gacrux (Female)
*   Iapetus (Male)
*   Kore (Female)
*   Laomedeia (Female)
*   Leda (Female)
*   Orus (Male)
*   Pulcherrima (Female)
*   Puck (Male)
*   Rasalgethi (Male)
*   Sadachbia (Male)
*   Sadaltager (Male)
*   Schedar (Male)
*   Sulafat (Female)
*   Umbriel (Male)
*   Vindemiatrix (Female)
*   Zephyr (Female)
*   Zubenelgenubi (Male)

## 4. Implementation Plan

1.  **Update Model:** Change the model name in the code from `gemini-2.0-flash-exp` to `gemini-2.5-flash-native-audio-preview-09-2025`.
2.  **Update Voices:** Replace the old voice list in the settings UI with the new, expanded list.
3.  **Test Compatibility:** Verify if the new voices work with the updated Live API model. If they do not, the application will likely default to a standard voice for that model, but the primary goal of updating the model itself will still be achieved.