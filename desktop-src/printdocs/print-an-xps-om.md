---
description: Beschreibt, wie ein XPS-OM als XPS-Dokument an einen Drucker gesendet wird.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Drucken eines XPS-OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01ae1081c4f0c58c66efedc30406e310dd8dd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042438"
---
# <a name="print-an-xps-om"></a><span data-ttu-id="e8da9-103">Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="e8da9-103">Print an XPS OM</span></span>

<span data-ttu-id="e8da9-104">Beschreibt, wie ein XPS-OM als XPS-Dokument an einen Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8da9-104">Describes how to send an XPS OM to a printer as an XPS document.</span></span>

<span data-ttu-id="e8da9-105">Anweisungen zum Drucken eines XPS-OMS, das ein vollständiges XPS-Dokument enthält, finden Sie unter [Drucken eines vollständigen XPS-OMS](#print-a-complete-xps-om).</span><span class="sxs-lookup"><span data-stu-id="e8da9-105">For instructions on how to print an XPS OM that contains a complete XPS document, see [Print a complete XPS OM](#print-a-complete-xps-om).</span></span> <span data-ttu-id="e8da9-106">Um ein XPS-Dokument zu enthalten, muss ein XPS-OM die unter [Erstellen eines leeren XPS-Maps](create-a-blank-xps-om.md)aufgeführten Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="e8da9-106">To contain an XPS document, an XPS OM must include the items listed in [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>

<span data-ttu-id="e8da9-107">Anweisungen zum Drucken eines XPS-OMS, das jeweils nacheinander erstellt oder verarbeitet wird, finden Sie unter [inkrementelles Drucken eines XPS-OM](#incrementally-print-an-xps-om).</span><span class="sxs-lookup"><span data-stu-id="e8da9-107">For instructions on how to print an XPS OM that is being created or processed one page at a time, see [Incrementally print an XPS OM](#incrementally-print-an-xps-om).</span></span>

<span data-ttu-id="e8da9-108">Bevor Sie diese Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e8da9-108">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

<span data-ttu-id="e8da9-109">In diesem Thema erfahren Sie, wie Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="e8da9-109">In this topic, you will learn how to perform the following tasks:</span></span>

-   [<span data-ttu-id="e8da9-110">Drucken eines vollständigen XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="e8da9-110">Print a complete XPS OM</span></span>](#print-a-complete-xps-om)
-   [<span data-ttu-id="e8da9-111">Inkrementelles Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="e8da9-111">Incrementally print an XPS OM</span></span>](#incrementally-print-an-xps-om)
-   [<span data-ttu-id="e8da9-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8da9-112">Related topics</span></span>](#related-topics)

## <a name="print-a-complete-xps-om"></a><span data-ttu-id="e8da9-113">Drucken eines vollständigen XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="e8da9-113">Print a complete XPS OM</span></span>

<span data-ttu-id="e8da9-114">Wenn ein XPS-OM ein vollständiges XPS-Dokument enthält, kann die " [**Write**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) "-Methode der [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) -Schnittstelle den Inhalt des XPS-OMS an einen Drucker oder eine Druck Warteschlange senden.</span><span class="sxs-lookup"><span data-stu-id="e8da9-114">When an XPS OM contains a complete XPS document, the [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface can send the contents of the XPS OM to a printer or a print queue.</span></span>

<span data-ttu-id="e8da9-115">Um zu ermitteln, wann der Druckauftrag abgeschlossen wurde, erstellen Sie ein Ereignis handle, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8da9-115">To detect when the print job has completed, create an event handle as shown in the following example.</span></span>


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="e8da9-116">So drucken Sie ein vollständiges XPS-om:</span><span class="sxs-lookup"><span data-stu-id="e8da9-116">To print a complete XPS OM:</span></span>

1.  <span data-ttu-id="e8da9-117">Erstellen Sie einen neuen Druckauftrags Datenstrom, indem Sie [**startxpsprintjob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-117">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="e8da9-118">Senden Sie den Inhalt des XPS-OMS in den Stream, indem Sie die Methode " [**Write-tostream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) " des Pakets aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-118">Send the contents of the XPS OM to the stream by calling the package's [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method.</span></span>
3.  <span data-ttu-id="e8da9-119">Schließen Sie den Druckauftrags Datenstrom, indem Sie die **Close** -Methode des Streams aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-119">Close the print job stream by calling the stream's **Close** method.</span></span>
4.  <span data-ttu-id="e8da9-120">Warten Sie, bis der Druckauftrag signalisiert hat, dass er abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e8da9-120">Wait for the print job to signal that it has completed.</span></span>
5.  <span data-ttu-id="e8da9-121">Überprüfen Sie den Abschluss Status.</span><span class="sxs-lookup"><span data-stu-id="e8da9-121">Check the completion status.</span></span>
6.  <span data-ttu-id="e8da9-122">Schließen und Freigeben von Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-122">Close and release resources.</span></span>


```C++
    IXpsPrintJob *job = NULL;
    IXpsPrintJobStream *jobStream = NULL;
    hr = StartXpsPrintJob(
                printerName,
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Write package to print job stream
    hr = package->WriteToStream (jobStream, FALSE);

    // Close the stream to tell the print job
    // that the entire document has been sent.
    hr = jobStream->Close();

    // Wait for the print job to finish spooling...
    if (NULL != completionEvent) {
        if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
        {
            // Get the print job status to see why the wait completed.
            //  Note that without waiting for a completion event, 
            //  the print job may not be complete when the status is queried.
            XPS_JOB_STATUS jobStatus;
            hr = job->GetJobStatus(&jobStatus);

            // Evaluate the job status returned.
            switch (jobStatus.completion)
            {
                case XPS_JOB_COMPLETED:
                    // The job completed as expected.
                    hr = S_OK;
                    break;
                case XPS_JOB_CANCELLED:
                    // The job was canceled.
                    hr = E_FAIL;
                    break;
                case XPS_JOB_FAILED:
                    // The job failed, 
                    // jobStatus.jobStatus has the reason.
                    hr = E_FAIL;
                    break;
                default:
                    // An unexpected value was returned.
                    hr = E_UNEXPECTED;
                    break;
            }
                
            // Release completion event handle
            CloseHandle(completionEvent);
        }
        else
        {    // there was a problem, set hr to error status
            hr  = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // hr contains the result of the print operation

    CoUninitialize(); // if COM is no longer needed in this thread
```



## <a name="incrementally-print-an-xps-om"></a><span data-ttu-id="e8da9-123">Inkrementelles Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="e8da9-123">Incrementally print an XPS OM</span></span>

<span data-ttu-id="e8da9-124">Sie können die Dokument Komponenten eines XPS OM inkrementell an einen Drucker Auftrag senden, indem Sie einen XPS-Druckauftrags Datenstrom erstellen und die einzelnen Dokument Komponenten nacheinander an den Druckauftrags Datenstrom übergeben.</span><span class="sxs-lookup"><span data-stu-id="e8da9-124">You can send the document components of an XPS OM to a printer job incrementally, by creating an XPS print job stream and then passing the individual document components to the print job stream, one at a time.</span></span> <span data-ttu-id="e8da9-125">Die Reihenfolge, in der die Dokument Komponenten gesendet werden, bestimmt, wie diese im fertigen Dokument angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e8da9-125">The sequence in which the document components are sent determines how they will appear in the finished document.</span></span> <span data-ttu-id="e8da9-126">Daher muss die Dokument Komponenten ordnungsgemäß organisiert werden, bevor ein Programm den Code in diesem Beispiel abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="e8da9-126">Thus, before a program can call the code in this example, it must correctly organize the document components.</span></span>

<span data-ttu-id="e8da9-127">Bevor Sie XPS OM-Schnittstellen verwenden, initialisieren Sie com im Thread, wie im folgenden Beispielcode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8da9-127">Before using XPS OM interfaces, initialize COM in the thread as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="e8da9-128">Erstellen Sie ein Ereignis handle, wie im folgenden Beispielcode gezeigt, um den Abschluss des Druckauftrags zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-128">To monitor the print job completion, create an event handle as shown in the following example code.</span></span>


```C++
    HANDLE completionEvent = NULL;
    completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="e8da9-129">Erstellen Sie einen neuen Druckauftrags Datenstrom und einen neuen paketwriter.</span><span class="sxs-lookup"><span data-stu-id="e8da9-129">Create a new print job stream and a new package writer.</span></span> <span data-ttu-id="e8da9-130">Übergeben Sie die einzelnen Dokument Komponenten an die entsprechenden paketwriter-Methoden in derselben Reihenfolge, in der Sie im fertigen Dokument angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e8da9-130">Pass each of the document components to the corresponding package writer methods in the same sequence as they will appear in the finished document.</span></span>

<span data-ttu-id="e8da9-131">Starten Sie jedes Dokument neu, und fügen Sie ihm Seiten hinzu.</span><span class="sxs-lookup"><span data-stu-id="e8da9-131">Start each document new, then add pages to it.</span></span> <span data-ttu-id="e8da9-132">Nachdem Sie alle Dokument Komponenten an den Druckauftrags Datenstrom übergeben haben, schließen Sie den Stream, warten Sie, bis der Druckauftrag abgeschlossen ist, und schließen Sie dann offene Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-132">After passing all document components to the print job stream, close the stream, wait for the print job to complete, and then close and release open resources.</span></span>

1.  <span data-ttu-id="e8da9-133">Erstellen Sie einen neuen Druckauftrags Datenstrom, indem Sie [**startxpsprintjob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-133">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="e8da9-134">Erstellen Sie einen Teil-URI für den FixedDocumentSequence-Teil.</span><span class="sxs-lookup"><span data-stu-id="e8da9-134">Create a part URI for the FixedDocumentSequence part.</span></span>
3.  <span data-ttu-id="e8da9-135">Erstellen Sie einen neuen paketwriter im Druckauftrags Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e8da9-135">Create a new package writer on the print job stream.</span></span>
4.  <span data-ttu-id="e8da9-136">Für jedes Dokument, das geschrieben werden soll:</span><span class="sxs-lookup"><span data-stu-id="e8da9-136">For each document to be written:</span></span>
    1.  <span data-ttu-id="e8da9-137">Erstellen Sie einen neuen Teil-URI für den FixedDocument-Teil.</span><span class="sxs-lookup"><span data-stu-id="e8da9-137">Create a new part URI for the FixedDocument part.</span></span>
    2.  <span data-ttu-id="e8da9-138">Startet ein neues Dokument im paketwriter.</span><span class="sxs-lookup"><span data-stu-id="e8da9-138">Start a new document in the package writer.</span></span>
    3.  <span data-ttu-id="e8da9-139">Erstellen Sie für jede Seite im aktuellen Dokument einen Teil-URI für den FixedPage-Teil, und fügen Sie die Seite dem paketwriter hinzu.</span><span class="sxs-lookup"><span data-stu-id="e8da9-139">For each page in the current document, create a part URI for the FixedPage part and add the page to the package writer.</span></span>
5.  <span data-ttu-id="e8da9-140">Nachdem dem paketwriter alle Seiten hinzugefügt wurden, schließen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="e8da9-140">After all pages have been added to the package writer, close it.</span></span>
6.  <span data-ttu-id="e8da9-141">Schließen Sie den Druckauftrags Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e8da9-141">Close the print job stream.</span></span>
7.  <span data-ttu-id="e8da9-142">Warten Sie, bis der Druckauftrag vollständig ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e8da9-142">Wait for the print job to complete.</span></span>
8.  <span data-ttu-id="e8da9-143">Überprüfen Sie den Abschluss Status.</span><span class="sxs-lookup"><span data-stu-id="e8da9-143">Check the completion status.</span></span>
9.  <span data-ttu-id="e8da9-144">Schließen und freigeben offener Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e8da9-144">Close and release open resources.</span></span>


```C++
    IXpsPrintJob* job = NULL;
    IXpsPrintJobStream* jobStream = NULL;
    hr = StartXpsPrintJob(
                argv[1],
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Note the implicit requirement that CoInitializeEx 
    //  has previously been called from this thread.
    IXpsOMObjectFactory *xpsFactory = NULL;
    hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IXpsOMObjectFactory),
                reinterpret_cast<void**>(&xpsFactory)
                );
    // Create part URI for FixedDocumentSequence part
    //  This can use a static string because there is only one
    //  FixedDocumentSequence part in the print job.
    IOpcPartUri *partUri = NULL;
    hr = xpsFactory->CreatePartUri(L"/FixedDocumentSequence.fdseq", &partUri);

    // Create the package writer on the print job stream
    //  Note that the interleaving parameter set to 
    //  XPS_INTERLEAVING_ON, the package writer will create
    //  empty print ticket parts when a NULL pointer is
    //  passed in the print ticket argument of this method,
    //  the StartNewDocument method, and the AddPage method.
    //  For more information, see the help for these methods.
    IXpsOMPackageWriter *packageWriter = NULL;
    hr = xpsFactory->CreatePackageWriterOnStream(
            jobStream,
            TRUE,
            XPS_INTERLEAVING_ON, // to create blank print ticket objects
            partUri,
            NULL,
            NULL,
            NULL,
            NULL,
            &packageWriter);
    // release partUri after it's been used to create new doc. seq.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    // Add document content to the print job stream.
    int docNumber = 1;
    int docsInPackage = 1; // Change this value as required.
    while (docNumber <= docsInPackage) {

        // Create a unique part URI for the current document.
        WCHAR DocPartUri[MAX_PATH];
        hr = MakeDocumentPartUri (docNumber, MAX_PATH, DocPartUri);
        hr = xpsFactory->CreatePartUri(DocPartUri, &partUri);
        
        // Initialize the new document in the package writer.
        hr = packageWriter->StartNewDocument(partUri, NULL, NULL, NULL, NULL);

        // release part URI after it's been used to create new doc.
        if (partUri)
        {
            partUri->Release();
            partUri = NULL;
        }

        // Add the pages
        int pageNumber = 1;
        int pagesInDocument = 1; // Change this value as required.
        while (pageNumber <= pagesInDocument) {

            // Create a unique part URI for the current page
            WCHAR PagePartUri[MAX_PATH];
            hr = MakePagePartUri (
                docNumber, 
                pageNumber, 
                MAX_PATH, 
                PagePartUri);
            hr = xpsFactory->CreatePartUri(PagePartUri, &partUri);

            // create page in OM
            XPS_SIZE pageSize = {816, 1056};
            IXpsOMPage *xpsPage = NULL;
            hr = xpsFactory->CreatePage(
                &pageSize, 
                L"en-US", 
                partUri, 
                &xpsPage);

            // release pagePartUri after it's been used to create the page
            if (partUri)
            {
                partUri->Release();
                partUri = NULL;
            }

            // add content to the page or retrieve 
            //  the page from the XPS OM.
            //  (not shown in this example)

            // add page to document
            hr = packageWriter->AddPage(
                        xpsPage,
                        &pageSize,
                        NULL,
                        NULL,
                        NULL,
                        NULL);

             if (xpsPage)
              {
                 xpsPage->Release();
                 xpsPage = NULL;
             }

            // go to the next page
            pageNumber++;
        }
        // the fixed document does not need to be closed.
        // it will be closed when a new fixed doc is opened
        // or the package is closed.

        // go to the next document
        docNumber++;
    }

    // Close the package writer when finished
    hr = packageWriter->Close();

    if (SUCCEEDED(hr))
    {
        // Close the print stream to tell the print
        //  job that the all document contents have
        //  been sent
        hr = jobStream->Close();
        // Wait for the print job to finish spooling...
        if (NULL != completionEvent) {
            if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
            {
                // Get the print job status to see why the wait completed.
                //  Note that without waiting for a completion event, 
                //  the print job may not be complete when the status is queried.
                XPS_JOB_STATUS jobStatus;
                hr = job->GetJobStatus(&jobStatus);

                // Evaluate the job status returned.
                switch (jobStatus.completion)
                {
                    case XPS_JOB_COMPLETED:
                        // The job completed as expected.
                        hr = S_OK;
                        break;
                    case XPS_JOB_CANCELLED:
                        // The job was canceled.
                        hr = E_FAIL;
                        break;
                    case XPS_JOB_FAILED:
                        // The job failed, 
                        // jobStatus.jobStatus has the reason.
                        hr = E_FAIL;
                        break;
                    default:
                        // An unexpected value was returned.
                        hr = E_UNEXPECTED;
                        break;
                }
                    
                // Release completion event handle
                CloseHandle(completionEvent);
            }
            else
            {    // there was a problem, set hr to error status
                hr  = HRESULT_FROM_WIN32(GetLastError());
            }
        }
    } 
    else
    {
        // cancel the job, if one exists, because
        //  the close call returned an error
        if (job) job->Cancel();
    }
    // hr contains the result of the print operation

    // free/release pointers and handles used.

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

    CoUninitialize(); // If done with COM in this thread.
```



<span data-ttu-id="e8da9-145">Wenn das Programm die Dokument Komponenten inkrementell schreibt, wie in diesem Beispiel gezeigt, muss es die Teilnamen für jeden Dokument Teil generieren, der an den Druckauftrags Datenstrom gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8da9-145">When the program is writing the document components incrementally, as shown in this example, it must generate the part names for each document part that it sends to the print job stream.</span></span> <span data-ttu-id="e8da9-146">Im vorangehenden Beispiel wird der FixedDocumentSequence-Teil-URI aus einer statischen Zeichenfolge erstellt, da nur ein solcher Teil im XPS-Dokument vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e8da9-146">In the preceding example, the FixedDocumentSequence part URI is created from a static string because there is one and only one such part in the XPS document.</span></span> <span data-ttu-id="e8da9-147">Der URI jedes FixedPage-und FixedDocument-Teils muss innerhalb des XPS-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="e8da9-147">The URI of each FixedPage and FixedDocument part must be unique within the XPS document.</span></span> <span data-ttu-id="e8da9-148">Wenn Sie den Teil-URI mit dem Index dieser Komponenten verwenden, können Sie sicherstellen, dass die resultierende URI-Zeichenfolge innerhalb des XPS-Dokuments eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="e8da9-148">Building the part URI by using the index of these components can help ensure that the resulting URI string is unique within the XPS document.</span></span>


```C++
HRESULT MakeDocumentPartUri (
                              __in int docNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //  that was passed as an argument
    // for example, "/Documents/1/FixedDocument.fdoc"
    //  where "1" specifies the document number, which would
    //  change with each document printed
    return S_OK;
}
 
HRESULT MakePagePartUri (
                              __in int docNumber,
                              __in int pageNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //   and page number that were passed as an argument
    // for example: "/Documents/1/Pages/1.fpage"
    //  where the first "1" between Documents and Pages 
    //  specifies the document number, which would change with
    //  each document. The second "1" specifies the page number,
    //  which would change with each page in the document.
    return S_OK;
}
```



<span data-ttu-id="e8da9-149">Weitere Informationen zur Struktur eines XPS-Dokuments finden Sie in der [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="e8da9-149">For more information on the structure of an XPS document, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8da9-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8da9-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e8da9-151">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="e8da9-151">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="e8da9-152">Schreiben eines XPS-om in ein XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="e8da9-152">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

<span data-ttu-id="e8da9-153">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="e8da9-153">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="e8da9-154">**CoInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="e8da9-154">**CoInitializeEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="e8da9-155">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="e8da9-155">**CreateEvent**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="e8da9-156">**Iopcparamei**</span><span class="sxs-lookup"><span data-stu-id="e8da9-156">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="e8da9-157">**Ixpsompackage**</span><span class="sxs-lookup"><span data-stu-id="e8da9-157">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="e8da9-158">**Ixpsompackagewriter**</span><span class="sxs-lookup"><span data-stu-id="e8da9-158">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="e8da9-159">**Ixpsprintjob**</span><span class="sxs-lookup"><span data-stu-id="e8da9-159">**IXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[<span data-ttu-id="e8da9-160">**Ixpsprintjobstream**</span><span class="sxs-lookup"><span data-stu-id="e8da9-160">**IXpsPrintJobStream**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[<span data-ttu-id="e8da9-161">**Startxpsprintjob**</span><span class="sxs-lookup"><span data-stu-id="e8da9-161">**StartXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[<span data-ttu-id="e8da9-162">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="e8da9-162">**WaitForSingleObject**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

<span data-ttu-id="e8da9-163">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="e8da9-163">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="e8da9-164">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="e8da9-164">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="e8da9-165">XPS-Dokument-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="e8da9-165">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="e8da9-166">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e8da9-166">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
