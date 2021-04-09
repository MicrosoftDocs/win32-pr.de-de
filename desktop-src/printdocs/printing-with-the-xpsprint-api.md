---
description: In diesem Thema wird beschrieben, wie die XPS-Druck-API zum Drucken aus einer Windows-Anwendung verwendet wird.
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: 'Gewusst wie: Drucken mit der XPS-Druck-API'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867536"
---
# <a name="how-to-print-with-the-xps-print-api"></a><span data-ttu-id="e4df9-103">Gewusst wie: Drucken mit der XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="e4df9-103">How To: Print with the XPS Print API</span></span>

<span data-ttu-id="e4df9-104">In diesem Thema wird beschrieben, wie die [XPS-Druck-API](xpsprint-api.md) zum Drucken aus einer Windows-Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4df9-104">This topic describes how to use the [XPS Print API](xpsprint-api.md) to print from a Windows application.</span></span>

<span data-ttu-id="e4df9-105">Mit der [XPS-Druck-API](xpsprint-api.md) können native Windows-Anwendungen XPS-Dokumente drucken.</span><span class="sxs-lookup"><span data-stu-id="e4df9-105">The [XPS Print API](xpsprint-api.md) enables native Windows applications to print XPS documents.</span></span> <span data-ttu-id="e4df9-106">Eine Anwendung kann ein XPS-Dokument mithilfe der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4df9-106">An application can create an XPS document by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="e4df9-107">Das Thema [Allgemeine XPS-Dokument Programmieraufgaben](/previous-versions/windows/desktop/dd316968(v=vs.85)) beschreibt, wie dies zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="e4df9-107">The [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)) help topic describes how to do this.</span></span> <span data-ttu-id="e4df9-108">Nachdem ein XPS-Dokument erstellt wurde, kann die Anwendung die XPS-Druck-API verwenden, um Sie zu drucken.</span><span class="sxs-lookup"><span data-stu-id="e4df9-108">Once an XPS document has been created, the application can use the XPS Print API to print it.</span></span>

<span data-ttu-id="e4df9-109">Die Verwendung der [XPS-Druck-API](xpsprint-api.md) zum Drucken eines Dokuments aus einer Anwendung umfasst die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="e4df9-109">Using the [XPS Print API](xpsprint-api.md) to print a document from an application involves the following steps.</span></span>

-   [<span data-ttu-id="e4df9-110">COM-Schnittstelle initialisieren</span><span class="sxs-lookup"><span data-stu-id="e4df9-110">Initialize COM Interface</span></span>](#initialize-com-interface)
-   [<span data-ttu-id="e4df9-111">Erstellen eines Abschluss Ereignisses</span><span class="sxs-lookup"><span data-stu-id="e4df9-111">Create a Completion Event</span></span>](#create-a-completion-event)
-   [<span data-ttu-id="e4df9-112">Starten eines XPS-Druckauftrags</span><span class="sxs-lookup"><span data-stu-id="e4df9-112">Start an XPS Print Job</span></span>](#start-an-xps-print-job)
-   [<span data-ttu-id="e4df9-113">Erstellen einer ixpsompackagewriter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e4df9-113">Create an IXpsOMPackageWriter Interface</span></span>](#create-an-ixpsompackagewriter-interface)
-   [<span data-ttu-id="e4df9-114">Schließen Sie die ixpsompackagewriter-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e4df9-114">Close the IXpsOMPackageWriter Interface</span></span>](#close-the-ixpsompackagewriter-interface)
-   [<span data-ttu-id="e4df9-115">Schließen Sie den Druckauftrags Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e4df9-115">Close the Print Job Stream</span></span>](#close-the-print-job-stream)
-   [<span data-ttu-id="e4df9-116">Auf Abschluss Ereignis warten</span><span class="sxs-lookup"><span data-stu-id="e4df9-116">Wait for the Completion Event</span></span>](#wait-for-the-completion-event)
-   [<span data-ttu-id="e4df9-117">Freigeben von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e4df9-117">Release Resources</span></span>](#release-resources)

<span data-ttu-id="e4df9-118">Die [XPS-Druck-API](xpsprint-api.md) erfordert, dass ein XPS-Dokument gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="e4df9-118">The [XPS Print API](xpsprint-api.md) requires an XPS document to print.</span></span> <span data-ttu-id="e4df9-119">Im folgenden Beispiel wird das XPS-Dokument erstellt, das von der XPS-Druck-API an den Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4df9-119">In the following example, the XPS document is created as it is sent to the printer by the XPS Print API.</span></span> <span data-ttu-id="e4df9-120">Es ist auch möglich, ein XPS-Dokument zu erstellen, ohne es mit der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) an einen Drucker zu senden und als XPS-OM zu verwalten oder das XPS-OM als XPS-Dokument zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e4df9-120">It is also possible to create an XPS document without sending it to a printer by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and maintaining it as an XPS OM or by saving the XPS OM as an XPS document.</span></span> <span data-ttu-id="e4df9-121">Weitere Informationen zur Verwendung von XPS OM finden Sie in der XPS-Dokument-API.</span><span class="sxs-lookup"><span data-stu-id="e4df9-121">For more information about using an XPS OM, see the XPS Document API.</span></span>

### <a name="initialize-com-interface"></a><span data-ttu-id="e4df9-122">COM-Schnittstelle initialisieren</span><span class="sxs-lookup"><span data-stu-id="e4df9-122">Initialize COM Interface</span></span>

<span data-ttu-id="e4df9-123">Initialisieren Sie die COM-Schnittstelle, wenn die Anwendung dies noch nicht getan hat.</span><span class="sxs-lookup"><span data-stu-id="e4df9-123">Initialize the COM interface, if the application has not already done so.</span></span>


```C++
    // Initialize the COM interface, if the application has not 
    //  already done so.
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        fwprintf(stderr, 
            L"ERROR: CoInitializeEx failed with HRESULT 0x%X\n", hr);
        return 1;
    }
```



### <a name="create-a-completion-event"></a><span data-ttu-id="e4df9-124">Erstellen eines Abschluss Ereignisses</span><span class="sxs-lookup"><span data-stu-id="e4df9-124">Create a Completion Event</span></span>

<span data-ttu-id="e4df9-125">Erstellen Sie ein Abschluss Ereignis, das die [XPS-Druck-API](xpsprint-api.md) verwendet, um die Anwendung zu benachrichtigen, wenn der Druck Spooler das gesamte Dokument von der Anwendung erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="e4df9-125">Create a completion event, which the [XPS Print API](xpsprint-api.md) uses to notify the application when the print spooler has received the entire document from the application.</span></span> <span data-ttu-id="e4df9-126">Die XPS-Druck-API unterstützt auch ein Fortschritts Ereignis, sodass eine Anwendung über andere spoolingaktivitäten informiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4df9-126">The XPS Print API also supports a progress event so an application can know about other spooling activity.</span></span>


```C++
        // Create the completion event
        completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
        if (!completionEvent)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(stderr, 
                L"ERROR: Could not create completion event: %08X\n", hr);
        }
```



### <a name="start-an-xps-print-job"></a><span data-ttu-id="e4df9-127">Starten eines XPS-Druckauftrags</span><span class="sxs-lookup"><span data-stu-id="e4df9-127">Start an XPS Print Job</span></span>

<span data-ttu-id="e4df9-128">Starten Sie einen XPS-Druckauftrag durch Aufrufen von [**startxpsprintjob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="e4df9-128">Start an XPS print job by calling [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span> <span data-ttu-id="e4df9-129">**Startxpsprintjob** gibt einen Datenstrom zurück, in den die Anwendung das zu druckende Dokument sendet.</span><span class="sxs-lookup"><span data-stu-id="e4df9-129">**StartXpsPrintJob** returns a stream into which the application will send the document to be printed.</span></span>


```C++
        // Start an XPS Print Job
        if (FAILED(hr = StartXpsPrintJob(
                    printerName,
                    NULL,
                    NULL,
                    NULL,
                    completionEvent,
                    NULL,
                    0,
                    &job,
                    &jobStream,
                    NULL
                    )))
        {
            fwprintf(stderr, 
                L"ERROR: Could not start XPS print job: %08X\n", hr);
        }
```



### <a name="create-an-ixpsompackagewriter-interface"></a><span data-ttu-id="e4df9-130">Erstellen einer ixpsompackagewriter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e4df9-130">Create an IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="e4df9-131">Erstellen Sie eine [**ixpsompackagewriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle, indem Sie [**ixpsomobjectfactory:: createpackageschreiteronstream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) für den von [**startxpsprintjob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob)zurückgegebenen Stream aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4df9-131">Create an [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface by calling [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) on the stream returned by [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span>


```C++
    // Create an XPS OM Object Factory. If one has already been 
    //  created by the application, a new one is not necessary.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory), 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&xpsFactory))))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create XPS OM Object Factory: %08X\n", 
                hr);
        }
    }
    // Create the Part URI for the Fixed Document Sequence. The
    //  Fixed Document Sequence is the top-level element in the
    //  package hierarchy of objects. There is one Fixed Document
    //  Sequence in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name used in this example is the part name
    //  used by convention.
    //
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/FixedDocumentSequence.fdseq", 
                    &partUri)))
        {
            fwprintf(stderr, 
                L"ERROR: Could not create part URI: %08X\n", hr);
        }
    }

    // Create the package writer on the print job stream.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePackageWriterOnStream(
                    jobStream,
                    TRUE,
                    XPS_INTERLEAVING_ON,
                    partUri,
                    NULL,
                    NULL,
                    NULL,
                    NULL,
                    &packageWriter
                    )
                )
           )
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create package writer: 0x%X\n", 
                hr);
        }
    }

    // Release the part URI interface.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



<span data-ttu-id="e4df9-132">Starten Sie für jedes Dokument in diesem Druckauftrag ein neues Dokument, und fügen Sie diesem Dokument Seiten hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4df9-132">For each document in this print job, start a new document and then add pages to that document.</span></span>

### <a name="start-a-new-document"></a><span data-ttu-id="e4df9-133">Neues Dokument starten</span><span class="sxs-lookup"><span data-stu-id="e4df9-133">Start a New Document</span></span>

<span data-ttu-id="e4df9-134">Startet ein neues Dokument im paketwriter, indem [**ixpsompackagewriter:: startnewdocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e4df9-134">Start a new document in the package writer by calling [**IXpsOMPackageWriter::StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span></span> <span data-ttu-id="e4df9-135">Wenn ein Dokument geöffnet ist, wenn diese Methode aufgerufen wird, wird es geschlossen, und ein neues Dokument wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e4df9-135">If a document is open when this method is called, it is closed and a new document is opened.</span></span>


```C++
    // Create the Part URI for the Fixed Document. The
    //  Fixed Document part contains the pages of the document. 
    //  There can be one or more Fixed Documents in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name format used in this example is the format 
    //  used by convention. The number "1" in this example must be 
    //  changed for each document in the package. For example, 1 
    //  for the first document, 2 for the second, and so on.
    //

    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/Documents/1/FixedDocument.fdoc", 
                    &partUri)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create part URI: %08X\n", 
                hr);
        }
    }

    // Start the new document.
    //
    //  If there was already a document started in this page,
    //  this call will close it and start a new one.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->StartNewDocument(
                    partUri, 
                    NULL, 
                    NULL, 
                    NULL,
                    NULL)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not start new document: 0x%X\n", 
                hr);
        }
    }
    
    // Release the part URI interface
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



### <a name="add-a-page"></a><span data-ttu-id="e4df9-136">Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e4df9-136">Add a Page</span></span>

<span data-ttu-id="e4df9-137">Wenden Sie [**ixpsompackagewriter:: addPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) an, um die einzelnen Seiten des Dokuments aus der Anwendung in das neue Dokument im paketwriter zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e4df9-137">Call [**IXpsOMPackageWriter::AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) to write each of the document's pages from the application to the new document in the package writer.</span></span>

> [!Note]  
> <span data-ttu-id="e4df9-138">Es wird davon ausgegangen, dass die Seite vor diesem Schritt von der Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e4df9-138">The application is assumed to have created the page prior to this step.</span></span> <span data-ttu-id="e4df9-139">Weitere Informationen zum Erstellen von Dokument Seiten und zum Hinzufügen von Inhalten finden Sie unter [Allgemeine XPS-Dokument Programmieraufgaben](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4df9-139">For more information about creating document pages and adding content to them, see the [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        // Add the current page to the document.
        if (FAILED(hr = packageWriter->AddPage(
                    xpsPage,
                    &pageSize,
                    NULL,
                    NULL,
                    NULL,
                    NULL
                    )))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not add page to document: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-ixpsompackagewriter-interface"></a><span data-ttu-id="e4df9-140">Schließen Sie die ixpsompackagewriter-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e4df9-140">Close the IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="e4df9-141">Nachdem alle Dokumente für diesen Druckauftrag geschrieben wurden, können Sie [**ixpsompackagewriter:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) anrufen, um das Paket zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4df9-141">After all the documents have been written for this print job, call [**IXpsOMPackageWriter::Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) to close the package.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->Close()))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not close package writer: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-print-job-stream"></a><span data-ttu-id="e4df9-142">Schließen Sie den Druckauftrags Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e4df9-142">Close the Print Job Stream</span></span>

<span data-ttu-id="e4df9-143">Schließen Sie den Druckauftrags Datenstrom, indem Sie [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close)aufrufen, der dem Druck Spooler mitteilt, dass der gesamte Druckauftrag von der Anwendung gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e4df9-143">Close the print job stream by calling [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), which tells the print spooler that the entire print job has been sent by the application.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = jobStream->Close()))
        {
            fwprintf(
                stderr,
                L"ERROR: Could not close job stream: %08X\n",
                hr);
        }
    }
    else
    {
        // Only cancel the job if we succeeded in creating a job.
        if (job)
        {
            // Tell the XPS Print API that we're giving up.  
            //  Don't overwrite hr with the return from this function.
            job->Cancel();
        }
    }
```



### <a name="wait-for-the-completion-event"></a><span data-ttu-id="e4df9-144">Auf Abschluss Ereignis warten</span><span class="sxs-lookup"><span data-stu-id="e4df9-144">Wait for the Completion Event</span></span>

<span data-ttu-id="e4df9-145">Warten Sie auf das Abschluss Ereignis des Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="e4df9-145">Wait for the print job's completion event.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        wprintf(L"Waiting for job completion...\n");

        if (WaitForSingleObject(completionEvent, INFINITE) != 
                                                    WAIT_OBJECT_0)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(
                stderr, 
                L"ERROR: Wait for completion event failed: %08X\n", 
                hr);
        }
    }
```



<span data-ttu-id="e4df9-146">Nachdem das Abschluss Ereignis signalisiert wurde, können Sie [**getjobstatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) aufrufen, um den Auftragsstatus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e4df9-146">After the completion event is signaled, call [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) to get the job status.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = job->GetJobStatus(&jobStatus)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not get job status: %08X\n", 
                hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        switch (jobStatus.completion)
        {
            case XPS_JOB_COMPLETED:
                break;
            case XPS_JOB_CANCELLED:
                fwprintf(stderr, L"ERROR: job was cancelled\n");
                hr = E_FAIL;
                break;
            case XPS_JOB_FAILED:
                fwprintf(
                    stderr, 
                    L"ERROR: Print job failed: %08X\n", 
                    jobStatus.jobStatus);
                hr = E_FAIL;
                break;
            default:
                fwprintf(stderr, L"ERROR: unexpected failure\n");
                hr = E_UNEXPECTED;
                break;
        }
    }
```



### <a name="release-resources"></a><span data-ttu-id="e4df9-147">Freigeben von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e4df9-147">Release Resources</span></span>

<span data-ttu-id="e4df9-148">Wenn ein Auftragsstatus den Abschluss angibt, geben Sie die für diesen Druckauftrag verwendeten Schnittstellen und Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="e4df9-148">After a job status indicates completion, release the interfaces and resources used for this print job.</span></span>


```C++
    if (packageWriter)
    {
        packageWriter->Release();
        packageWriter = NULL;
    }

    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    if (xpsFactory)
    {
        xpsFactory->Release();
        xpsFactory = NULL;
    }

    if (jobStream)
    {
        jobStream->Release();
        jobStream = NULL;
    }

    if (job)
    {
        job->Release();
        job = NULL;
    }

    if (completionEvent)
    {
        CloseHandle(completionEvent);
        completionEvent = NULL;
    }
```



 

 
