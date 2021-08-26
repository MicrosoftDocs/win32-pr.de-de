---
description: Erfassen eines Streams
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Erfassen eines Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dda6fd8527acbfff4072a2b79854eca4c32541f57d462b6073f9f6f39854ddb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059030"
---
# <a name="capturing-a-stream"></a>Erfassen eines Streams

Der Client ruft die Methoden in der [**IAudioCaptureClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) auf, um erfasste Daten aus einem Endpunktpuffer zu lesen. Der Client teilt den Endpunktpuffer mit der Audio-Engine im freigegebenen Modus und mit dem Audiogerät im exklusiven Modus. Zum Anfordern eines Endpunktpuffers einer bestimmten Größe ruft der Client die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) auf. Um die Größe des zugeordneten Puffers zu erhalten, die sich von der angeforderten Größe unterscheiden kann, ruft der Client die [**IAudioClient::GetBufferSize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) auf.

Um einen Datenstrom erfasster Daten durch den Endpunktpuffer zu verschieben, ruft der Client alternativ die [**IAudioCaptureClient::GetBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) und die [**IAudioCaptureClient::ReleaseBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) auf. Der Client greifen auf die Daten im Endpunktpuffer als eine Reihe von Datenpaketen zu. Der **GetBuffer-Aufruf** ruft das nächste Paket der erfassten Daten aus dem Puffer ab. Nach dem Lesen der Daten aus dem Paket ruft der Client **ReleaseBuffer** auf, um das Paket frei zu geben und für weitere erfasste Daten verfügbar zu machen.

Die Paketgröße kann von einem [**GetBuffer-Aufruf**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) bis zum nächsten variieren. Vor dem **Aufrufen von GetBuffer** kann der Client die [**IAudioCaptureClient::GetNextPacketSize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) aufrufen, um die Größe des nächsten Pakets im Voraus zu erhalten. Darüber hinaus kann der Client die [**IAudioClient::GetCurrentPadding-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) aufrufen, um die Gesamtmenge der erfassten Daten zu erhalten, die im Puffer verfügbar sind. Die Paketgröße ist immer kleiner oder gleich der Gesamtmenge der erfassten Daten im Puffer.

Während jeder Verarbeitung hat der Client die Möglichkeit, die erfassten Daten auf eine der folgenden Arten zu verarbeiten:

-   Der Client ruft alternativ [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) und [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)auf und liest ein Paket mit jedem Aufrufpaar, bis **GetBuffer** AUDCNT \_ S BUFFEREMPTY zurückgibt, was angibt, dass der Puffer leer \_ ist.
-   Der Client ruft [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) vor jedem Aufrufpaar von [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) und [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) auf, bis **GetNextPacketSize** eine Paketgröße von 0 meldet und angibt, dass der Puffer leer ist.

Die beiden Techniken führen zu gleichwertigen Ergebnissen.

Das folgende Codebeispiel zeigt, wie Sie einen Audiodatenstrom vom Standarderfassungsgerät aufzeichnen:


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



Im vorherigen Beispiel akzeptiert die RecordAudioStream-Funktion einen einzelnen Parameter, , der ein Zeiger auf ein Objekt ist, das zu einer `pMySink` clientdefinierten Klasse, MyAudioSink, mit den beiden Funktionen CopyData und SetFormat gehört. Der Beispielcode enthält die Implementierung von MyAudioSink nicht, da:

-   Keiner der Klassenmitglieder kommuniziert direkt mit einer der Methoden in den Schnittstellen in WASAPI.
-   Die -Klasse kann je nach den Anforderungen des Clients auf unterschiedliche Weise implementiert werden. (Beispielsweise könnten die Erfassungsdaten in eine WAV-Datei geschrieben werden.)

Informationen zum Betrieb der beiden Methoden sind jedoch nützlich, um das Beispiel zu verstehen.

Die CopyData-Funktion kopiert eine angegebene Anzahl von Audioframes von einer angegebenen Pufferposition. Die RecordAudioStream-Funktion verwendet die CopyData-Funktion, um die Audiodaten aus dem freigegebenen Puffer zu lesen und zu speichern. Die SetFormat-Funktion gibt das Format für die CopyData-Funktion an, das für die Daten verwendet werden soll.

Solange das MyAudioSink-Objekt zusätzliche Daten erfordert, gibt die CopyData-Funktion den Wert **FALSE** über den dritten Parameter aus, der im vorherigen Codebeispiel ein Zeiger auf die Variable `bDone` ist. Wenn das MyAudioSink-Objekt über alle benötigten Daten verfügt, legt die CopyData-Funktion auf TRUE fest, wodurch das Programm die Schleife in der `bDone` RecordAudioStream-Funktion beendet. 

Die RecordAudioStream-Funktion weist einen freigegebenen Puffer mit einer Dauer von einer Sekunde zu. (Der zugeordnete Puffer kann eine etwas längere Dauer haben.) Innerhalb der main-Schleife führt der Aufruf der Windows [**Sleep-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-sleep) dazu, dass das Programm eine halbe Sekunde wartet. Zu Beginn jedes **Sleep-Aufrufs** ist der freigegebene Puffer leer oder fast leer. Zum Zeitpunkt der Rückgabe **des Sleep-Aufrufs** wird der freigegebene Puffer ungefähr zur Hälfte mit Erfassungsdaten gefüllt.

Nach dem Aufruf der [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) bleibt der Stream geöffnet, bis der Client alle seine Verweise auf die [**IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) und alle Verweise auf Dienstschnittstellen frei gibt, die der Client über die [**IAudioClient::GetService-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) erhalten hat. Der letzte [**Releaseaufruf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) schließt den Stream.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamverwaltung](stream-management.md)
</dt> </dl>

 

 
