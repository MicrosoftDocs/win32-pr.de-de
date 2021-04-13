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
# <a name="rendering-a-stream"></a><span data-ttu-id="feca3-103">Rendern eines Streams</span><span class="sxs-lookup"><span data-stu-id="feca3-103">Rendering a Stream</span></span>

<span data-ttu-id="feca3-104">Der Client ruft die Methoden in der [**iaudiorenderclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) -Schnittstelle auf, um Renderingdaten in einen Endpunkt Puffer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="feca3-104">The client calls the methods in the [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) interface to write rendering data to an endpoint buffer.</span></span> <span data-ttu-id="feca3-105">Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.</span><span class="sxs-lookup"><span data-stu-id="feca3-105">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span> <span data-ttu-id="feca3-106">Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.</span><span class="sxs-lookup"><span data-stu-id="feca3-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span> <span data-ttu-id="feca3-107">Um einen Endpunkt Puffer einer bestimmten Größe anzufordern, ruft der Client die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="feca3-107">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="feca3-108">Um die Größe des zugeordneten Puffers zu erhalten, der sich von der angeforderten Größe unterscheiden kann, ruft der Client die [**iaudioclient:: getBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="feca3-108">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="feca3-109">Um einen Stream von Renderingdaten über den Endpunkt Puffer zu verschieben, ruft der Client alternativ die [**iaudiorenderclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Methode und die [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="feca3-109">To move a stream of rendering data through the endpoint buffer, the client alternately calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method and the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method.</span></span> <span data-ttu-id="feca3-110">Der Client greift als eine Reihe von Datenpaketen auf die Daten im Endpunkt Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="feca3-110">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="feca3-111">Der **GetBuffer** -Befehl ruft das nächste Paket ab, sodass der Client es mit Renderingdaten auffüllen kann.</span><span class="sxs-lookup"><span data-stu-id="feca3-111">The **GetBuffer** call retrieves the next packet so that the client can fill it with rendering data.</span></span> <span data-ttu-id="feca3-112">Nachdem die Daten in das Paket geschrieben wurden, ruft der Client **ReleaseBuffer** auf, um das fertige Paket der renderinganschlange hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="feca3-112">After writing the data to the packet, the client calls **ReleaseBuffer** to add the completed packet to the rendering queue.</span></span>

<span data-ttu-id="feca3-113">Bei einem renderingpuffer stellt der von der [**iaudioclient:: getcurrentpadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) -Methode gemeldete Auffüll Wert die Menge der Renderingdaten dar, die in die Warteschlange eingereiht werden, um im Puffer wiedergegeben zu werden.</span><span class="sxs-lookup"><span data-stu-id="feca3-113">For a rendering buffer, the padding value that is reported by the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method represents the amount of rendering data that is queued up to play in the buffer.</span></span> <span data-ttu-id="feca3-114">Eine renderinganwendung kann den Füll Wert verwenden, um zu bestimmen, wie viele neue Daten sicher in den Puffer geschrieben werden können, ohne dass zuvor geschriebene Daten überschrieben werden müssen, die von der Audioengine noch nicht aus dem Puffer gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="feca3-114">A rendering application can use the padding value to determine how much new data it can safely write to the buffer without the risk of overwriting previously written data that the audio engine has not yet read from the buffer.</span></span> <span data-ttu-id="feca3-115">Der verfügbare Speicherplatz ist einfach die Puffergröße abzüglich der Auffüll Größe.</span><span class="sxs-lookup"><span data-stu-id="feca3-115">The available space is simply the buffer size minus the padding size.</span></span> <span data-ttu-id="feca3-116">Der Client kann eine Paketgröße anfordern, die einen Teil oder den gesamten verfügbaren Speicherplatz im nächsten [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Befehl darstellt.</span><span class="sxs-lookup"><span data-stu-id="feca3-116">The client can request a packet size that represents some or all of this available space in its next [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) call.</span></span>

<span data-ttu-id="feca3-117">Die Größe eines Pakets wird in *Audioframes* ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="feca3-117">The size of a packet is expressed in *audio frames*.</span></span> <span data-ttu-id="feca3-118">Ein audioframe in einem PCM-Stream besteht aus einem Satz von Stichproben (der Satz enthält ein Beispiel für jeden Kanal im Stream), die wiedergegeben werden oder gleichzeitig aufgezeichnet werden (Takt Takt).</span><span class="sxs-lookup"><span data-stu-id="feca3-118">An audio frame in a PCM stream is a set of samples (the set contains one sample for each channel in the stream) that play or are recorded at the same time (clock tick).</span></span> <span data-ttu-id="feca3-119">Daher ist die Größe eines Audioframes die Stichprobengröße multipliziert mit der Anzahl der Kanäle im Stream.</span><span class="sxs-lookup"><span data-stu-id="feca3-119">Thus, the size of an audio frame is the sample size multiplied by the number of channels in the stream.</span></span> <span data-ttu-id="feca3-120">Beispielsweise beträgt die Frame Größe für einen Stereo-Stream (2-Kanal) mit 16-Bit-Stichproben vier Bytes.</span><span class="sxs-lookup"><span data-stu-id="feca3-120">For example, the frame size for a stereo (2-channel) stream with 16-bit samples is four bytes.</span></span>

<span data-ttu-id="feca3-121">Im folgenden Codebeispiel wird gezeigt, wie Sie einen Audiostream auf dem standardmäßigen renderinggerät wiedergeben:</span><span class="sxs-lookup"><span data-stu-id="feca3-121">The following code example shows how to play an audio stream on the default rendering device:</span></span>


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



<span data-ttu-id="feca3-122">Im vorangehenden Beispiel nimmt die Funktion playaudiostream den einzelnen Parameter, `pMySource` , ein Zeiger auf ein Objekt, das zu einer Client definierten Klasse, myaudiosource, mit zwei Element Funktionen (LoadData und SetFormat) gehört.</span><span class="sxs-lookup"><span data-stu-id="feca3-122">In the preceding example, the PlayAudioStream function takes a single parameter, `pMySource`, which is a pointer to an object that belongs to a client-defined class, MyAudioSource, with two member functions, LoadData and SetFormat.</span></span> <span data-ttu-id="feca3-123">Der Beispielcode enthält nicht die Implementierung von myaudiosource aus folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="feca3-123">The example code does not include the implementation of MyAudioSource because:</span></span>

-   <span data-ttu-id="feca3-124">Keines der Klassenmember kommuniziert direkt mit einer der Methoden in den Schnittstellen in WASAPI.</span><span class="sxs-lookup"><span data-stu-id="feca3-124">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="feca3-125">Die Klasse kann auf verschiedene Weise implementiert werden, je nach den Anforderungen des Clients.</span><span class="sxs-lookup"><span data-stu-id="feca3-125">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="feca3-126">(Beispielsweise können die Renderingdaten aus einer WAV-Datei gelesen und eine dynamische Konvertierung in das Streamformat durchgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="feca3-126">(For example, it might read the rendering data from a WAV file and perform on-the-fly conversion to the stream format.)</span></span>

<span data-ttu-id="feca3-127">Einige Informationen über den Betrieb der beiden Funktionen sind jedoch nützlich, um das Beispiel zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="feca3-127">However, some information about the operation of the two functions is useful for understanding the example.</span></span>

<span data-ttu-id="feca3-128">Die LoadData-Funktion schreibt eine angegebene Anzahl von Audioframes (erster Parameter) in einen angegebenen Puffer Speicherort (zweiter Parameter).</span><span class="sxs-lookup"><span data-stu-id="feca3-128">The LoadData function writes a specified number of audio frames (first parameter) to a specified buffer location (second parameter).</span></span> <span data-ttu-id="feca3-129">(Bei der Größe eines Audioframes handelt es sich um die Anzahl der Kanäle im Stream multipliziert mit der Stichprobengröße.) Die playaudiostream-Funktion verwendet LoadData, um Teile des freigegebenen Puffers mit Audiodaten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="feca3-129">(The size of an audio frame is the number of channels in the stream multiplied by the sample size.) The PlayAudioStream function uses LoadData to fill portions of the shared buffer with audio data.</span></span> <span data-ttu-id="feca3-130">Die SetFormat-Funktion gibt das Format für die LoadData-Funktion an, die für die Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="feca3-130">The SetFormat function specifies the format for the LoadData function to use for the data.</span></span> <span data-ttu-id="feca3-131">Wenn die LoadData-Funktion in der Lage ist, mindestens einen Frame in den angegebenen Puffer Speicherort zu schreiben, ohne die angegebene Anzahl von Frames zu schreiben, wird die Ruhe in die restlichen Frames geschrieben.</span><span class="sxs-lookup"><span data-stu-id="feca3-131">If the LoadData function is able to write at least one frame to the specified buffer location but runs out of data before it has written the specified number of frames, then it writes silence to the remaining frames.</span></span>

<span data-ttu-id="feca3-132">Solange LoadData das Schreiben von mindestens einem Frame mit echten Daten (nicht Stille) an den angegebenen Puffer Speicherort erfolgreich durchläuft, wird 0 über den dritten Parameter ausgegeben, der im vorangehenden Codebeispiel ein Ausgabe Zeiger auf die Variable ist `flags` .</span><span class="sxs-lookup"><span data-stu-id="feca3-132">As long as LoadData succeeds in writing at least one frame of real data (not silence) to the specified buffer location, it outputs 0 through its third parameter, which, in the preceding code example, is an output pointer to the `flags` variable.</span></span> <span data-ttu-id="feca3-133">Wenn LoadData nicht über Daten verfügt und auch keinen einzelnen Frame in den angegebenen Puffer Speicherort schreiben kann, schreibt er nichts in den Puffer (nicht einmal) und schreibt den Wert von "audclnt \_ bufferflags" \_ in die `flags` Variable.</span><span class="sxs-lookup"><span data-stu-id="feca3-133">When LoadData is out of data and cannot write even a single frame to the specified buffer location, it writes nothing to the buffer (not even silence), and it writes the value AUDCLNT\_BUFFERFLAGS\_SILENT to the `flags` variable.</span></span> <span data-ttu-id="feca3-134">Die- `flags` Variable überträgt diesen Wert an die [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode, die antwortet, indem Sie die angegebene Anzahl von Frames im Puffer mit Ruhe füllt.</span><span class="sxs-lookup"><span data-stu-id="feca3-134">The `flags` variable conveys this value to the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method, which responds by filling the specified number of frames in the buffer with silence.</span></span>

<span data-ttu-id="feca3-135">Beim Abrufen der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode fordert die playaudiostream-Funktion im vorangehenden Beispiel einen freigegebenen Puffer an, der eine Sekunde Dauer von einer Sekunde hat.</span><span class="sxs-lookup"><span data-stu-id="feca3-135">In its call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the PlayAudioStream function in the preceding example requests a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="feca3-136">(Der zugewiesene Puffer kann etwas länger dauern.) Bei den ersten Aufrufen der [**iaudiorenderclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) -Methode und der [**iaudiorenderclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) -Methode füllt die Funktion den gesamten Puffer aus, bevor die [**iaudioclient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) -Methode aufgerufen wird, um die Wiedergabe des Puffers zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="feca3-136">(The allocated buffer might have a slightly longer duration.) In its initial calls to the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) and [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) methods, the function fills the entire buffer before calling the [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) method to begin playing the buffer.</span></span>

<span data-ttu-id="feca3-137">Innerhalb der Hauptschleife füllt die Funktion die Hälfte des Puffers in Intervallen von halb Sekunden iterativ auf.</span><span class="sxs-lookup"><span data-stu-id="feca3-137">Within the main loop, the function iteratively fills half of the buffer at half-second intervals.</span></span> <span data-ttu-id="feca3-138">Unmittelbar vor jedem Aufrufe der Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) -Funktion in der Hauptschleife ist der Puffer voll oder fast voll.</span><span class="sxs-lookup"><span data-stu-id="feca3-138">Just before each call to the Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function in the main loop, the buffer is full or nearly full.</span></span> <span data-ttu-id="feca3-139">Wenn der Standby-Rückruf zurückgegeben wird, **ist der Puffer** ungefähr halb voll.</span><span class="sxs-lookup"><span data-stu-id="feca3-139">When the **Sleep** call returns, the buffer is about half full.</span></span> <span data-ttu-id="feca3-140">Die Schleife wird beendet, nachdem der letzte-Befehl der LoadData-Funktion die- `flags` Variable auf den Wert "audclnt \_ bufferflags Silent" festgelegt hat \_ .</span><span class="sxs-lookup"><span data-stu-id="feca3-140">The loop ends after the final call to the LoadData function sets the `flags` variable to the value AUDCLNT\_BUFFERFLAGS\_SILENT.</span></span> <span data-ttu-id="feca3-141">Zu diesem Zeitpunkt enthält der Puffer mindestens einen Frame mit echten Daten und kann so viel wie eine halbe Sekunde an echten Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="feca3-141">At that point, the buffer contains at least one frame of real data, and it might contain as much as a half second of real data.</span></span> <span data-ttu-id="feca3-142">Der Rest des Puffers enthält Ruhe.</span><span class="sxs-lookup"><span data-stu-id="feca3-142">The remainder of the buffer contains silence.</span></span> <span data-ttu-id="feca3-143">Der Standby **-Aufruf, der auf** die Schleife folgt, bietet ausreichend Zeit (eine halbe Sekunde), um alle verbleibenden Daten wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="feca3-143">The **Sleep** call that follows the loop provides sufficient time (a half second) to play all of the remaining data.</span></span> <span data-ttu-id="feca3-144">Die Stille, die auf die Daten folgt, verhindert unerwünschte Sounds, bevor der Aufrufe der [**iaudioclient:: Stopp**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) -Methode den Audiodatenstrom stoppt.</span><span class="sxs-lookup"><span data-stu-id="feca3-144">The silence that follows the data prevents unwanted sounds before the call to the [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) method stops the audio stream.</span></span> <span data-ttu-id="feca3-145">Weitere **Informationen zum** Standbymodus finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="feca3-145">For more information about **Sleep**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="feca3-146">Nach dem Aufrufen der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode bleibt der Stream geöffnet, bis der Client alle Verweise auf die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle und alle Verweise auf Dienst Schnittstellen freigibt, die vom Client über die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="feca3-146">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="feca3-147">Der endgültige [**releaseaufrufad**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) schließt den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="feca3-147">The final [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

<span data-ttu-id="feca3-148">Die Funktion playaudiostream im vorangehenden Codebeispiel ruft die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf, um einen Enumerator für die audioendpunktgeräte im System zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="feca3-148">The PlayAudioStream function in the preceding code example calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="feca3-149">Wenn das aufrufende Programm die **CoCreateInstance** -Funktion oder die [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion nicht zum Initialisieren der com-Bibliothek aufgerufen hat, tritt beim **CoCreateInstance** -Aufruf ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="feca3-149">Unless the calling program previously called either the **CoCreateInstance** or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="feca3-150">Weitere Informationen zu **cokreateinstance**, **cokreateinstance** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="feca3-150">For more information about **CoCreateInstance**, **CoCreateInstance**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="feca3-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="feca3-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feca3-152">Datenstrom Verwaltung</span><span class="sxs-lookup"><span data-stu-id="feca3-152">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
