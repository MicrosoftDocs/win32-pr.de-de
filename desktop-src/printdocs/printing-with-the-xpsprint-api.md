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
# <a name="how-to-print-with-the-xps-print-api"></a>Gewusst wie: Drucken mit der XPS-Druck-API

In diesem Thema wird beschrieben, wie die [XPS-Druck-API](xpsprint-api.md) zum Drucken aus einer Windows-Anwendung verwendet wird.

Mit der [XPS-Druck-API](xpsprint-api.md) können native Windows-Anwendungen XPS-Dokumente drucken. Eine Anwendung kann ein XPS-Dokument mithilfe der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))erstellen. Das Thema [Allgemeine XPS-Dokument Programmieraufgaben](/previous-versions/windows/desktop/dd316968(v=vs.85)) beschreibt, wie dies zu tun ist. Nachdem ein XPS-Dokument erstellt wurde, kann die Anwendung die XPS-Druck-API verwenden, um Sie zu drucken.

Die Verwendung der [XPS-Druck-API](xpsprint-api.md) zum Drucken eines Dokuments aus einer Anwendung umfasst die folgenden Schritte.

-   [COM-Schnittstelle initialisieren](#initialize-com-interface)
-   [Erstellen eines Abschluss Ereignisses](#create-a-completion-event)
-   [Starten eines XPS-Druckauftrags](#start-an-xps-print-job)
-   [Erstellen einer ixpsompackagewriter-Schnittstelle](#create-an-ixpsompackagewriter-interface)
-   [Schließen Sie die ixpsompackagewriter-Schnittstelle.](#close-the-ixpsompackagewriter-interface)
-   [Schließen Sie den Druckauftrags Datenstrom.](#close-the-print-job-stream)
-   [Auf Abschluss Ereignis warten](#wait-for-the-completion-event)
-   [Freigeben von Ressourcen](#release-resources)

Die [XPS-Druck-API](xpsprint-api.md) erfordert, dass ein XPS-Dokument gedruckt wird. Im folgenden Beispiel wird das XPS-Dokument erstellt, das von der XPS-Druck-API an den Drucker gesendet wird. Es ist auch möglich, ein XPS-Dokument zu erstellen, ohne es mit der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) an einen Drucker zu senden und als XPS-OM zu verwalten oder das XPS-OM als XPS-Dokument zu speichern. Weitere Informationen zur Verwendung von XPS OM finden Sie in der XPS-Dokument-API.

### <a name="initialize-com-interface"></a>COM-Schnittstelle initialisieren

Initialisieren Sie die COM-Schnittstelle, wenn die Anwendung dies noch nicht getan hat.


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



### <a name="create-a-completion-event"></a>Erstellen eines Abschluss Ereignisses

Erstellen Sie ein Abschluss Ereignis, das die [XPS-Druck-API](xpsprint-api.md) verwendet, um die Anwendung zu benachrichtigen, wenn der Druck Spooler das gesamte Dokument von der Anwendung erhalten hat. Die XPS-Druck-API unterstützt auch ein Fortschritts Ereignis, sodass eine Anwendung über andere spoolingaktivitäten informiert werden kann.


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



### <a name="start-an-xps-print-job"></a>Starten eines XPS-Druckauftrags

Starten Sie einen XPS-Druckauftrag durch Aufrufen von [**startxpsprintjob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob). **Startxpsprintjob** gibt einen Datenstrom zurück, in den die Anwendung das zu druckende Dokument sendet.


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



### <a name="create-an-ixpsompackagewriter-interface"></a>Erstellen einer ixpsompackagewriter-Schnittstelle

Erstellen Sie eine [**ixpsompackagewriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle, indem Sie [**ixpsomobjectfactory:: createpackageschreiteronstream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) für den von [**startxpsprintjob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob)zurückgegebenen Stream aufrufen.


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



Starten Sie für jedes Dokument in diesem Druckauftrag ein neues Dokument, und fügen Sie diesem Dokument Seiten hinzu.

### <a name="start-a-new-document"></a>Neues Dokument starten

Startet ein neues Dokument im paketwriter, indem [**ixpsompackagewriter:: startnewdocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)aufgerufen wird. Wenn ein Dokument geöffnet ist, wenn diese Methode aufgerufen wird, wird es geschlossen, und ein neues Dokument wird geöffnet.


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



### <a name="add-a-page"></a>Seite hinzufügen

Wenden Sie [**ixpsompackagewriter:: addPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) an, um die einzelnen Seiten des Dokuments aus der Anwendung in das neue Dokument im paketwriter zu schreiben.

> [!Note]  
> Es wird davon ausgegangen, dass die Seite vor diesem Schritt von der Anwendung erstellt wurde. Weitere Informationen zum Erstellen von Dokument Seiten und zum Hinzufügen von Inhalten finden Sie unter [Allgemeine XPS-Dokument Programmieraufgaben](/previous-versions/windows/desktop/dd316968(v=vs.85)).

 


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



### <a name="close-the-ixpsompackagewriter-interface"></a>Schließen Sie die ixpsompackagewriter-Schnittstelle.

Nachdem alle Dokumente für diesen Druckauftrag geschrieben wurden, können Sie [**ixpsompackagewriter:: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) anrufen, um das Paket zu schließen.


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



### <a name="close-the-print-job-stream"></a>Schließen Sie den Druckauftrags Datenstrom.

Schließen Sie den Druckauftrags Datenstrom, indem Sie [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close)aufrufen, der dem Druck Spooler mitteilt, dass der gesamte Druckauftrag von der Anwendung gesendet wurde.


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



### <a name="wait-for-the-completion-event"></a>Auf Abschluss Ereignis warten

Warten Sie auf das Abschluss Ereignis des Druckauftrags.


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



Nachdem das Abschluss Ereignis signalisiert wurde, können Sie [**getjobstatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) aufrufen, um den Auftragsstatus zu erhalten.


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



### <a name="release-resources"></a>Freigeben von Ressourcen

Wenn ein Auftragsstatus den Abschluss angibt, geben Sie die für diesen Druckauftrag verwendeten Schnittstellen und Ressourcen frei.


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



 

 
