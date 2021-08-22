---
description: Rendern eines Streams
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Rendern eines Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a49632e89e42e4e353cec48ee993f990904bc4557c0f63fcaec4d13bed5becf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318570"
---
# <a name="rendering-a-stream"></a>Rendern eines Streams

Der Client ruft die Methoden in der [**IAudioRenderClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) auf, um Renderingdaten in einen Endpunktpuffer zu schreiben. Für einen Datenstrom im freigegebenen Modus teilt sich der Client den Endpunktpuffer mit der Audio-Engine. Für einen Stream im exklusiven Modus teilt sich der Client den Endpunktpuffer mit dem Audiogerät. Um einen Endpunktpuffer einer bestimmten Größe anzufordern, ruft der Client die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) auf. Um die Größe des zugeordneten Puffers abzurufen, die sich von der angeforderten Größe unterscheiden kann, ruft der Client die [**IAudioClient::GetBufferSize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) auf.

Um einen Stream von Renderingdaten durch den Endpunktpuffer zu verschieben, ruft der Client alternativ die [**IAudioRenderClient::GetBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) und die [**IAudioRenderClient::ReleaseBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) auf. Der Client greift als Reihe von Datenpaketen auf die Daten im Endpunktpuffer zu. Der **GetBuffer-Aufruf** ruft das nächste Paket ab, sodass der Client es mit Renderingdaten füllen kann. Nachdem die Daten in das Paket geschrieben wurden, ruft der Client **ReleaseBuffer** auf, um das fertige Paket der Renderingwarteschlange hinzuzufügen.

Bei einem Renderingpuffer stellt der von der [**IAudioClient::GetCurrentPadding-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) gemeldete Auffüllwert die Menge der Renderingdaten dar, die in der Warteschlange stehen, um im Puffer wiedergegeben zu werden. Eine Renderinganwendung kann den Auffüllwert verwenden, um zu bestimmen, wie viele neue Daten sicher in den Puffer geschrieben werden können, ohne dass das Risiko besteht, zuvor geschriebene Daten zu überschreiben, die die Audio-Engine noch nicht aus dem Puffer gelesen hat. Der verfügbare Speicherplatz ist einfach die Puffergröße minus der Auffüllungsgröße. Der Client kann eine Paketgröße anfordern, die einen Teil oder den gesamten verfügbaren Speicherplatz im nächsten [**GetBuffer-Aufruf**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) darstellt.

Die Größe eines Pakets wird in *Audioframes* ausgedrückt. Ein Audioframe in einem PCM-Stream ist ein Satz von Beispielen (der Satz enthält ein Beispiel für jeden Kanal im Stream), die wiedergegeben oder gleichzeitig aufgezeichnet werden (Takt im Takt). Daher entspricht die Größe eines Audioframes der Stichprobengröße multipliziert mit der Anzahl der Kanäle im Stream. Beispielsweise beträgt die Framegröße für einen Stereodatenstrom (2-Kanal) mit 16-Bit-Stichproben vier Bytes.

Das folgende Codebeispiel zeigt, wie Sie einen Audiostream auf dem Standardrenderinggerät wiedergeben:


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



Im vorherigen Beispiel verwendet die PlayAudioStream-Funktion einen einzelnen Parameter, `pMySource` , der ein Zeiger auf ein Objekt ist, das zu einer clientdefinierten Klasse myAudioSource gehört, mit zwei Memberfunktionen, LoadData und SetFormat. Der Beispielcode enthält die Implementierung von MyAudioSource aus folgenden Grund nicht:

-   Keiner der Klassenmember kommuniziert direkt mit einer der Methoden in den Schnittstellen in WASAPI.
-   Die -Klasse kann abhängig von den Anforderungen des Clients auf verschiedene Weise implementiert werden. (Es kann z. B. die Renderingdaten aus einer WAV-Datei lesen und eine on-the-fly-Konvertierung in das Streamformat ausführen.)

Einige Informationen zum Betrieb der beiden Funktionen sind jedoch nützlich, um das Beispiel zu verstehen.

Die LoadData-Funktion schreibt eine angegebene Anzahl von Audioframes (erster Parameter) in eine angegebene Pufferposition (zweiter Parameter). (Die Größe eines Audioframes ist die Anzahl der Kanäle im Stream multipliziert mit der Stichprobengröße.) Die PlayAudioStream-Funktion verwendet LoadData, um Teile des freigegebenen Puffers mit Audiodaten aufzufüllen. Die SetFormat-Funktion gibt das Format für die LoadData-Funktion an, das für die Daten verwendet werden soll. Wenn die LoadData-Funktion in der Lage ist, mindestens einen Frame in die angegebene Pufferposition zu schreiben, aber keine Daten mehr vorhanden sind, bevor sie die angegebene Anzahl von Frames geschrieben hat, schreibt sie Stille in die verbleibenden Frames.

Solange LoadData erfolgreich mindestens einen Frame realer Daten (nicht Stille) an die angegebene Pufferposition schreibt, gibt es 0 über den dritten Parameter aus, der im vorherigen Codebeispiel ein Ausgabezeiger auf die `flags` Variable ist. Wenn LoadData nicht mehr über Daten verfügt und nicht einmal einen einzelnen Frame in die angegebene Pufferposition schreiben kann, wird nichts in den Puffer geschrieben (nicht einmal Stille), und der Wert AUDCLNT \_ BUFFERFLAGS SILENT wird in die Variable \_ `flags` geschrieben. Die `flags` Variable übergibt diesen Wert an die [**IAudioRenderClient::ReleaseBuffer-Methode,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) die antwortet, indem die angegebene Anzahl von Frames im Puffer mit Stille gefüllt wird.

Beim Aufruf der [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) fordert die PlayAudioStream-Funktion im vorherigen Beispiel einen freigegebenen Puffer mit einer Dauer von einer Sekunde an. (Der zugeordnete Puffer kann eine etwas längere Dauer haben.) In den ersten Aufrufen der Methoden [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) und [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) füllt die Funktion den gesamten Puffer aus, bevor die [**IAudioClient::Start-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) aufgerufen wird, um mit der Wiedergabe des Puffers zu beginnen.

Innerhalb der Main-Schleife füllt die Funktion die Hälfte des Puffers in Intervallen von halber Sekunde iterativ aus. Unmittelbar vor jedem Aufruf der Windows [**Sleep-Funktion**](/windows/win32/api/synchapi/nf-synchapi-sleep) in der Main-Schleife ist der Puffer voll oder fast voll. Wenn der **Sleep-Aufruf** zurückgegeben wird, ist der Puffer etwa halb voll. Die Schleife endet, nachdem der letzte Aufruf der LoadData-Funktion die `flags` Variable auf den Wert AUDCLNT \_ BUFFERFLAGS SILENT festgelegt \_ hat. An diesem Punkt enthält der Puffer mindestens einen Frame mit echten Daten und kann bis zu einer halben Sekunde an echten Daten enthalten. Der Rest des Puffers enthält Stille. Der **Sleep-Aufruf,** der der Schleife folgt, bietet ausreichend Zeit (eine halbe Sekunde), um alle verbleibenden Daten wiederzuspielen. Die Ruhe, die auf die Daten folgt, verhindert unerwünschte Sounds, bevor der Aufruf der [**IAudioClient::Stop-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) den Audiostream beendet. Weitere Informationen zum **Standbymodus** finden Sie in der Windows SDK-Dokumentation.

Nach dem Aufruf der [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) bleibt der Stream geöffnet, bis der Client alle seine Verweise auf die [**IAudioClient-Schnittstelle**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) und alle Verweise auf Dienstschnittstellen freigibt, die der Client über die [**IAudioClient::GetService-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) abgerufen hat. Der letzte [**Releaseaufruf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) schließt den Stream.

Die PlayAudioStream-Funktion im vorherigen Codebeispiel ruft die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um einen Enumerator für die Audioendpunktgeräte im System zu erstellen. Der **CoCreateInstance-Aufruf** schlägt fehl, es sei denn, das aufrufende Programm hat zuvor entweder die **CoCreateInstance-** oder [**CoInitializeEx-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) aufgerufen, um die COM-Bibliothek zu initialisieren. Weitere Informationen zu **CoCreateInstance,** **CoCreateInstance** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamverwaltung](stream-management.md)
</dt> </dl>

 

 
