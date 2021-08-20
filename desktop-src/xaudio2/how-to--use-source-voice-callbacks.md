---
description: Wenn Sie eine Quellstimme erstellen, können Sie eine Struktur an sie übergeben, die Rückrufe für bestimmte Audioereignisse definiert. Sie können diese Rückrufe verwenden, um Aktionen auszuführen oder anderen Code zu signalisieren.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: "So wird's gemacht: Verwenden der Rückrufe für Quellstimmen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa19de67c8e02bfa4c283fac8677a7eae2325b074eef5d5f5c7db644b3f113a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583770"
---
# <a name="how-to-use-source-voice-callbacks"></a>So wird's gemacht: Verwenden der Rückrufe für Quellstimmen

Wenn Sie eine Quellstimme erstellen, können Sie eine Struktur an sie übergeben, die Rückrufe für bestimmte Audioereignisse definiert. Sie können diese Rückrufe verwenden, um Aktionen auszuführen oder anderen Code zu signalisieren.

1.  Erstellen Sie eine Klasse, die von der [**IXAudio2VoiceCallback-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) erbt. Alle Memberfunktionen von **IXAudio2VoiceCallback** sind rein virtuell und müssen definiert werden. Die einzige für dieses Beispiel interessante Funktion ist [**OnStreamEnd.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend) Daher sind die restlichen Funktionen Stubs. Die **OnStreamEnd-Funktion** löst ein Ereignis aus, das angibt, dass der Sound wiedergegeben wird.

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

    

2.  Erstellen Sie eine [**Quellstimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) mit [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) mithilfe einer Instanz der Rückrufklasse, die zuvor als pCallback-Parameter erstellt wurde.

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  Verwenden Sie nach dem Starten der Stimme die [**WaitForSingleObjectEx-Methode,**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) um auf das Auslösen des Ereignisses zu warten.

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

 

 
