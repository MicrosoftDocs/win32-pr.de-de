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
# <a name="print-an-xps-om"></a>Drucken eines XPS-OM

Beschreibt, wie ein XPS-OM als XPS-Dokument an einen Drucker gesendet wird.

Anweisungen zum Drucken eines XPS-OMS, das ein vollständiges XPS-Dokument enthält, finden Sie unter [Drucken eines vollständigen XPS-OMS](#print-a-complete-xps-om). Um ein XPS-Dokument zu enthalten, muss ein XPS-OM die unter [Erstellen eines leeren XPS-Maps](create-a-blank-xps-om.md)aufgeführten Elemente enthalten.

Anweisungen zum Drucken eines XPS-OMS, das jeweils nacheinander erstellt oder verarbeitet wird, finden Sie unter [inkrementelles Drucken eines XPS-OM](#incrementally-print-an-xps-om).

Bevor Sie diese Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

In diesem Thema erfahren Sie, wie Sie die folgenden Aufgaben ausführen:

-   [Drucken eines vollständigen XPS-OMS](#print-a-complete-xps-om)
-   [Inkrementelles Drucken eines XPS-OM](#incrementally-print-an-xps-om)
-   [Zugehörige Themen](#related-topics)

## <a name="print-a-complete-xps-om"></a>Drucken eines vollständigen XPS-OMS

Wenn ein XPS-OM ein vollständiges XPS-Dokument enthält, kann die " [**Write**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) "-Methode der [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) -Schnittstelle den Inhalt des XPS-OMS an einen Drucker oder eine Druck Warteschlange senden.

Um zu ermitteln, wann der Druckauftrag abgeschlossen wurde, erstellen Sie ein Ereignis handle, wie im folgenden Beispiel gezeigt.


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



So drucken Sie ein vollständiges XPS-om:

1.  Erstellen Sie einen neuen Druckauftrags Datenstrom, indem Sie [**startxpsprintjob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)aufrufen.
2.  Senden Sie den Inhalt des XPS-OMS in den Stream, indem Sie die Methode " [**Write-tostream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) " des Pakets aufrufen.
3.  Schließen Sie den Druckauftrags Datenstrom, indem Sie die **Close** -Methode des Streams aufrufen.
4.  Warten Sie, bis der Druckauftrag signalisiert hat, dass er abgeschlossen wurde.
5.  Überprüfen Sie den Abschluss Status.
6.  Schließen und Freigeben von Ressourcen.


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



## <a name="incrementally-print-an-xps-om"></a>Inkrementelles Drucken eines XPS-OM

Sie können die Dokument Komponenten eines XPS OM inkrementell an einen Drucker Auftrag senden, indem Sie einen XPS-Druckauftrags Datenstrom erstellen und die einzelnen Dokument Komponenten nacheinander an den Druckauftrags Datenstrom übergeben. Die Reihenfolge, in der die Dokument Komponenten gesendet werden, bestimmt, wie diese im fertigen Dokument angezeigt werden. Daher muss die Dokument Komponenten ordnungsgemäß organisiert werden, bevor ein Programm den Code in diesem Beispiel abrufen kann.

Bevor Sie XPS OM-Schnittstellen verwenden, initialisieren Sie com im Thread, wie im folgenden Beispielcode gezeigt.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Erstellen Sie ein Ereignis handle, wie im folgenden Beispielcode gezeigt, um den Abschluss des Druckauftrags zu überwachen.


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



Erstellen Sie einen neuen Druckauftrags Datenstrom und einen neuen paketwriter. Übergeben Sie die einzelnen Dokument Komponenten an die entsprechenden paketwriter-Methoden in derselben Reihenfolge, in der Sie im fertigen Dokument angezeigt werden.

Starten Sie jedes Dokument neu, und fügen Sie ihm Seiten hinzu. Nachdem Sie alle Dokument Komponenten an den Druckauftrags Datenstrom übergeben haben, schließen Sie den Stream, warten Sie, bis der Druckauftrag abgeschlossen ist, und schließen Sie dann offene Ressourcen.

1.  Erstellen Sie einen neuen Druckauftrags Datenstrom, indem Sie [**startxpsprintjob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)aufrufen.
2.  Erstellen Sie einen Teil-URI für den FixedDocumentSequence-Teil.
3.  Erstellen Sie einen neuen paketwriter im Druckauftrags Datenstrom.
4.  Für jedes Dokument, das geschrieben werden soll:
    1.  Erstellen Sie einen neuen Teil-URI für den FixedDocument-Teil.
    2.  Startet ein neues Dokument im paketwriter.
    3.  Erstellen Sie für jede Seite im aktuellen Dokument einen Teil-URI für den FixedPage-Teil, und fügen Sie die Seite dem paketwriter hinzu.
5.  Nachdem dem paketwriter alle Seiten hinzugefügt wurden, schließen Sie ihn.
6.  Schließen Sie den Druckauftrags Datenstrom.
7.  Warten Sie, bis der Druckauftrag vollständig ausgeführt wurde.
8.  Überprüfen Sie den Abschluss Status.
9.  Schließen und freigeben offener Ressourcen.


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



Wenn das Programm die Dokument Komponenten inkrementell schreibt, wie in diesem Beispiel gezeigt, muss es die Teilnamen für jeden Dokument Teil generieren, der an den Druckauftrags Datenstrom gesendet wird. Im vorangehenden Beispiel wird der FixedDocumentSequence-Teil-URI aus einer statischen Zeichenfolge erstellt, da nur ein solcher Teil im XPS-Dokument vorhanden ist. Der URI jedes FixedPage-und FixedDocument-Teils muss innerhalb des XPS-Dokuments eindeutig sein. Wenn Sie den Teil-URI mit dem Index dieser Komponenten verwenden, können Sie sicherstellen, dass die resultierende URI-Zeichenfolge innerhalb des XPS-Dokuments eindeutig ist.


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



Weitere Informationen zur Struktur eines XPS-Dokuments finden Sie in der [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Schreiben eines XPS-om in ein XPS-Dokument](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**Iopcparamei**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**Ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Ixpsprintjob**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[**Ixpsprintjobstream**](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[**Startxpsprintjob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren eines XPS-OMS](xps-object-model-initialization.md)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
