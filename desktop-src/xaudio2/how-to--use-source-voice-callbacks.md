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
# <a name="how-to-use-source-voice-callbacks"></a>So wird's gemacht: Verwenden der Rückrufe für Quellstimmen

Wenn Sie eine Quellsprache erstellen, können Sie eine Struktur an diese übergeben, die Rückrufe für bestimmte Audioereignisse definiert. Sie können diese Rückrufe zum Ausführen von Aktionen oder zum signalisieren anderer Codes verwenden.

1.  Erstellen Sie eine Klasse, die von der [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) -Schnittstelle erbt. Alle Member-Funktionen von **IXAudio2VoiceCallback** sind rein virtuell und müssen definiert werden. Die einzige Funktion, die in diesem Beispiel von Interesse ist, ist [**onstreamend**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend). Daher sind die restlichen Funktionen Stub. Die **onstreamend** -Funktion löst ein Ereignis aus, das angibt, dass der Sound wiedergegeben wird.

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

    

2.  Erstellen Sie eine [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) mit [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) , indem Sie eine Instanz der Rückruf Klasse verwenden, die zuvor als pCallback-Parameter erstellt wurde.

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  Verwenden Sie nach dem Starten der Stimme die [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) -Methode, um zu warten, bis das Ereignis ausgelöst wird.

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückrufe](callbacks.md)
</dt> <dt>

[XAudio2-Rückrufe](xaudio2-callbacks.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[So wird's gemacht: Streamen von Sound von einem Datenträger](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
