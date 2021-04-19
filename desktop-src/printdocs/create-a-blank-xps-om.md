---
description: In diesem Thema wird beschrieben, wie ein leeres XPS-OM erstellt wird.
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: Erstellen eines leeren XPS-OMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0588fc11deb4b3d980e978dfe8a5370bc170d506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373034"
---
# <a name="create-a-blank-xps-om"></a>Erstellen eines leeren XPS-OMS

In diesem Thema wird beschrieben, wie ein leeres XPS-OM erstellt wird. Es zeigt die Codebeispiele, die veranschaulichen, wie ein XPS-OM zum Erstellen der Dokumentstruktur eines XPS-Dokuments mit einer leeren Seite verwendet wird.

Um als XPS-Dokument gespeichert zu werden, sind für das XPS-OM mindestens die folgenden Komponenten erforderlich:

-   Ein [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , das das XPS-Dokument Paket beschreibt.
-   Eine [**ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , die das Framework des Paket Inhalts enthält.
-   Ein [**ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) , das das Framework eines Dokuments innerhalb des Pakets enthält.
-   Eine [**ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) , die die Sammlung der Seiten im Dokument enthält.
-   Eine [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) , die eine leere Seite enthält.

Wenn diese Schnittstellen verwendet werden, enthält das XPS-OM ein Dokument, das eine leere Seite enthält. Zum Erstellen dieses Dokuments in einem XPS-OM muss das Programm zuerst die einzelnen Komponenten erstellen und dann miteinander verknüpfen.

Bevor Sie die folgenden Codebeispiele verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

## <a name="code-examples"></a>Codebeispiele

Im folgenden Codebeispiel wird davon ausgegangen, dass die in [Initialisieren eines XPS-OM](xps-object-model-initialization.md)beschriebene Initialisierung erfolgreich war.


```C++
    // Declare the variables used in this section.
    HRESULT                       hr = S_OK;
    IOpcPartUri                   *opcPartUri = NULL;
    IXpsOMPackage                 *xpsPackage = NULL;
    IXpsOMDocumentSequence        *xpsFDS = NULL;
    IXpsOMDocumentCollection      *fixedDocuments = NULL;
    IXpsOMDocument                *xpsFD = NULL;
    IXpsOMPage                    *xpsPage = NULL;
    IXpsOMPageReferenceCollection *pageRefs = NULL;
    IXpsOMPageReference           *xpsPageRef = NULL;
    // These values are set outside of this code example.
    XPS_SIZE pageSize = {width, height}; 
    
    // Create the package.
    hr = xpsFactory->CreatePackage( &xpsPackage );

    // Create the URI for the fixed document sequence part and then  
    //  create the fixed document sequence
    hr = xpsFactory->CreatePartUri( 
        L"/FixedDocumentSequence.fdseq", &opcPartUri );
    hr = xpsFactory->CreateDocumentSequence( opcPartUri, &xpsFDS );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create the URI for the document part and then create the document.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/FixedDocument.fdoc", &opcPartUri );
    hr = xpsFactory->CreateDocument( opcPartUri, &xpsFD );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a blank page.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/Pages/1.fpage", &opcPartUri );
    hr = xpsFactory->CreatePage(
        &pageSize,                  // Page size
        L"en-US",                   // Page language
        opcPartUri,                 // Page part name
        &xpsPage);                
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a page reference for the page.
    hr = xpsFactory->CreatePageReference( &pageSize, &xpsPageRef );

    // Add the fixed document sequence to the package.
    hr = xpsPackage->SetDocumentSequence( xpsFDS );

    // Get the document collection of the fixed document sequence
    //  and then add the document to the collection.
    hr = xpsFDS->GetDocuments( &fixedDocuments );
    hr = fixedDocuments->Append( xpsFD );

    // Get the page reference collection from the document
    //  and add the page reference and blank page.
    hr = xpsFD->GetPageReferences( &pageRefs );
    hr = pageRefs->Append( xpsPageRef );
    hr = xpsPageRef->SetPage( xpsPage );

    // Release interface pointer
    if (NULL != xpsPage) xpsPage->Release();
    if (NULL != pageRefs) pageRefs->Release();
    if (NULL != fixedDocuments) fixedDocuments->Release();
    if (NULL != xpsPageRef) xpsPageRef->Release();
    if (NULL != xpsFD) xpsFD->Release();
    if (NULL != xpsFDS) xpsFDS->Release();
    if (NULL != xpsPackage) xpsPackage->Release();

```



## <a name="best-practices"></a>Bewährte Methoden

Nachdem Sie eine [**iopcsamturi**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) -Schnittstelle zum Erstellen einer Komponente (z. b. nach dem Aufrufen der **createDocument** -Methode im Codebeispiel) verwendet haben, geben Sie den Zeiger auf diese Schnittstelle –, es sei denn, Sie benötigen Sie für einen weiteren Aufruf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Navigieren im XPS-OM](navigate-the-xps-om.md)
</dt> <dt>

[Schreiben von Text in ein XPS-OM](write-text-to-an-xps-om.md)
</dt> <dt>

[Zeichnen von Grafiken in einem XPS-OM](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Platzieren von Bildern in einem XPS-OM](place-images-in-an-xps-om.md)
</dt> <dt>

**Auf dieser Seite verwendet**
</dt> <dt>

[**Iopcparamei**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**Ixpsomobjectfactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Ixpsomdocumentcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**Ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**XPS- \_ Größe**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren eines XPS-OMS](xps-object-model-initialization.md)
</dt> <dt>

[Verpacken von APIs](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
