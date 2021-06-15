---
description: Exclusive-Mode Streams
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677efa83d099bd32ddb0674414e25a9af219bd1a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068586"
---
# <a name="exclusive-mode-streams"></a>Exclusive-Mode Streams

Wie bereits erläutert, verwendet die Anwendung beim Öffnen eines Streams im exklusiven Modus ausschließlich das Audioendpunktgerät, das den Stream abgespielt oder aufzeichnet. Im Gegensatz dazu können mehrere Anwendungen ein Audioendpunktgerät gemeinsam nutzen, indem datenströme im freigegebenen Modus auf dem Gerät geöffnet werden.

Der Zugriff im exklusiven Modus auf ein Audiogerät kann wichtige Systemsounds blockieren, die Interoperabilität mit anderen Anwendungen verhindern und andernfalls die Benutzerfreundlichkeit beeinträchtigen. Um diese Probleme zu beheben, gibt eine Anwendung mit einem Stream im exklusiven Modus in der Regel die Kontrolle über das Audiogerät ab, wenn die Anwendung nicht der Vordergrundprozess ist oder nicht aktiv streamt.

Streamlatenz ist die Verzögerung, die dem Datenpfad inhärent ist, der den Endpunktpuffer einer Anwendung mit einem Audioendpunktgerät verbindet. Bei einem Renderingstream ist die Latenz die maximale Verzögerung von der Zeit, zu der eine Anwendung eine Stichprobe in einen Endpunktpuffer schreibt, bis zu dem Zeitpunkt, zu dem das Beispiel über die Lautsprecher gehört wird. Bei einem Erfassungsdatenstrom ist die Latenz die maximale Verzögerung von der Zeit, zu der ein Sound in das Mikrofon eintritt, bis zu dem Zeitpunkt, zu dem eine Anwendung das Beispiel für diesen Sound aus dem Endpunktpuffer lesen kann.

Anwendungen, die Streams im exklusiven Modus verwenden, tun dies häufig, da sie niedrige Latenzen in den Datenpfaden zwischen den Audioendpunktgeräten und den Anwendungsthreads erfordern, die auf die Endpunktpuffer zugreifen. In der Regel werden diese Threads mit relativ hoher Priorität ausgeführt, und sie planen die Ausführung in regelmäßigen Intervallen, die dem periodischen Intervall entsprechen, das nachfolgende Verarbeitungsdurchläufe durch die Audiohardware trennt. Während jedes Durchlaufs verarbeitet die Audiohardware die neuen Daten in den Endpunktpuffern.

Um die kleinsten Streamlatenzzeiten zu erzielen, benötigt eine Anwendung möglicherweise sowohl spezielle Audiohardware als auch ein Leicht geladenes Computersystem. Wenn die Audiohardware über die Zeitlimits hinausgeht oder das System mit konkurrierenden Aufgaben mit hoher Priorität geladen wird, kann dies zu einer Störung in einem Audiostream mit geringer Latenz führen. Bei einem Renderingstream kann beispielsweise eine Störung auftreten, wenn die Anwendung nicht in einen Endpunktpuffer schreiben kann, bevor die Audiohardware den Puffer liest, oder wenn die Hardware den Puffer nicht lesen kann, bevor die Wiedergabe des Puffers geplant ist. In der Regel sollte eine Anwendung, die auf einer Vielzahl von Audiohardware und in einer vielzahl von Systemen ausgeführt werden soll, ihre Zeitanforderungen so lockern, dass Störungen in allen Zielumgebungen vermieden werden.

Windows Vista verfügt über mehrere Features zur Unterstützung von Anwendungen, die Audiostreams mit geringer Latenz erfordern. Wie unter [Benutzermodus-Audiokomponenten](user-mode-audio-components.md)erläutert, können Anwendungen, die zeitkritische Vorgänge ausführen, die MMCSS-Funktionen (Multimedia Class Scheduler Service) aufrufen, um die Threadpriorität zu erhöhen, ohne CPU-Ressourcen für Anwendungen mit niedrigerer Priorität zu verweigern. Darüber hinaus unterstützt die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) ein AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK-Flag, mit dem der Pufferwartungsthread einer Anwendung die Ausführung planen kann, wenn ein neuer Puffer vom Audiogerät verfügbar wird. Durch die Verwendung dieser Features kann ein Anwendungsthread die Unklarheit darüber reduzieren, wann er ausgeführt wird, wodurch das Risiko von Störungen in einem Audiodatenstrom mit geringer Latenz verringert wird.

Die Treiber für ältere Audioadapter verwenden wahrscheinlich die WaveCyclic- oder WavePci-Gerätetreiberschnittstelle (Device Driver Interface, DDI), während die Treiber für neuere Audioadapter die WaveRT-DDI eher unterstützen. Bei Anwendungen im exklusiven Modus können WaveRT-Treiber eine bessere Leistung bieten als WaveCyclic- oder WavePci-Treiber, aber WaveRT-Treiber erfordern zusätzliche Hardwarefunktionen. Zu diesen Funktionen gehört die Möglichkeit, Hardwarepuffer direkt für Anwendungen freizugeben. Bei direkter Freigabe ist kein Systemeingriff erforderlich, um Daten zwischen einer Anwendung im exklusiven Modus und der Audiohardware zu übertragen. Im Gegensatz dazu eignen sich WaveCyclic- und WavePci-Treiber für ältere, weniger leistungsfähige Audioadapter. Diese Adapter verwenden Systemsoftware, um Datenblöcke (angefügt an System-E/A-Anforderungspakete oder IRPs) zwischen Anwendungspuffern und Hardwarepuffern zu übertragen. Darüber hinaus verwenden USB-Audiogeräte Systemsoftware, um Daten zwischen Anwendungspuffern und Hardwarepuffern zu übertragen. Um die Leistung von Anwendungen im exklusiven Modus zu verbessern, die eine Verbindung mit Audiogeräten herstellen, die das System für den Datentransport verwenden, erhöht WASAPI automatisch die Priorität der Systemthreads, die Daten zwischen den Anwendungen und der Hardware übertragen. WASAPI verwendet MMCSS, um die Threadpriorität zu erhöhen. Wenn ein Systemthread in Windows Vista den Datentransport für einen Audiowiedergabestream im exklusiven Modus mit einem PCM-Format und einem Gerätezeitraum von weniger als 10 Millisekunden verwaltet, weist WASAPI dem Thread den MMCSS-Aufgabennamen "Pro Audio" zu. Wenn der Gerätezeitraum des Streams größer oder gleich 10 Millisekunden ist, weist WASAPI dem Thread den MMCSS-Aufgabennamen "Audio" zu. Weitere Informationen zu den WaveCyclic-, WavePci- und WaveRT-DDIs finden Sie in der Windows DDK-Dokumentation. Informationen zum Auswählen eines geeigneten Gerätezeitraums finden Sie unter [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).

Wie unter [Sitzungsvolumesteuerelemente](session-volume-controls.md)beschrieben, stellt [WASAPI](wasapi.md) die Schnittstellen [**ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) zum Steuern der Lautstärkeebenen von Audiostreams im freigegebenen Modus bereit. Die Steuerelemente in diesen Schnittstellen haben jedoch keine Auswirkungen auf Streams im exklusiven Modus. Stattdessen verwenden Anwendungen, die Streams im exklusiven Modus verwalten, in der Regel die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) in der [EndpointVolume-API,](endpointvolume-api.md) um die Volumeebenen dieser Streams zu steuern. Informationen zu dieser Schnittstelle finden Sie unter [Endpunktvolumesteuerelemente.](endpoint-volume-controls.md)

Für jedes Wiedergabegerät und Erfassungsgerät im System kann der Benutzer steuern, ob das Gerät im exklusiven Modus verwendet werden kann. Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus deaktiviert, kann das Gerät verwendet werden, um nur Streams im freigegebenen Modus wiederzugeben oder aufzuzeichnen.

Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus aktiviert, kann der Benutzer auch steuern, ob eine Anforderung einer Anwendung, das Gerät im exklusiven Modus zu verwenden, der Verwendung des Geräts durch Anwendungen vorkommt, die derzeit Streams im freigegebenen Modus über das Gerät wiedergeben oder aufzeichnen. Wenn die Vorzeitigemption aktiviert ist, ist eine Anforderung einer Anwendung, die exklusive Kontrolle über das Gerät zu übernehmen, erfolgreich, wenn das Gerät derzeit nicht verwendet wird oder wenn das Gerät im freigegebenen Modus verwendet wird. Die Anforderung schlägt jedoch fehl, wenn eine andere Anwendung bereits über die exklusive Kontrolle über das Gerät verfügt. Wenn die Vorzeitigemption deaktiviert ist, ist eine Anforderung einer Anwendung, die exklusive Kontrolle über das Gerät zu übernehmen, erfolgreich, wenn das Gerät derzeit nicht verwendet wird. Die Anforderung schlägt jedoch fehl, wenn das Gerät bereits im freigegebenen modus oder im exklusiven Modus verwendet wird.

In Windows Vista sind die Standardeinstellungen für ein Audioendpunktgerät die folgenden:

-   Das Gerät kann verwendet werden, um Streams im exklusiven Modus wiederzugeben oder aufzuzeichnen.
-   Eine Anforderung, ein Gerät zum Wiedergeben oder Aufzeichnen eines Streams im exklusiven Modus zu verwenden, setzt alle Datenströme im freigegebenen Modus voraus, die derzeit über das Gerät wiedergegeben oder aufgezeichnet werden.

**So ändern Sie die Einstellungen im exklusiven Modus eines Wiedergabe- oder Aufzeichnungsgeräts**

1.  Klicken Sie mit der rechten Maustaste auf das Lautsprechersymbol im Infobereich auf der rechten Seite der Taskleiste, und wählen Sie **Wiedergabegeräte** oder **Aufzeichnungsgeräte** aus. (Alternativ können Sie die Windows-Multimedia-Systemsteuerung Mmsys.cpl über ein Eingabeaufforderungsfenster ausführen. Weitere Informationen finden Sie unter Hinweise in [DEVICE \_ STATE \_ XXX-Konstanten](device-state-xxx-constants.md).)
2.  Nachdem das Fenster **Sound** angezeigt wird, wählen Sie **Wiedergabe** oder **Aufzeichnung** aus. Wählen Sie als Nächstes einen Eintrag in der Liste der Gerätenamen aus, und klicken Sie auf **Eigenschaften.**
3.  Nachdem das Fenster **Eigenschaften** angezeigt wird, klicken Sie auf **Erweitert.**
4.  Um Anwendungen die Verwendung des Geräts im exklusiven Modus zu ermöglichen, aktivieren Sie das Kontrollkästchen Zulassen, dass **Anwendungen die exklusive Kontrolle über dieses Gerät übernehmen.** Deaktivieren Sie das Kontrollkästchen, um die Verwendung des Geräts im exklusiven Modus zu deaktivieren.
5.  Wenn die Verwendung des Geräts im exklusiven Modus aktiviert ist, können Sie angeben, ob eine Anforderung zur exklusiven Steuerung des Geräts erfolgreich ist, wenn das Gerät derzeit Streams im freigegebenen Modus abspielt oder aufzeichnet. Aktivieren Sie das Kontrollkästchen Anwendungen im exklusiven Modus Priorität geben, um Anwendungen im **exklusiven Modus** Vorrang vor Anwendungen im gemeinsam genutzten Modus zu geben. Deaktivieren Sie das Kontrollkästchen, um die Priorität von Anwendungen im exklusiven Modus gegenüber Anwendungen im freigegebenen Modus zu verweigern.

Das folgende Codebeispiel zeigt, wie Sie einen Audiostream mit geringer Latenz auf einem Audiorenderinggerät wiedergeben, das für die Verwendung im exklusiven Modus konfiguriert ist:


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
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

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;
    DWORD taskIndex = 0;
    
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

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    if (hr == AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED) {
        // Align the buffer if needed, see IAudioClient::Initialize() documentation
        UINT32 nFrames = 0;
        hr = pAudioClient->GetBufferSize(&nFrames);
        EXIT_ON_ERROR(hr)
        hnsRequestedDuration = (REFERENCE_TIME)((double)REFTIMES_PER_SEC / pwfx->nSamplesPerSec * nFrames + 0.5);
        hr = pAudioClient->Initialize(
            AUDCLNT_SHAREMODE_EXCLUSIVE,
            AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
            hnsRequestedDuration,
            hnsRequestedDuration,
            pwfx,
            NULL);
    }
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



Im vorherigen Codebeispiel wird die PlayExclusiveStream-Funktion im Anwendungsthread ausgeführt, der die Endpunktpuffer wartet, während ein Renderingstream wiedergegeben wird. Die Funktion verwendet einen einzelnen Parameter, pMySource, der ein Zeiger auf ein Objekt ist, das zu einer vom Client definierten Klasse MyAudioSource gehört. Diese Klasse verfügt über zwei Memberfunktionen, LoadData und SetFormat, die im Codebeispiel aufgerufen werden. MyAudioSource wird unter [Rendern eines Streams](rendering-a-stream.md)beschrieben.

Die PlayExclusiveStream-Funktion ruft die Hilfsfunktion GetStreamFormat auf, die mit dem Standardrenderinggerät aushandelt, um zu bestimmen, ob das Gerät ein Streamformat im exklusiven Modus unterstützt, das für die Verwendung durch die Anwendung geeignet ist. Der Code für die GetStreamFormat-Funktion wird im Codebeispiel nicht angezeigt. Dies liegt daran, dass die Details der Implementierung vollständig von den Anforderungen der Anwendung abhängen. Der Vorgang der GetStreamFormat-Funktion kann jedoch einfach beschrieben werden. Sie ruft die [**IAudioClient::IsFormatSupported-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) ein oder mehrere Male auf, um zu bestimmen, ob das Gerät ein geeignetes Format unterstützt. Die Anforderungen der Anwendung legen fest, welche Formate GetStreamFormat der **IsFormatSupported-Methode** und in welcher Reihenfolge sie präsentiert werden. Weitere Informationen zu **IsFormatSupported** finden Sie unter [Geräteformate.](device-formats.md)

Nach dem GetStreamFormat-Aufruf ruft die PlayExclusiveStream-Funktion die [**IAudioClient::GetDevicePeriod-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) auf, um den minimalen Gerätezeitraum abzurufen, der von der Audiohardware unterstützt wird. Als Nächstes ruft die Funktion die [**IAudioClient::Initialize-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) auf, um eine Pufferdauer anzufordern, die dem Mindestzeitraum entspricht. Wenn der Aufruf erfolgreich ist, ordnet die **Initialize-Methode** zwei Endpunktpuffer zu, von denen jeder der Mindestdauer entspricht. Wenn der Audiostream später ausgeführt wird, teilen sich die Anwendung und die Audiohardware die beiden Puffer "ping-pong", d. h., während die Anwendung in einen Puffer schreibt, liest die Hardware aus dem anderen Puffer.

Vor dem Starten des Streams führt die PlayExclusiveStream-Funktion Folgendes aus:

-   Erstellt und registriert das Ereignishandle, über das Benachrichtigungen empfangen werden, wenn Puffer gefüllt werden können.
-   Füllt den ersten Puffer mit Daten aus der Audioquelle aus, um die Verzögerung von der Ausführung des Streams bis zu dem Zeitpunkt zu reduzieren, zu dem der erste Sound gehört wird.
-   Ruft die **AvSetMmThreadCharacteristics-Funktion** auf, um anzufordern, dass MMCSS die Priorität des Threads erhöht, in dem PlayExclusiveStream ausgeführt wird. (Wenn die Ausführung des Streams beendet wird, stellt der **AvRevertMmThreadCharacteristics-Funktionsaufruf** die ursprüngliche Threadpriorität wieder her.)

Weitere Informationen zu **AvSetMmThreadCharacteristics** und **AvRevertMmThreadCharacteristics** finden Sie in der Windows SDK-Dokumentation.

Während der Stream ausgeführt wird, füllt jede Iteration von **while**-loop im vorherigen Codebeispiel einen Endpunktpuffer aus. Zwischen Iterationen wartet der **WaitForSingleObject-Funktionsaufruf,** bis das Ereignishandle signalisiert wird. Wenn das Handle signalisiert wird, führt der Schleifentext Folgendes aus:

1.  Ruft die [**IAudioRenderClient::GetBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) auf, um den nächsten Puffer abzurufen.
2.  Füllt den Puffer aus.
3.  Ruft die [**IAudioRenderClient::ReleaseBuffer-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) auf, um den Puffer freizugeben.

Weitere Informationen zu **WaitForSingleObject** finden Sie in der Windows SDK-Dokumentation.

Wenn der Audioadapter von einem WaveRT-Treiber gesteuert wird, ist die Signalisierung des Ereignishandle an die DMA-Übertragungsbenachrichtigungen von der Audiohardware gebunden. Für ein USB-Audiogerät oder für ein Audiogerät, das von einem WaveCyclic- oder WavePci-Treiber gesteuert wird, ist die Signalisierung des Ereignishandle an Vervollständigungen der IRPs gebunden, die Daten aus dem Anwendungspuffer in den Hardwarepuffer übertragen.

Im obigen Codebeispiel werden die Audiohardware und das Computersystem an ihre Leistungsgrenzen gepusht. Um zunächst die Streamlatenz zu reduzieren, plant die Anwendung ihren Pufferwartungsthread so, dass er den minimalen Gerätezeitraum verwendet, den die Audiohardware unterstützt. Zweitens legt der **AvSetMmThreadCharacteristics-Funktionsaufruf** den TaskName-Parameter auf "Pro Audio" fest, d.h. in Windows Vista den Standardtasknamen mit der höchsten Priorität, um sicherzustellen, dass der Thread innerhalb jedes Gerätezeitraums zuverlässig ausgeführt wird. Überlegen Sie, ob die Zeitlichen Anforderungen Ihrer Anwendung möglicherweise gelockert werden, ohne ihre Nützlichkeit zu beeinträchtigen. Beispielsweise kann die Anwendung ihren Pufferwartungsthread so planen, dass er einen Zeitraum verwendet, der länger als der mindeste ist. Ein längerer Zeitraum kann die Verwendung einer niedrigeren Threadpriorität sicher zulassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamverwaltung](stream-management.md)
</dt> </dl>

 

 



