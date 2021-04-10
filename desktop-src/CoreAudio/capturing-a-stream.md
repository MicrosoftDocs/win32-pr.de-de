---
description: Erfassen eines Streams
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Erfassen eines Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861212"
---
# <a name="capturing-a-stream"></a>Erfassen eines Streams

Der Client ruft die Methoden in der [**iaudiocaptureclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) -Schnittstelle auf, um erfasste Daten aus einem Endpunkt Puffer zu lesen. Der Client verwendet den Endpunkt Puffer mit dem Audiomodul im freigegebenen Modus und mit dem Audiogerät im exklusiven Modus. Um einen Endpunkt Puffer einer bestimmten Größe anzufordern, ruft der Client die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf. Um die Größe des zugeordneten Puffers zu erhalten, der sich von der angeforderten Größe unterscheiden kann, ruft der Client die [**iaudioclient:: getBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) -Methode auf.

Um einen Stream erfasster Daten über den Endpunkt Puffer zu verschieben, ruft der Client alternativ die [**iaudiocaptureclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) -Methode und die [**iaudiocaptureclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) -Methode auf. Der Client greift als eine Reihe von Datenpaketen auf die Daten im Endpunkt Puffer zu. Der **GetBuffer** -Befehl ruft das nächste Paket der aufgezeichneten Daten aus dem Puffer ab. Nachdem die Daten aus dem Paket gelesen wurden, ruft der Client **ReleaseBuffer** auf, um das Paket freizugeben und für mehr erfasste Daten verfügbar zu machen.

Die Paketgröße kann von einem [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) -aufrufen zum nächsten abweichen. Vor dem Aufrufen von **GetBuffer** hat der Client die Möglichkeit, die [**iaudiocaptureclient:: getnextpacketsize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) -Methode aufrufen, um die Größe des nächsten Pakets im Voraus zu erhalten. Außerdem kann der Client die [**iaudioclient:: getcurrentpadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) -Methode aufrufen, um die Gesamtmenge der aufgezeichneten Daten zu erhalten, die im Puffer verfügbar ist. Die Paketgröße ist immer kleiner oder gleich der Gesamtmenge der aufgezeichneten Daten im Puffer.

Bei jedem Verarbeitungs Durchlauf hat der Client die Möglichkeit, die erfassten Daten auf eine der folgenden Arten zu verarbeiten:

-   Der Client ruft alternativ [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) und [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)auf, wobei ein Paket mit jedem Paar von Aufrufen gelesen wird, bis **GetBuffer** den Wert von audcnt \_ S \_ bufferempty zurückgibt, wodurch angegeben wird, dass der Puffer leer ist.
-   Der Client ruft [**getnextpacketsize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) vor jedem Paar von Aufrufen von [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) und [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) auf, bis **getnextpacketsize** eine Paketgröße von 0 meldet, was angibt, dass der Puffer leer ist.

Die beiden Techniken liefern gleichwertige Ergebnisse.

Das folgende Codebeispiel zeigt, wie Sie einen Audiostream vom Standard Erfassungsgerät aufzeichnen:


```C++
//-----------------------------------------------------------
// Record an audio stream from the default audio capture
// device. The RecordAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data from the
// capture device. The main loop runs every 1/2 second.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioCaptureClient = __uuidof(IAudioCaptureClient);

HRESULT RecordAudioStream(MyAudioSink *pMySink)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioCaptureClient *pCaptureClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 packetLength = 0;
    BOOL bDone = FALSE;
    BYTE *pData;
    DWORD flags;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eCapture, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetMixFormat(&pwfx);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_SHARED,
                         0,
                         hnsRequestedDuration,
                         0,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Get the size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioCaptureClient,
                         (void**)&pCaptureClient);
    EXIT_ON_ERROR(hr)

    // Notify the audio sink which format to use.
    hr = pMySink->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                     bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start recording.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (bDone == FALSE)
    {
        // Sleep for half the buffer duration.
        Sleep(hnsActualDuration/REFTIMES_PER_MILLISEC/2);

        hr = pCaptureClient->GetNextPacketSize(&packetLength);
        EXIT_ON_ERROR(hr)

        while (packetLength != 0)
        {
            // Get the available data in the shared buffer.
            hr = pCaptureClient->GetBuffer(
                                   &pData,
                                   &numFramesAvailable,
                                   &flags, NULL, NULL);
            EXIT_ON_ERROR(hr)

            if (flags & AUDCLNT_BUFFERFLAGS_SILENT)
            {
                pData = NULL;  // Tell CopyData to write silence.
            }

            // Copy the available capture data to the audio sink.
            hr = pMySink->CopyData(
                              pData, numFramesAvailable, &bDone);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->ReleaseBuffer(numFramesAvailable);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->GetNextPacketSize(&packetLength);
            EXIT_ON_ERROR(hr)
        }
    }

    hr = pAudioClient->Stop();  // Stop recording.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pCaptureClient)

    return hr;
}
```



Im vorangehenden Beispiel nimmt die Funktion recordaudiostream den einzelnen Parameter, `pMySink` , ein Zeiger auf ein Objekt, das zu einer Client definierten Klasse, myaudiosink, mit zwei Funktionen (CopyData und SetFormat) gehört. Der Beispielcode enthält nicht die Implementierung von myaudiosink:

-   Keines der Klassenmember kommuniziert direkt mit einer der Methoden in den Schnittstellen in WASAPI.
-   Die Klasse kann auf verschiedene Weise implementiert werden, je nach den Anforderungen des Clients. (Beispielsweise können die Erfassungsdaten in eine WAV-Datei geschrieben werden.)

Informationen zum Vorgang der beiden Methoden sind jedoch nützlich, um das Beispiel zu verstehen.

Die CopyData-Funktion kopiert eine angegebene Anzahl von Audioframes von einem angegebenen Puffer Speicherort. Die Funktion "recordaudiostream" verwendet die CopyData-Funktion, um die Audiodaten aus dem freigegebenen Puffer zu lesen und zu speichern. Die Funktion SetFormat gibt das Format für die CopyData-Funktion an, die für die Daten verwendet werden soll.

Solange das myaudiosink-Objekt zusätzliche Daten erfordert, gibt die CopyData-Funktion den Wert **false** über den dritten Parameter aus, der im vorangehenden Codebeispiel ein Zeiger auf die Variable ist `bDone` . Wenn das myaudiosink-Objekt über alle Daten verfügt, die es erfordert, legt die CopyData-Funktion `bDone` auf **true** fest. Dies bewirkt, dass das Programm die Schleife in der recordaudiostream-Funktion verlässt.

Die Funktion recordaudiostream weist einen freigegebenen Puffer mit einer Dauer von einer Sekunde zu. (Der zugewiesene Puffer kann etwas länger dauern.) Innerhalb der Hauptschleife bewirkt der Aufrufe der Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) -Funktion, dass das Programm eine halbe Sekunde wartet. Zu **Beginn jedes Ruhe** Zustands ist der freigegebene Puffer leer oder fast leer. Wenn der Standby- **Aufruf zurück** kehrt, ist der freigegebene Puffer ungefähr die Hälfte der erfassten Daten.

Nach dem Aufrufen der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode bleibt der Stream geöffnet, bis der Client alle Verweise auf die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle und alle Verweise auf Dienst Schnittstellen freigibt, die vom Client über die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode abgerufen wurden. Der endgültige [**releaseaufrufad**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) schließt den Datenstrom.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> </dl>

 

 
