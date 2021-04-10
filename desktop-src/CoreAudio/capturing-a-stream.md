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
# <a name="capturing-a-stream"></a><span data-ttu-id="26fb9-103">Erfassen eines Streams</span><span class="sxs-lookup"><span data-stu-id="26fb9-103">Capturing a Stream</span></span>

<span data-ttu-id="26fb9-104">Der Client ruft die Methoden in der [**iaudiocaptureclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) -Schnittstelle auf, um erfasste Daten aus einem Endpunkt Puffer zu lesen.</span><span class="sxs-lookup"><span data-stu-id="26fb9-104">The client calls the methods in the [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface to read captured data from an endpoint buffer.</span></span> <span data-ttu-id="26fb9-105">Der Client verwendet den Endpunkt Puffer mit dem Audiomodul im freigegebenen Modus und mit dem Audiogerät im exklusiven Modus.</span><span class="sxs-lookup"><span data-stu-id="26fb9-105">The client shares the endpoint buffer with the audio engine in shared mode and with the audio device in exclusive mode.</span></span> <span data-ttu-id="26fb9-106">Um einen Endpunkt Puffer einer bestimmten Größe anzufordern, ruft der Client die [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="26fb9-106">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="26fb9-107">Um die Größe des zugeordneten Puffers zu erhalten, der sich von der angeforderten Größe unterscheiden kann, ruft der Client die [**iaudioclient:: getBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="26fb9-107">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="26fb9-108">Um einen Stream erfasster Daten über den Endpunkt Puffer zu verschieben, ruft der Client alternativ die [**iaudiocaptureclient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) -Methode und die [**iaudiocaptureclient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="26fb9-108">To move a stream of captured data through the endpoint buffer, the client alternately calls the [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) method and the [**IAudioCaptureClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) method.</span></span> <span data-ttu-id="26fb9-109">Der Client greift als eine Reihe von Datenpaketen auf die Daten im Endpunkt Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="26fb9-109">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="26fb9-110">Der **GetBuffer** -Befehl ruft das nächste Paket der aufgezeichneten Daten aus dem Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="26fb9-110">The **GetBuffer** call retrieves the next packet of captured data from the buffer.</span></span> <span data-ttu-id="26fb9-111">Nachdem die Daten aus dem Paket gelesen wurden, ruft der Client **ReleaseBuffer** auf, um das Paket freizugeben und für mehr erfasste Daten verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="26fb9-111">After reading the data from the packet, the client calls **ReleaseBuffer** to release the packet and make it available for more captured data.</span></span>

<span data-ttu-id="26fb9-112">Die Paketgröße kann von einem [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) -aufrufen zum nächsten abweichen.</span><span class="sxs-lookup"><span data-stu-id="26fb9-112">The packet size can vary from one [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) call to the next.</span></span> <span data-ttu-id="26fb9-113">Vor dem Aufrufen von **GetBuffer** hat der Client die Möglichkeit, die [**iaudiocaptureclient:: getnextpacketsize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) -Methode aufrufen, um die Größe des nächsten Pakets im Voraus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="26fb9-113">Before calling **GetBuffer**, the client has the option of calling the [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) method to get the size of the next packet in advance.</span></span> <span data-ttu-id="26fb9-114">Außerdem kann der Client die [**iaudioclient:: getcurrentpadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) -Methode aufrufen, um die Gesamtmenge der aufgezeichneten Daten zu erhalten, die im Puffer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="26fb9-114">In addition, the client can call the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method to get the total amount of captured data that is available in the buffer.</span></span> <span data-ttu-id="26fb9-115">Die Paketgröße ist immer kleiner oder gleich der Gesamtmenge der aufgezeichneten Daten im Puffer.</span><span class="sxs-lookup"><span data-stu-id="26fb9-115">At any instant, the packet size is always less than or equal to the total amount of captured data in the buffer.</span></span>

<span data-ttu-id="26fb9-116">Bei jedem Verarbeitungs Durchlauf hat der Client die Möglichkeit, die erfassten Daten auf eine der folgenden Arten zu verarbeiten:</span><span class="sxs-lookup"><span data-stu-id="26fb9-116">During each processing pass, the client has the option of processing the captured data in one of the following ways:</span></span>

-   <span data-ttu-id="26fb9-117">Der Client ruft alternativ [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) und [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)auf, wobei ein Paket mit jedem Paar von Aufrufen gelesen wird, bis **GetBuffer** den Wert von audcnt \_ S \_ bufferempty zurückgibt, wodurch angegeben wird, dass der Puffer leer ist.</span><span class="sxs-lookup"><span data-stu-id="26fb9-117">The client alternately calls [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), reading one packet with each pair of calls, until **GetBuffer** returns AUDCNT\_S\_BUFFEREMPTY, indicating that the buffer is empty.</span></span>
-   <span data-ttu-id="26fb9-118">Der Client ruft [**getnextpacketsize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) vor jedem Paar von Aufrufen von [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) und [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) auf, bis **getnextpacketsize** eine Paketgröße von 0 meldet, was angibt, dass der Puffer leer ist.</span><span class="sxs-lookup"><span data-stu-id="26fb9-118">The client calls [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) before each pair of calls to [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) until **GetNextPacketSize** reports a packet size of 0, indicating that the buffer is empty.</span></span>

<span data-ttu-id="26fb9-119">Die beiden Techniken liefern gleichwertige Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="26fb9-119">The two techniques yield equivalent results.</span></span>

<span data-ttu-id="26fb9-120">Das folgende Codebeispiel zeigt, wie Sie einen Audiostream vom Standard Erfassungsgerät aufzeichnen:</span><span class="sxs-lookup"><span data-stu-id="26fb9-120">The following code example shows how to record an audio stream from the default capture device:</span></span>


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



<span data-ttu-id="26fb9-121">Im vorangehenden Beispiel nimmt die Funktion recordaudiostream den einzelnen Parameter, `pMySink` , ein Zeiger auf ein Objekt, das zu einer Client definierten Klasse, myaudiosink, mit zwei Funktionen (CopyData und SetFormat) gehört.</span><span class="sxs-lookup"><span data-stu-id="26fb9-121">In the preceding example, the RecordAudioStream function takes a single parameter, `pMySink`, which is a pointer to an object that belongs to a client-defined class, MyAudioSink, with two functions, CopyData and SetFormat.</span></span> <span data-ttu-id="26fb9-122">Der Beispielcode enthält nicht die Implementierung von myaudiosink:</span><span class="sxs-lookup"><span data-stu-id="26fb9-122">The example code does not include the implementation of MyAudioSink because:</span></span>

-   <span data-ttu-id="26fb9-123">Keines der Klassenmember kommuniziert direkt mit einer der Methoden in den Schnittstellen in WASAPI.</span><span class="sxs-lookup"><span data-stu-id="26fb9-123">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="26fb9-124">Die Klasse kann auf verschiedene Weise implementiert werden, je nach den Anforderungen des Clients.</span><span class="sxs-lookup"><span data-stu-id="26fb9-124">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="26fb9-125">(Beispielsweise können die Erfassungsdaten in eine WAV-Datei geschrieben werden.)</span><span class="sxs-lookup"><span data-stu-id="26fb9-125">(For example, it might write the capture data to a WAV file.)</span></span>

<span data-ttu-id="26fb9-126">Informationen zum Vorgang der beiden Methoden sind jedoch nützlich, um das Beispiel zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="26fb9-126">However, information about the operation of the two methods is useful for understanding the example.</span></span>

<span data-ttu-id="26fb9-127">Die CopyData-Funktion kopiert eine angegebene Anzahl von Audioframes von einem angegebenen Puffer Speicherort.</span><span class="sxs-lookup"><span data-stu-id="26fb9-127">The CopyData function copies a specified number of audio frames from a specified buffer location.</span></span> <span data-ttu-id="26fb9-128">Die Funktion "recordaudiostream" verwendet die CopyData-Funktion, um die Audiodaten aus dem freigegebenen Puffer zu lesen und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="26fb9-128">The RecordAudioStream function uses the CopyData function to read and save the audio data from the shared buffer.</span></span> <span data-ttu-id="26fb9-129">Die Funktion SetFormat gibt das Format für die CopyData-Funktion an, die für die Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26fb9-129">The SetFormat function specifies the format for the CopyData function to use for the data.</span></span>

<span data-ttu-id="26fb9-130">Solange das myaudiosink-Objekt zusätzliche Daten erfordert, gibt die CopyData-Funktion den Wert **false** über den dritten Parameter aus, der im vorangehenden Codebeispiel ein Zeiger auf die Variable ist `bDone` .</span><span class="sxs-lookup"><span data-stu-id="26fb9-130">As long as the MyAudioSink object requires additional data, the CopyData function outputs the value **FALSE** through its third parameter, which, in the preceding code example, is a pointer to the variable `bDone`.</span></span> <span data-ttu-id="26fb9-131">Wenn das myaudiosink-Objekt über alle Daten verfügt, die es erfordert, legt die CopyData-Funktion `bDone` auf **true** fest. Dies bewirkt, dass das Programm die Schleife in der recordaudiostream-Funktion verlässt.</span><span class="sxs-lookup"><span data-stu-id="26fb9-131">When the MyAudioSink object has all the data that it requires, the CopyData function sets `bDone` to **TRUE**, which causes the program to exit the loop in the RecordAudioStream function.</span></span>

<span data-ttu-id="26fb9-132">Die Funktion recordaudiostream weist einen freigegebenen Puffer mit einer Dauer von einer Sekunde zu.</span><span class="sxs-lookup"><span data-stu-id="26fb9-132">The RecordAudioStream function allocates a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="26fb9-133">(Der zugewiesene Puffer kann etwas länger dauern.) Innerhalb der Hauptschleife bewirkt der Aufrufe der Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) -Funktion, dass das Programm eine halbe Sekunde wartet.</span><span class="sxs-lookup"><span data-stu-id="26fb9-133">(The allocated buffer might have a slightly longer duration.) Within the main loop, the call to the Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) function causes the program to wait for a half second.</span></span> <span data-ttu-id="26fb9-134">Zu **Beginn jedes Ruhe** Zustands ist der freigegebene Puffer leer oder fast leer.</span><span class="sxs-lookup"><span data-stu-id="26fb9-134">At the start of each **Sleep** call, the shared buffer is empty or nearly empty.</span></span> <span data-ttu-id="26fb9-135">Wenn der Standby- **Aufruf zurück** kehrt, ist der freigegebene Puffer ungefähr die Hälfte der erfassten Daten.</span><span class="sxs-lookup"><span data-stu-id="26fb9-135">By the time the **Sleep** call returns, the shared buffer is about half filled with capture data.</span></span>

<span data-ttu-id="26fb9-136">Nach dem Aufrufen der [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) -Methode bleibt der Stream geöffnet, bis der Client alle Verweise auf die [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Schnittstelle und alle Verweise auf Dienst Schnittstellen freigibt, die vom Client über die [**iaudioclient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) -Methode abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="26fb9-136">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="26fb9-137">Der endgültige [**releaseaufrufad**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) schließt den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="26fb9-137">The final [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26fb9-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26fb9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26fb9-139">Datenstrom Verwaltung</span><span class="sxs-lookup"><span data-stu-id="26fb9-139">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
