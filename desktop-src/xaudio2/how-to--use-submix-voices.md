---
description: In diesem Thema wird gezeigt, wie Sie Gruppen von Stimmen festlegen können, um Ihre Ausgabe an dieselbe teilmix-Stimme zu senden. Dies ermöglicht eine einzelne Änderung an einer teilmix-Stimme, um eine ganze Gruppe von Stimmen zu beeinflussen.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: "So wird's gemacht: Verwenden von Submixstimmen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216790"
---
# <a name="how-to-use-submix-voices"></a>So wird's gemacht: Verwenden von Submixstimmen

In diesem Thema wird gezeigt, wie Sie Gruppen von Stimmen festlegen können, um Ihre Ausgabe an dieselbe teilmix-Stimme zu senden. Dies ermöglicht eine einzelne Änderung an einer teilmix-Stimme, um eine ganze Gruppe von Stimmen zu beeinflussen.

1.  Erstellen Sie eine [**teilmix-Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) , an die alle Stimmen des Sound Effekts des Spiels gesendet werden.
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  Erstellen Sie eine [**XAUDIO2 \_ Voice \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) Send-Struktur, die einen Verweis auf die Teil Mischungs Sprache enthält.
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  Übergeben Sie die [**XAUDIO2 Voice-Nachricht \_ \_ sendet**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) die Struktur an neue Quell Stimmen, wenn Sie erstellt werden.
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  Übernehmen Sie Änderungen an allen Soundeffekt Stimmen, indem Sie die Teil Mischungs Sprache anpassen.

    In diesem Beispiel ändert das Ändern des Volumes der unter Mischungs Sprache mit der [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) -Funktion die Menge aller in ihr ausgegebenen Stimmen.

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stimmen](voices.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
