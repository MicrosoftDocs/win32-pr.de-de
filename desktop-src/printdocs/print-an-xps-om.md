---
description: Beschreibt, wie ein XPS OM als XPS-Dokument an einen Drucker gesendet wird.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Drucken eines XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f1386352cff1556a5ce2403f34ebe4258c4110d4c3bf455990f3f1eb226d17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470903"
---
# <a name="print-an-xps-om"></a>Drucken eines XPS OM

Beschreibt, wie ein XPS OM als XPS-Dokument an einen Drucker gesendet wird.

Anweisungen zum Drucken eines XPS OM, das ein vollständiges XPS-Dokument enthält, finden Sie unter [Drucken eines vollständigen XPS OM.](#print-a-complete-xps-om) Um ein XPS-Dokument enthalten zu können, muss ein XPS OM die unter Erstellen eines leeren XPS OM aufgeführten [Elemente enthalten.](create-a-blank-xps-om.md)

Anweisungen zum Drucken eines XPS OM, das gleichzeitig erstellt oder verarbeitet wird, finden Sie unter [Inkrementelles](#incrementally-print-an-xps-om)Drucken eines XPS OM.

Bevor Sie diese Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss unter [Allgemeine XPS-Dokumentprogrammieraufgaben](common-xps-document-tasks.md).

In diesem Thema erfahren Sie, wie Sie die folgenden Aufgaben ausführen:

-   [Drucken eines vollständigen XPS OM](#print-a-complete-xps-om)
-   [Inkrementelles Drucken eines XPS OM](#incrementally-print-an-xps-om)
-   [Zugehörige Themen](#related-topics)

## <a name="print-a-complete-xps-om"></a>Drucken eines vollständigen XPS OM

Wenn ein XPS OM ein vollständiges XPS-Dokument enthält, kann die [**WriteToStream-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) der [**IXpsOMPackage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) den Inhalt des XPS OM an einen Drucker oder eine Druckwarteschlange senden.

Um zu ermitteln, wann der Druckauftrag abgeschlossen wurde, erstellen Sie ein Ereignishand handle, wie im folgenden Beispiel gezeigt.


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



So drucken Sie ein vollständiges XPS OM

1.  Erstellen Sie einen neuen Druckauftragsstream, indem [**Sie StartXpsPrintJob aufrufen.**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
2.  Senden Sie den Inhalt des XPS OM an den Stream, indem Sie die [**WriteToStream-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) des Pakets aufrufen.
3.  Schließen Sie den Druckauftragsstream, indem Sie die **Close-Methode** des Streams aufrufen.
4.  Warten Sie, bis der Druckauftrag signalisiert, dass er abgeschlossen wurde.
5.  Überprüfen Sie den Abschlussstatus.
6.  Schließen sie Ressourcen, und geben Sie sie frei.


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



## <a name="incrementally-print-an-xps-om"></a>Inkrementelles Drucken eines XPS OM

Sie können die Dokumentkomponenten eines XPS OM inkrementell an einen Druckerauftrag senden, indem Sie einen XPS-Druckauftragsstream erstellen und dann die einzelnen Dokumentkomponenten einzeln an den Druckauftragsstream übergeben. Die Reihenfolge, in der die Dokumentkomponenten gesendet werden, bestimmt, wie sie im fertigen Dokument angezeigt werden. Daher müssen die Dokumentkomponenten ordnungsgemäß organisiert werden, bevor ein Programm den Code in diesem Beispiel aufrufen kann.

Bevor Sie XPS OM-Schnittstellen verwenden, initialisieren Sie COM im Thread, wie im folgenden Beispielcode gezeigt.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Um den Abschluss des Druckauftrags zu überwachen, erstellen Sie ein Ereignishand handle, wie im folgenden Beispielcode gezeigt.


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



Erstellen Sie einen neuen Druckauftragsstream und einen neuen Paketwriter. Übergeben Sie jede der Dokumentkomponenten in derselben Reihenfolge an die entsprechenden Paketwritermethoden, wie sie im fertigen Dokument angezeigt werden.

Starten Sie jedes Dokument neu, und fügen Sie ihm Seiten hinzu. Nachdem Sie alle Dokumentkomponenten an den Druckauftragsstream übergeben haben, schließen Sie den Stream, warten Sie, bis der Druckauftrag abgeschlossen ist, und schließen Sie dann geöffnete Ressourcen, und geben Sie sie frei.

1.  Erstellen Sie einen neuen Druckauftragsstream, indem [**Sie StartXpsPrintJob aufrufen.**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
2.  Erstellen Sie einen Teil-URI für den FixedDocumentSequence-Teil.
3.  Erstellen Sie einen neuen Paketwriter für den Druckauftragsstream.
4.  Für jedes zu schreibende Dokument:
    1.  Erstellen Sie einen neuen Teil-URI für den FixedDocument-Teil.
    2.  Starten Sie ein neues Dokument im Paketwriter.
    3.  Erstellen Sie für jede Seite im aktuellen Dokument einen Teil-URI für den FixedPage-Teil, und fügen Sie die Seite dem Paketwriter hinzu.
5.  Nachdem alle Seiten dem Paketwriter hinzugefügt wurden, schließen Sie sie.
6.  Schließen Sie den Druckauftragsstream.
7.  Warten Sie, bis der Druckauftrag abgeschlossen ist.
8.  Überprüfen Sie den Abschlussstatus.
9.  Schließen Sie geöffnete Ressourcen, und geben Sie sie frei.


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



Wenn das Programm die Dokumentkomponenten inkrementell schreibt, wie in diesem Beispiel gezeigt, muss es die Teilenamen für jeden Dokumentteil generieren, den es an den Druckauftragsstream sendet. Im vorherigen Beispiel wird der FixedDocumentSequence-Teil-URI aus einer statischen Zeichenfolge erstellt, da das XPS-Dokument nur einen teil davon enthält. Der URI jedes FixedPage- und FixedDocument-Teils muss innerhalb des XPS-Dokuments eindeutig sein. Wenn Sie den Teil-URI mithilfe des Index dieser Komponenten erstellen, können Sie sicherstellen, dass die resultierende URI-Zeichenfolge innerhalb des XPS-Dokuments eindeutig ist.


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



Weitere Informationen zur Struktur eines XPS-Dokuments finden Sie im [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Schreiben eines XPS OM in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

**Wird in diesem Abschnitt verwendet**
</dt> <dt>

[**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[**Createevent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**IXpsPrintJob**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[**IXpsPrintJobStream**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[**Waitforsingleobject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren eines XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[REFERENZ ZUR XPS-Dokument-API](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
