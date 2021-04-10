---
description: In diesem Thema wird beschrieben, wie der Quell Leser im asynchronen Modus verwendet wird.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Verwenden des Quell Readers im asynchronen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041899"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a><span data-ttu-id="78d05-103">Verwenden des Quell Readers im asynchronen Modus</span><span class="sxs-lookup"><span data-stu-id="78d05-103">Using the Source Reader in Asynchronous Mode</span></span>

<span data-ttu-id="78d05-104">In diesem Thema wird beschrieben, wie der [Quell Leser](source-reader.md) im asynchronen Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78d05-104">This topic describes how to use the [Source Reader](source-reader.md) in asynchronous mode.</span></span> <span data-ttu-id="78d05-105">Im asynchronen Modus stellt die Anwendung eine Rückruf Schnittstelle bereit, die verwendet wird, um die Anwendung darüber zu benachrichtigen, dass Daten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="78d05-105">In asynchronous mode, the application provides a callback interface, which is used to notify the application that data is available.</span></span>

<span data-ttu-id="78d05-106">In diesem Thema wird davon ausgegangen, dass Sie das Thema [zum Verarbeiten von Mediendaten mithilfe des Quell Lesers](processing-media-data-with-the-source-reader.md)bereits gelesen haben.</span><span class="sxs-lookup"><span data-stu-id="78d05-106">This topic assumes that you have already read the topic [Using the Source Reader to Process Media Data](processing-media-data-with-the-source-reader.md).</span></span>

## <a name="using-asynchronous-mode"></a><span data-ttu-id="78d05-107">Verwenden des asynchronen Modus</span><span class="sxs-lookup"><span data-stu-id="78d05-107">Using Asynchronous Mode</span></span>

<span data-ttu-id="78d05-108">Der Quell Reader funktioniert entweder im synchronen oder asynchronen Modus.</span><span class="sxs-lookup"><span data-stu-id="78d05-108">The Source Reader operates either in synchronous mode or asynchronous mode.</span></span> <span data-ttu-id="78d05-109">Im Codebeispiel im vorherigen Abschnitt wird davon ausgegangen, dass der Quell Leser den synchronen Modus verwendet. Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="78d05-109">The code example shown in the previous section assumes that the Source Reader is using synchronous mode, which is the default.</span></span> <span data-ttu-id="78d05-110">Im synchronen Modus wird die [**IMF sourcereader:: lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) -Methode blockiert, während die Medienquelle das nächste Beispiel erzeugt.</span><span class="sxs-lookup"><span data-stu-id="78d05-110">In synchronous mode, the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method blocks while the media source produces the next sample.</span></span> <span data-ttu-id="78d05-111">Eine Medienquelle ruft in der Regel Daten aus einer externen Quelle (z. b. einer lokalen Datei oder einer Netzwerkverbindung) ab, sodass die Methode den aufrufenden Thread für eine merkliche Zeit blockieren kann.</span><span class="sxs-lookup"><span data-stu-id="78d05-111">A media source typically acquires data from some external source (such as a local file or a network connection), so the method can block the calling thread for a noticeable amount of time.</span></span>

<span data-ttu-id="78d05-112">Im asynchronen Modus gibt das "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " sofort zurück, und die Arbeit wird in einem anderen Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78d05-112">In asynchronous mode, the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) returns immediately and the work is performed on another thread.</span></span> <span data-ttu-id="78d05-113">Nachdem der Vorgang beendet wurde, ruft der Quell Leser die Anwendung über die [**IMF sourcereadercallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) -Rückruf Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="78d05-113">After the operation is complete, the Source Reader calls the application through the [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) callback interface.</span></span> <span data-ttu-id="78d05-114">Um den asynchronen Modus zu verwenden, müssen Sie beim ersten Erstellen des Quell Readers wie folgt einen Rückruf Zeiger bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="78d05-114">To use asynchronous mode, you must provide a callback pointer when you first create the Source Reader, as follows:</span></span>

1.  <span data-ttu-id="78d05-115">Erstellen Sie einen Attribut Speicher, indem Sie die [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="78d05-115">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
2.  <span data-ttu-id="78d05-116">Legen Sie [das \_ \_ \_ Async- \_ Rückruf Attribut des MF-Quell Readers](mf-source-reader-async-callback.md) für den Attribut Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="78d05-116">Set the [MF\_SOURCE\_READER\_ASYNC\_CALLBACK](mf-source-reader-async-callback.md) attribute on the attribute store.</span></span> <span data-ttu-id="78d05-117">Der Attribut Wert ist ein Zeiger auf das Rückruf Objekt.</span><span class="sxs-lookup"><span data-stu-id="78d05-117">The attribute value is a pointer to your callback object.</span></span>
3.  <span data-ttu-id="78d05-118">Wenn Sie den Quell Reader erstellen, übergeben Sie den Attribut Speicher an die Erstellungs Funktion im *pattributes* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="78d05-118">When you create the Source Reader, pass the attribute store to the creation function in the *pAttributes* parameter.</span></span> <span data-ttu-id="78d05-119">Alle Funktionen zum Erstellen des Quell Readers verfügen über diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="78d05-119">All of the functions to create the Source Reader have this parameter.</span></span>

<span data-ttu-id="78d05-120">Das folgende Beispiel zeigt die erforderlichen Schritte:</span><span class="sxs-lookup"><span data-stu-id="78d05-120">The following example shows these steps.</span></span>


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="78d05-121">Nachdem Sie den Quell Leser erstellt haben, können Sie nicht zwischen synchronen und asynchronen Modi wechseln.</span><span class="sxs-lookup"><span data-stu-id="78d05-121">After you create the Source Reader, you cannot switch modes between synchronous and asynchronous.</span></span>

<span data-ttu-id="78d05-122">Zum Abrufen von Daten im asynchronen Modus wird die Methode "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " aufgerufen, aber die letzten vier Parameter werden auf **null** festgelegt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="78d05-122">To get data in asynchronous mode, call the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method but set the last four parameters to **NULL**, as shown in the following example.</span></span>


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



<span data-ttu-id="78d05-123">Wenn die "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) "-Methode asynchron abgeschlossen wird, ruft der Quell Leser die [**IMF sourcereadercallback:: onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="78d05-123">When the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method completes asynchronously, the Source Reader calls your [**IMFSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method.</span></span> <span data-ttu-id="78d05-124">Diese Methode hat fünf Parameter:</span><span class="sxs-lookup"><span data-stu-id="78d05-124">This method has five parameters:</span></span>

-   <span data-ttu-id="78d05-125">*hrStatus*: enthält einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="78d05-125">*hrStatus*: Contains an **HRESULT** value.</span></span> <span data-ttu-id="78d05-126">Dies ist derselbe Wert, den "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " im synchronen Modus zurückgeben würde.</span><span class="sxs-lookup"><span data-stu-id="78d05-126">This is the same value that [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) would return in synchronous mode.</span></span> <span data-ttu-id="78d05-127">Wenn *hrStatus* einen Fehlercode enthält, können Sie die restlichen Parameter ignorieren.</span><span class="sxs-lookup"><span data-stu-id="78d05-127">If *hrStatus* contains an error code, you can ignore the remaining parameters.</span></span>
-   <span data-ttu-id="78d05-128">*dwstreamindex*, *dwstreamflags*, lltimestamp und *psample*: Diese drei Parameter entsprechen den letzten drei Parametern in "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)".</span><span class="sxs-lookup"><span data-stu-id="78d05-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp, and *pSample*: These three parameters are equivalent to the last three parameters in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="78d05-129">Sie enthalten die Datenstrom Nummer, Statusflags und den [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="78d05-129">They contain the stream number, status flags, and [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, respectively.</span></span>


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



<span data-ttu-id="78d05-130">Außerdem werden von der Rückruf Schnittstelle zwei weitere Methoden definiert:</span><span class="sxs-lookup"><span data-stu-id="78d05-130">In addition, the callback interface defines two other methods:</span></span>

-   <span data-ttu-id="78d05-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span><span class="sxs-lookup"><span data-stu-id="78d05-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span></span> <span data-ttu-id="78d05-132">Benachrichtigt die Anwendung, wenn bestimmte Ereignisse in der Medienquelle auftreten, z. b. Pufferung oder Netzwerk Verbindungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="78d05-132">Notifies the application when certain events occur in media source, such as buffering or network connection events.</span></span>
-   <span data-ttu-id="78d05-133">[**Onflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span><span class="sxs-lookup"><span data-stu-id="78d05-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span></span> <span data-ttu-id="78d05-134">Wird aufgerufen, wenn die [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) -Methode abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="78d05-134">Called when the [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) method completes.</span></span>

## <a name="implementing-the-callback-interface"></a><span data-ttu-id="78d05-135">Implementieren der Rückruf Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="78d05-135">Implementing the Callback Interface</span></span>

<span data-ttu-id="78d05-136">Die Rückruf Schnittstelle muss Thread sicher sein, da [**onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) und die anderen Rückruf Methoden von Arbeitsthreads aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="78d05-136">The callback interface must be thread-safe, because [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) and the other callback methods are called from worker threads.</span></span>

<span data-ttu-id="78d05-137">Es gibt verschiedene Ansätze, die Sie bei der Implementierung des Rückrufs durchführen können.</span><span class="sxs-lookup"><span data-stu-id="78d05-137">There are several different approaches you can take when you implement the callback.</span></span> <span data-ttu-id="78d05-138">Beispielsweise können Sie die gesamte Arbeit innerhalb des Rückrufs ausführen, oder Sie können den Rückruf verwenden, um die Anwendung zu benachrichtigen (z. b. durch Signalisieren eines Ereignis Handles) und dann die Arbeit aus dem Anwendungs Thread ausführen.</span><span class="sxs-lookup"><span data-stu-id="78d05-138">For example, you can do all of the work inside the callback, or you can use the callback to notify the application (for example, by signaling an event handle) and then do work from the application thread.</span></span>

<span data-ttu-id="78d05-139">Die [**onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) -Methode wird einmal für jeden Aufruf aufgerufen, den Sie an der [**imfsourcereader:: lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) -Methode vornehmen.</span><span class="sxs-lookup"><span data-stu-id="78d05-139">The [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method will be called once for every call that you make to the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method.</span></span> <span data-ttu-id="78d05-140">Um das nächste Beispiel abzurufen, nennen Sie "read **Sample** " erneut.</span><span class="sxs-lookup"><span data-stu-id="78d05-140">To get the next sample, call **ReadSample** again.</span></span> <span data-ttu-id="78d05-141">Wenn ein Fehler auftritt, wird " **onlesesample** " mit einem Fehlercode für den Parameter " *hrStatus* " aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="78d05-141">If an error occurs, **OnReadSample** is called with an error code for the *hrStatus* parameter.</span></span>

<span data-ttu-id="78d05-142">Das folgende Beispiel zeigt eine minimale Implementierung der Rückruf Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="78d05-142">The following example shows a minimal implementation of the callback interface.</span></span> <span data-ttu-id="78d05-143">Hier ist die Deklaration einer Klasse, die die-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="78d05-143">First, here is the declaration of a class that implements the interface.</span></span>


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



<span data-ttu-id="78d05-144">In diesem Beispiel sind die [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) -Methode und die [**onflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) -Methode nicht interessiert, sodass Sie einfach **S \_ OK** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="78d05-144">In this example, we are not interested in the [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) and [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) methods, so they simply return **S\_OK**.</span></span> <span data-ttu-id="78d05-145">Die-Klasse verwendet ein Ereignis handle, um die Anwendung zu signalisieren. Dieses Handle wird durch den-Konstruktor bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="78d05-145">The class uses an event handle to signal the application; this handle is provided through the constructor.</span></span>

<span data-ttu-id="78d05-146">In diesem minimalen Beispiel druckt die [**onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) -Methode nur den Zeitstempel im Konsolenfenster.</span><span class="sxs-lookup"><span data-stu-id="78d05-146">In this minimal example, the [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method just prints the time stamp to the console window.</span></span> <span data-ttu-id="78d05-147">Anschließend werden der Statuscode und das Flag für das Ende des Streams gespeichert und dem Ereignis Handle signalisiert:</span><span class="sxs-lookup"><span data-stu-id="78d05-147">Then it stores the status code and the end-of-stream flag, and signals the event handle:</span></span>


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



<span data-ttu-id="78d05-148">Der folgende Code zeigt, wie die Anwendung diese Rückruf Klasse verwendet, um alle Video Frames aus einer Mediendatei zu lesen:</span><span class="sxs-lookup"><span data-stu-id="78d05-148">The following code shows the application would use this callback class to read all of the video frames from a media file:</span></span>


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="78d05-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78d05-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78d05-150">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="78d05-150">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 



