---
description: Rendern eines Streams
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Rendern eines Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96e720bab43c75b0a3958bb3b6137d3a3d9ef6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483478"
---
# <a name="rendering-a-stream"></a>Rendern eines Streams

Der Client ruft die Methoden in der [**iaudiorenderclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) -Schnittstelle auf, um Renderingdaten in einen Endpunkt Puffer zu schreiben. Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine. Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei. Um einen Endpunkt Puffer einer bestimmten Größe anzufordern, ruft der Client die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf. Um die Größe des zugeordneten Puffers zu erhalten, der sich von der angeforderten Größe unterscheiden kann, ruft der Client die [**iaudioclient:: getBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) -Methode auf.

Um einen Stream von Renderingdaten über den Endpunkt Puffer zu verschieben, ruft der Client alternativ die [**iaudiorenderclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Methode und die [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode auf. Der Client greift als eine Reihe von Datenpaketen auf die Daten im Endpunkt Puffer zu. Der **GetBuffer** -Befehl ruft das nächste Paket ab, sodass der Client es mit Renderingdaten auffüllen kann. Nachdem die Daten in das Paket geschrieben wurden, ruft der Client **ReleaseBuffer** auf, um das fertige Paket der renderinganschlange hinzuzufügen.

Bei einem renderingpuffer stellt der von der [**iaudioclient:: getcurrentpadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) -Methode gemeldete Auffüll Wert die Menge der Renderingdaten dar, die in die Warteschlange eingereiht werden, um im Puffer wiedergegeben zu werden. Eine renderinganwendung kann den Füll Wert verwenden, um zu bestimmen, wie viele neue Daten sicher in den Puffer geschrieben werden können, ohne dass zuvor geschriebene Daten überschrieben werden müssen, die von der Audioengine noch nicht aus dem Puffer gelesen wurden. Der verfügbare Speicherplatz ist einfach die Puffergröße abzüglich der Auffüll Größe. Der Client kann eine Paketgröße anfordern, die einen Teil oder den gesamten verfügbaren Speicherplatz im nächsten [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Befehl darstellt.

Die Größe eines Pakets wird in *Audioframes* ausgedrückt. Ein audioframe in einem PCM-Stream besteht aus einem Satz von Stichproben (der Satz enthält ein Beispiel für jeden Kanal im Stream), die wiedergegeben werden oder gleichzeitig aufgezeichnet werden (Takt Takt). Daher ist die Größe eines Audioframes die Stichprobengröße multipliziert mit der Anzahl der Kanäle im Stream. Beispielsweise beträgt die Frame Größe für einen Stereo-Stream (2-Kanal) mit 16-Bit-Stichproben vier Bytes.

Im folgenden Codebeispiel wird gezeigt, wie Sie einen Audiostream auf dem standardmäßigen renderinggerät wiedergeben:


```C++
//-----------------------------------------------------------
// Play an audio stream on the default audio rendering
// device. The PlayAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data to the
// rendering device. The inner loop runs every 1/2 second.
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
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayAudioStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    UINT32 numFramesPadding;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
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

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Get the actual size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // Grab the entire buffer for the initial fill operation.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    // Load the initial data into the shared buffer.
    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                        bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Sleep for half the buffer duration.
        Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

        // See how much buffer space is available.
        hr = pAudioClient->GetCurrentPadding(&numFramesPadding);
        EXIT_ON_ERROR(hr)

        numFramesAvailable = bufferFrameCount - numFramesPadding;

        // Grab all the available space in the shared buffer.
        hr = pRenderClient->GetBuffer(numFramesAvailable, &pData);
        EXIT_ON_ERROR(hr)

        // Get next 1/2-second of data from the audio source.
        hr = pMySource->LoadData(numFramesAvailable, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(numFramesAvailable, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for last data in buffer to play before stopping.
    Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



Im vorangehenden Beispiel nimmt die Funktion playaudiostream den einzelnen Parameter, `pMySource` , ein Zeiger auf ein Objekt, das zu einer Client definierten Klasse, myaudiosource, mit zwei Element Funktionen (LoadData und SetFormat) gehört. Der Beispielcode enthält nicht die Implementierung von myaudiosource aus folgenden Gründen:

-   Keines der Klassenmember kommuniziert direkt mit einer der Methoden in den Schnittstellen in WASAPI.
-   Die Klasse kann auf verschiedene Weise implementiert werden, je nach den Anforderungen des Clients. (Beispielsweise können die Renderingdaten aus einer WAV-Datei gelesen und eine dynamische Konvertierung in das Streamformat durchgeführt werden.)

Einige Informationen über den Betrieb der beiden Funktionen sind jedoch nützlich, um das Beispiel zu verstehen.

Die LoadData-Funktion schreibt eine angegebene Anzahl von Audioframes (erster Parameter) in einen angegebenen Puffer Speicherort (zweiter Parameter). (Bei der Größe eines Audioframes handelt es sich um die Anzahl der Kanäle im Stream multipliziert mit der Stichprobengröße.) Die playaudiostream-Funktion verwendet LoadData, um Teile des freigegebenen Puffers mit Audiodaten zu füllen. Die SetFormat-Funktion gibt das Format für die LoadData-Funktion an, die für die Daten verwendet werden soll. Wenn die LoadData-Funktion in der Lage ist, mindestens einen Frame in den angegebenen Puffer Speicherort zu schreiben, ohne die angegebene Anzahl von Frames zu schreiben, wird die Ruhe in die restlichen Frames geschrieben.

Solange LoadData das Schreiben von mindestens einem Frame mit echten Daten (nicht Stille) an den angegebenen Puffer Speicherort erfolgreich durchläuft, wird 0 über den dritten Parameter ausgegeben, der im vorangehenden Codebeispiel ein Ausgabe Zeiger auf die Variable ist `flags` . Wenn LoadData nicht über Daten verfügt und auch keinen einzelnen Frame in den angegebenen Puffer Speicherort schreiben kann, schreibt er nichts in den Puffer (nicht einmal) und schreibt den Wert von "audclnt \_ bufferflags" \_ in die `flags` Variable. Die- `flags` Variable überträgt diesen Wert an die [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode, die antwortet, indem Sie die angegebene Anzahl von Frames im Puffer mit Ruhe füllt.

Beim Abrufen der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode fordert die playaudiostream-Funktion im vorangehenden Beispiel einen freigegebenen Puffer an, der eine Sekunde Dauer von einer Sekunde hat. (Der zugewiesene Puffer kann etwas länger dauern.) Bei den ersten Aufrufen der [**iaudiorenderclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Methode und der [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode füllt die Funktion den gesamten Puffer aus, bevor die [**iaudioclient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) -Methode aufgerufen wird, um die Wiedergabe des Puffers zu beginnen.

Innerhalb der Hauptschleife füllt die Funktion die Hälfte des Puffers in Intervallen von halb Sekunden iterativ auf. Unmittelbar vor jedem Aufrufe der Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) -Funktion in der Hauptschleife ist der Puffer voll oder fast voll. Wenn der Standby-Rückruf zurückgegeben wird, **ist der Puffer** ungefähr halb voll. Die Schleife wird beendet, nachdem der letzte-Befehl der LoadData-Funktion die- `flags` Variable auf den Wert "audclnt \_ bufferflags Silent" festgelegt hat \_ . Zu diesem Zeitpunkt enthält der Puffer mindestens einen Frame mit echten Daten und kann so viel wie eine halbe Sekunde an echten Daten enthalten. Der Rest des Puffers enthält Ruhe. Der Standby **-Aufruf, der auf** die Schleife folgt, bietet ausreichend Zeit (eine halbe Sekunde), um alle verbleibenden Daten wiederzugeben. Die Stille, die auf die Daten folgt, verhindert unerwünschte Sounds, bevor der Aufrufe der [**iaudioclient:: Stopp**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) -Methode den Audiodatenstrom stoppt. Weitere **Informationen zum** Standbymodus finden Sie in der Windows SDK-Dokumentation.

Nach dem Aufrufen der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode bleibt der Stream geöffnet, bis der Client alle Verweise auf die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle und alle Verweise auf Dienst Schnittstellen freigibt, die vom Client über die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode abgerufen wurden. Der endgültige [**releaseaufrufad**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) schließt den Datenstrom.

Die Funktion playaudiostream im vorangehenden Codebeispiel ruft die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf, um einen Enumerator für die audioendpunktgeräte im System zu erstellen. Wenn das aufrufende Programm die **CoCreateInstance** -Funktion oder die [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion nicht zum Initialisieren der com-Bibliothek aufgerufen hat, tritt beim **CoCreateInstance** -Aufruf ein Fehler auf. Weitere Informationen zu **cokreateinstance**, **cokreateinstance** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> </dl>

 

 
