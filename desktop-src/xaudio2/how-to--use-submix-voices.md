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
# <a name="how-to-use-submix-voices"></a><span data-ttu-id="43250-104">So wird's gemacht: Verwenden von Submixstimmen</span><span class="sxs-lookup"><span data-stu-id="43250-104">How to: Use Submix Voices</span></span>

<span data-ttu-id="43250-105">In diesem Thema wird gezeigt, wie Sie Gruppen von Stimmen festlegen können, um Ihre Ausgabe an dieselbe teilmix-Stimme zu senden.</span><span class="sxs-lookup"><span data-stu-id="43250-105">This topic shows you how you can set groups of voices to send their output to the same submix voice.</span></span> <span data-ttu-id="43250-106">Dies ermöglicht eine einzelne Änderung an einer teilmix-Stimme, um eine ganze Gruppe von Stimmen zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="43250-106">This enables a single change to a submix voice to affect a whole group of voices.</span></span>

1.  <span data-ttu-id="43250-107">Erstellen Sie eine [**teilmix-Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) , an die alle Stimmen des Sound Effekts des Spiels gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="43250-107">Create a [**submix voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) to which all of the game's sound effect voices will send.</span></span>
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  <span data-ttu-id="43250-108">Erstellen Sie eine [**XAUDIO2 \_ Voice \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) Send-Struktur, die einen Verweis auf die Teil Mischungs Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="43250-108">Create an [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure that contains a reference to the submix voice.</span></span>
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  <span data-ttu-id="43250-109">Übergeben Sie die [**XAUDIO2 Voice-Nachricht \_ \_ sendet**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) die Struktur an neue Quell Stimmen, wenn Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="43250-109">Pass the [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure to new source voices as they are created.</span></span>
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  <span data-ttu-id="43250-110">Übernehmen Sie Änderungen an allen Soundeffekt Stimmen, indem Sie die Teil Mischungs Sprache anpassen.</span><span class="sxs-lookup"><span data-stu-id="43250-110">Apply changes to all sound effect voices by adjusting the submix voice.</span></span>

    <span data-ttu-id="43250-111">In diesem Beispiel ändert das Ändern des Volumes der unter Mischungs Sprache mit der [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) -Funktion die Menge aller in ihr ausgegebenen Stimmen.</span><span class="sxs-lookup"><span data-stu-id="43250-111">In this example, changing the volume of the submix voice with the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function effectively changes the volume of all voices that output to it.</span></span>

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="43250-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43250-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43250-113">Stimmen</span><span class="sxs-lookup"><span data-stu-id="43250-113">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="43250-114">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="43250-114">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="43250-115">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="43250-115">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
