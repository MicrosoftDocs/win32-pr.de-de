---
description: Wenn Sie eine Quellsprache erstellen, können Sie eine Struktur an diese übergeben, die Rückrufe für bestimmte Audioereignisse definiert. Sie können diese Rückrufe zum Ausführen von Aktionen oder zum signalisieren anderer Codes verwenden.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: "So wird's gemacht: Verwenden der Rückrufe für Quellstimmen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c10005ed838a22ea0dfce59312d6f293c213c39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752424"
---
# <a name="how-to-use-source-voice-callbacks"></a><span data-ttu-id="0b458-104">So wird's gemacht: Verwenden der Rückrufe für Quellstimmen</span><span class="sxs-lookup"><span data-stu-id="0b458-104">How to: Use Source Voice Callbacks</span></span>

<span data-ttu-id="0b458-105">Wenn Sie eine Quellsprache erstellen, können Sie eine Struktur an diese übergeben, die Rückrufe für bestimmte Audioereignisse definiert.</span><span class="sxs-lookup"><span data-stu-id="0b458-105">When you create a source voice, you can pass a structure to it that defines callbacks for certain audio events.</span></span> <span data-ttu-id="0b458-106">Sie können diese Rückrufe zum Ausführen von Aktionen oder zum signalisieren anderer Codes verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b458-106">You can use these callbacks to perform actions or to signal other code.</span></span>

1.  <span data-ttu-id="0b458-107">Erstellen Sie eine Klasse, die von der [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="0b458-107">Create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span> <span data-ttu-id="0b458-108">Alle Member-Funktionen von **IXAudio2VoiceCallback** sind rein virtuell und müssen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0b458-108">All member functions of **IXAudio2VoiceCallback** are purely virtual, and must be defined.</span></span> <span data-ttu-id="0b458-109">Die einzige Funktion, die in diesem Beispiel von Interesse ist, ist [**onstreamend**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span><span class="sxs-lookup"><span data-stu-id="0b458-109">The only function of interest in this example is [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span></span> <span data-ttu-id="0b458-110">Daher sind die restlichen Funktionen Stub.</span><span class="sxs-lookup"><span data-stu-id="0b458-110">Therefore, the rest of the functions are stubs.</span></span> <span data-ttu-id="0b458-111">Die **onstreamend** -Funktion löst ein Ereignis aus, das angibt, dass der Sound wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0b458-111">The **OnStreamEnd** function triggers an event that indicates the sound is done playing.</span></span>

    ```
    class VoiceCallback : public IXAudio2VoiceCallback
    {
    public:
        HANDLE hBufferEndEvent;
        VoiceCallback(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
        ~VoiceCallback(){ CloseHandle( hBufferEndEvent ); }

        //Called when the voice has just finished playing a contiguous audio stream.
        void OnStreamEnd() { SetEvent( hBufferEndEvent ); }

        //Unused methods are stubs
        void OnVoiceProcessingPassEnd() { }
        void OnVoiceProcessingPassStart(UINT32 SamplesRequired) {    }
        void OnBufferEnd(void * pBufferContext)    { }
        void OnBufferStart(void * pBufferContext) {    }
        void OnLoopEnd(void * pBufferContext) {    }
        void OnVoiceError(void * pBufferContext, HRESULT Error) { }
    };
    ```

    

2.  <span data-ttu-id="0b458-112">Erstellen Sie eine [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) mit [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) , indem Sie eine Instanz der Rückruf Klasse verwenden, die zuvor als pCallback-Parameter erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0b458-112">Create a [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) with [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) using an instance of the callback class created previously as the pCallback parameter.</span></span>

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  <span data-ttu-id="0b458-113">Verwenden Sie nach dem Starten der Stimme die [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) -Methode, um zu warten, bis das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0b458-113">After starting the voice, use the [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) method to wait for the event to be triggered.</span></span>

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="0b458-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b458-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b458-115">Rückrufe</span><span class="sxs-lookup"><span data-stu-id="0b458-115">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="0b458-116">XAudio2-Rückrufe</span><span class="sxs-lookup"><span data-stu-id="0b458-116">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="0b458-117">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="0b458-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="0b458-118">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="0b458-118">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="0b458-119">So wird's gemacht: Streamen von Sound von einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="0b458-119">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
