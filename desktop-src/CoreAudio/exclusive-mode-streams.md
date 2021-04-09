---
description: Exclusive-Mode Streams
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7722dd3463346e976f30a77949f56026a2425624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958386"
---
# <a name="exclusive-mode-streams"></a>Exclusive-Mode Streams

Wie bereits erläutert, hat die Anwendung, wenn eine Anwendung einen Stream im exklusiven Modus öffnet, die ausschließliche Verwendung des audioendpunktgeräts, das den Stream wieder gibt oder aufzeichnet. Im Gegensatz dazu können mehrere Anwendungen ein audioendpunktgerät gemeinsam nutzen, indem Datenströme im freigegebenen Modus auf dem Gerät geöffnet werden.

Der Zugriff auf ein Audiogerät im exklusiven Modus kann wichtige Systemsounds blockieren, die Interoperabilität mit anderen Anwendungen verhindern und die Benutzer Leistung anderweitig beeinträchtigen. Um diese Probleme zu beheben, gibt eine Anwendung mit einem Stream im exklusiven Modus normalerweise die Kontrolle über das Audiogerät aus, wenn die Anwendung nicht der Vordergrund Prozess ist oder kein aktives Streaming durchführt.

Die Datenstrom Latenz ist die Verzögerung, die dem Dateipfad zugrunde liegt, der den Endpunkt Puffer einer Anwendung mit einem audioendpunktgerät verbindet. Bei einem renderingstream ist die Latenz die maximale Verzögerung ab dem Zeitpunkt, an dem eine Anwendung ein Beispiel in einen Endpunkt Puffer schreibt, bis zu dem Zeitpunkt, an dem das Beispiel durch die Referenten gehört. Bei einem Aufzeichnungsdaten Strom ist die Latenz die maximale Verzögerung ab dem Zeitpunkt, an dem ein Sound das Mikrofon in den Zeitraum eingibt, in dem eine Anwendung das Beispiel für diesen Sound aus dem Endpunkt Puffer lesen kann.

Anwendungen, die streamingstreamstreams verwenden, werden häufig verwendet, da Sie niedrige Latenzzeiten in den Daten Pfaden zwischen den audioendpunktgeräten und den Anwendungsthreads erfordern, die auf die Endpunkt Puffer zugreifen. Diese Threads werden in der Regel mit einer relativ hohen Priorität ausgeführt und planen die Ausführung in regelmäßigen Abständen, die sich in der Nähe oder demselben Intervall befinden, in dem aufeinander folgende Verarbeitungs Durchgänge von der Audiohardware getrennt werden. Bei jedem Durchlauf verarbeitet die Audiohardware die neuen Daten in den Endpunkt Puffern.

Um die kleinsten streamlatenzen zu erzielen, benötigt eine Anwendung möglicherweise sowohl spezielle Audiohardware als auch ein Computersystem, das leicht ausgelastet ist. Wenn Sie die Audiohardware über die Zeitlimits hinaus setzen oder das System mit konkurrierenden Aufgaben mit hoher Priorität laden, kann dies zu einem Fehler in einem Audiostream mit niedriger Latenz führen. Beispielsweise kann bei einem renderingstream ein Fehler auftreten, wenn die Anwendung nicht in einen Endpunkt Puffer schreiben kann, bevor die Audiohardware den Puffer liest, oder wenn die Hardware den Puffer vor dem Zeitpunkt der Wiedergabe des Puffers nicht lesen kann. In der Regel sollte eine Anwendung, die auf einer großen Bandbreite von Audiohardware und in einer Vielzahl von Systemen ausgeführt werden soll, die Zeit Steuerungsanforderungen so lockern, dass Sie in allen Ziel Umgebungen einen Fehler vermeiden.

Windows Vista verfügt über mehrere Features zur Unterstützung von Anwendungen, die Audiostreams mit niedriger Latenz benötigen. Wie unter [benutzermodusaudiokomponenten](user-mode-audio-components.md)erläutert, können Anwendungen, die zeitkritische Vorgänge ausführen, die MMCSS-Funktionen (Multimedia Class Scheduler Service) zum Erhöhen der Thread Priorität aufruft, ohne dass CPU-Ressourcen Anwendungen mit niedrigerer Priorität verweigert werden. Darüber hinaus unterstützt die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode ein \_ \_ Ereignis Rückruf-Flag von audclnt StreamFlags, das es dem Puffer Wartungs Thread einer Anwendung ermöglicht, die Ausführung zu planen, wenn ein neuer Puffer vom Audiogerät verfügbar wird. Durch die Verwendung dieser Features kann ein Anwendungs Thread die Sicherheits Anfälligkeit verringern, wenn er ausgeführt wird. Dadurch wird das Risiko eines Fehlers bei einem Audiostream mit niedriger Latenz verringert.

Die Treiber für ältere Audioadapter verwenden wahrscheinlich die Gerätetreiber Schnittstelle (DDI) wavecyclic oder wavepci, wohingegen die Treiber für neuere Audioadapter wahrscheinlich den WaveRT-DDI unterstützen. Für Anwendungen im exklusiven Modus können WaveRT-Treiber eine bessere Leistung als wavecyclic-oder wavepci-Treiber bereitstellen, aber WaveRT-Treiber erfordern zusätzliche Hardwarefunktionen. Zu diesen Funktionen gehört die Möglichkeit, Hardware Puffer direkt für Anwendungen freizugeben. Bei direkter Freigabe ist kein System Eingriff erforderlich, um Daten zwischen einer Anwendung im exklusiven Modus und der Audiohardware zu übertragen. Im Gegensatz dazu eignen sich wavecyclic-und wavepci-Treiber für ältere, weniger leistungsfähige Audioadapter. Diese Adapter basieren auf Systemsoftware zum Transportieren von Datenblöcken (die an System-e/a-Anforderungs Pakete oder-nach Richt Paketen angefügt sind) zwischen Anwendungs Puffern und Hardware Puffern. Außerdem basieren USB-Audiogeräte auf Systemsoftware, um Daten zwischen Anwendungs Puffern und Hardware Puffern zu transportieren. Um die Leistung von Anwendungen im exklusiven Modus zu verbessern, die eine Verbindung mit Audiogeräten herstellen, die auf dem System für den Datentransport basieren, erhöht WASAPI automatisch die Priorität der Systemthreads, die Daten zwischen den Anwendungen und der Hardware übertragen. WASAPI verwendet MMCSS, um die Thread Priorität zu erhöhen. Wenn ein System Thread in Windows Vista den Datentransport für einen Audiowiedergabe-Stream im exklusiven Modus mit einem PCM-Format und einem Geräte Zeitraum von weniger als 10 Millisekunden verwaltet, weist WASAPI dem Thread den MMCSS-Aufgaben Namen "pro-Audiodatei" zu. Wenn der Geräte Zeitraum des Streams größer oder gleich 10 Millisekunden ist, weist WASAPI dem Thread den MMCSS-Aufgaben Namen "Audiodatei" zu. Weitere Informationen zu wavecyclic, wavepci und WaveRT DDIs finden Sie in der Windows-DDK-Dokumentation. Weitere Informationen zum Auswählen eines geeigneten Geräte Zeitraums finden Sie unter [**iaudioclient:: getdeviceperiod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).

Wie unter [Sitzungs Volume](session-volume-controls.md)-Steuerelemente beschrieben, bietet [WASAPI](wasapi.md) die Schnittstellen [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) zum Steuern der volumeebenen von Audiodatenströmen im freigegebenen Modus. Die Steuerelemente in diesen Schnittstellen wirken sich jedoch nicht auf Datenströme im exklusiven Modus aus. Anwendungen, die Stream im exklusiven Modus verwalten, verwenden stattdessen in der Regel die Schnittstelle [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) in der [endpointvolume-API](endpointvolume-api.md) , um die volumeebenen dieser Streams zu steuern. Weitere Informationen zu dieser Schnittstelle finden Sie unter [EndPoint Volume](endpoint-volume-controls.md)-Steuerelemente.

Der Benutzer kann für jedes Wiedergabe Gerät und Erfassungsgerät im System steuern, ob das Gerät im exklusiven Modus verwendet werden kann. Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus deaktiviert, kann das Gerät verwendet werden, um nur Datenströme im freigegebenen Modus wiederzugeben oder aufzuzeichnen.

Wenn der Benutzer die Verwendung des Geräts im exklusiven Modus ermöglicht, kann der Benutzer auch steuern, ob eine Anforderung von einer Anwendung, das Gerät im exklusiven Modus zu verwenden, der Verwendung des Geräts durch Anwendungen vorangestellt wird, die möglicherweise gerade wiedergeben oder die Datenströme im freigegebenen Modus über das Gerät aufzeichnen. Wenn die vorab Entfernung aktiviert ist, wird eine Anforderung von einer Anwendung, die exklusive Kontrolle über das Gerät zu nehmen, erfolgreich ausgeführt, wenn das Gerät derzeit nicht verwendet wird, oder wenn das Gerät im Modus für gemeinsame Nutzung verwendet wird, aber die Anforderung schlägt fehl, wenn eine andere Anwendung bereits über eine exklusive Kontrolle über das Gerät verfügt. Wenn die vorab Entfernung deaktiviert ist, wird eine Anforderung von einer Anwendung, die exklusive Kontrolle über das Gerät zu nehmen, erfolgreich ausgeführt, wenn das Gerät derzeit nicht verwendet wird, aber die Anforderung schlägt fehl, wenn das Gerät bereits im freigegebenen Modus oder im exklusiven Modus verwendet wird.

In Windows Vista lauten die Standardeinstellungen für ein audioendpunktgerät wie folgt:

-   Das Gerät kann verwendet werden, um Streams im exklusiven Modus wiederzugeben oder aufzuzeichnen.
-   Eine Anforderung zur Verwendung eines Geräts zum Wiedergeben oder Aufzeichnen eines Streams im exklusiven Modus weist jeden Datenstrom im freigegebenen Modus an, der gerade wiedergegeben oder über das Gerät aufgezeichnet wird.

**So ändern Sie die Einstellungen für den exklusiven Modus eines Wiedergabe-oder Aufzeichnungs Geräts**

1.  Klicken Sie mit der rechten Maustaste auf das Redner Symbol im Benachrichtigungsbereich, das sich auf der rechten Seite der Taskleiste befindet, und wählen Sie **Geräte wieder** geben oder **Geräte aufzeichnen** aus. (Alternativ können Sie die Windows-Multimedia-Systemsteuerung Mmsys.cpl in einem Eingabe Aufforderungs Fenster ausführen. Weitere Informationen finden Sie unter Hinweise in [Geräte \_ Status \_ xxx-Konstanten](device-state-xxx-constants.md).)
2.  Nachdem das **Sound** Fenster angezeigt wird, wählen Sie **Wiedergabe** oder **Aufzeichnung** aus. Wählen Sie als nächstes einen Eintrag in der Liste der Gerätenamen aus, und klicken Sie auf **Eigenschaften**.
3.  Nachdem das Fenster **Eigenschaften** angezeigt wird, klicken Sie auf **erweitert**.
4.  Aktivieren Sie das Kontrollkästchen **Anwendungen das ausschließliche Steuern dieses Geräts gestatten**, damit Anwendungen das Gerät im exklusiven Modus verwenden können. Deaktivieren Sie das Kontrollkästchen, um die Verwendung des Geräts im exklusiven Modus zu deaktivieren.
5.  Wenn die Verwendung des Geräts im exklusiven Modus aktiviert ist, können Sie angeben, ob eine Anforderung für die exklusive Kontrolle des Geräts erfolgreich ist, wenn das Gerät gerade wieder verwendet wird oder Datenströme im freigegebenen Modus aufzeichnen. Wenn Sie Anwendungen im exklusiven Modus Vorrang vor Anwendungen im freigegebenen Modus einräumen möchten, aktivieren Sie das Kontrollkästchen mit der Bezeichnung **Anwendungs Priorität im exklusiven Modus vergeben**. Deaktivieren Sie das Kontrollkästchen, um Anwendungen im exklusiven Modus Vorrang vor Anwendungen im Modus für freigegebene Anwendungen zu verweigern.

Im folgenden Codebeispiel wird gezeigt, wie Sie einen Audiostream mit niedriger Latenz auf einem audiorenderinggerät wiedergeben, das für die Verwendung im exklusiven Modus konfiguriert ist:


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
    DWORD taskIndex = 0;
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



Im vorangehenden Codebeispiel wird die playexclusivestream-Funktion im Anwendungs Thread ausgeführt, der die Endpunkt Puffer beim Abspielen eines renderingstreams Dienste ausführt. Die Funktion nimmt den einzelnen Parameter pmysource an, der ein Zeiger auf ein Objekt ist, das zu einer Client definierten Klasse myaudiosource gehört. Diese Klasse verfügt über zwei Member-Funktionen, LoadData und SetFormat, die im Codebeispiel aufgerufen werden. Myaudiosource wird unter [Rendern eines Streams](rendering-a-stream.md)beschrieben.

Die playexclusivestream-Funktion Ruft die Hilfsfunktion getstreamformat auf, die mit dem standardmäßigen renderinggerät aushandiert, um zu bestimmen, ob das Gerät ein Streamformat im exklusiven Modus unterstützt, das für die Verwendung durch die Anwendung geeignet ist. Der Code für die getstreamformat-Funktion wird nicht im Codebeispiel angezeigt. Dies liegt daran, dass die Details der Implementierung vollständig von den Anforderungen der Anwendung abhängen. Der Vorgang der getstreamformat-Funktion kann jedoch einfach beschrieben werden – Sie ruft die [**iaudioclient:: isformatsupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) -Methode einmal oder mehrmals auf, um zu bestimmen, ob das Gerät ein geeignetes Format unterstützt. Die Anforderungen der Anwendung legen fest, welche Formate getstreamformat für die **isformatsupported** -Methode und die Reihenfolge darstellt, in der Sie präsentiert werden. Weitere Informationen zu **isformatsupported** finden Sie unter [Geräte Formate](device-formats.md).

Nach dem Aufruf getstreamformat Ruft die playexclusivestream-Funktion die [**iaudioclient:: getdeviceperiod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) -Methode auf, um den minimalen von der Audiohardware unterstützten Geräte Zeitraum zu erhalten. Als nächstes Ruft die-Funktion die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf, um eine Puffer Dauer anzufordern, die dem minimalen Zeitraum entspricht. Wenn der-Vorgang erfolgreich ausgeführt wird, ordnet die **Initialize** -Methode zwei Endpunkt Puffer zu, von denen jeder gleich dem Mindestzeitraum ist. Wenn der Audiostream zu einem späteren Zeitpunkt ausgeführt wird, werden die beiden Puffer von der Anwendungs-und Audiohardware in der "Ping-Pong"-Weise gemeinsam genutzt – das heißt, während die Anwendung in einen Puffer schreibt, liest die Hardware aus dem anderen Puffer.

Vor dem Starten des Streams führt die playexclusivestream-Funktion folgende Aktionen aus:

-   Erstellt und registriert das Ereignis handle, über das es Benachrichtigungen empfängt, wenn Puffer bereit zum Auffüllen werden.
-   Füllt den ersten Puffer mit Daten aus der Audioquelle aus, um die Verzögerung zu verringern, wenn der Stream mit der Ausführung beginnt, wenn der ursprüngliche Sound gehört.
-   Ruft die **avsetmmthreadcharacteristics** -Funktion auf, um anzufordern, dass MMCSS die Priorität des Threads erhöht, in dem playexclusivestream ausgeführt wird. (Wenn der Stream nicht mehr ausgeführt wird, stellt der **avrevertmmthreadcharacteristics** -Funktionsaufrufe die ursprüngliche Thread Priorität wieder her.)

Weitere Informationen zu **avsetmmthreadcharacteristics** und **avrevertmmthreadcharacteristics** finden Sie in der Windows SDK-Dokumentation.

Während der Stream ausgeführt wird, füllt jede Iterationen der **while**-Schleife im vorangehenden Codebeispiel einen Endpunkt Puffer aus. Zwischen Iterationen wartet der **WaitForSingleObject** -Funktions Aufrufpunkt darauf, dass das Ereignis Handle signalisiert wird. Wenn das Handle signalisiert wird, führt der Schleifen Text Folgendes aus:

1.  Ruft die [**iaudiorenderclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Methode auf, um den nächsten Puffer zu erhalten.
2.  Füllt den Puffer.
3.  Ruft die [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode auf, um den Puffer freizugeben.

Weitere Informationen zu **WaitForSingleObject** finden Sie in der Windows SDK-Dokumentation.

Wenn der Audioadapter von einem WaveRT-Treiber gesteuert wird, ist die Signalisierung des Ereignis Handles an die DMA-Transfer-Benachrichtigungen von der Audiohardware gebunden. Bei einem USB-Audiogerät oder bei einem Audiogerät, das von einem wavecyclic-oder wavepci-Treiber gesteuert wird, ist die Signalisierung des Ereignis Handles an die Vervollständigung der Datenpunkte gebunden, die Daten aus dem Anwendungs Puffer an den Hardware Puffer übertragen.

Im vorangehenden Codebeispiel werden die Audiohardware und das Computersystem auf ihre Leistungs Limits übertragen. Um die Datenstrom Latenz zu verringern, plant die Anwendung zunächst, den Puffer Wartungs Thread für die Verwendung des minimalen Geräte Zeitraums zu verwenden, der von der Audiohardware unterstützt wird. Um sicherzustellen, dass der Thread zuverlässig innerhalb jedes Geräte Zeitraums ausgeführt wird, legt der **avsetmmthreadcharacteristics** -Funktionsname den Taskname-Parameter auf "pro-Audiodatei" (in Windows Vista) auf den Standardaufgaben Namen mit der höchsten Priorität fest. Stellen Sie sich vor, ob die zeitlichen Anforderungen Ihrer Anwendung gelockert werden können, ohne dass deren Nützlichkeit beeinträchtigt wird. Die Anwendung kann z. b. den Puffer Wartungs Thread so planen, dass er einen Zeitraum verwendet, der länger als der minimale Wert ist. Ein längerer Zeitraum kann die Verwendung einer niedrigeren Thread Priorität sicher erlauben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> </dl>

 

 



