---
description: Die Paketschnittstellen stellen die oberste Ebene der XPS OM dar, die einer XPS-Dokumentdatei entspricht.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: XPS OM-Paketschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6732531e3874046bbd174c363db24e304da95b9596b810014abb52a795e720c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886140"
---
# <a name="xps-om-package-interfaces"></a>XPS OM-Paketschnittstellen

Die Paketschnittstellen stellen die oberste Ebene der XPS OM dar, die einer XPS-Dokumentdatei entspricht. Diese Schnittstellen enthalten Methoden, die eine XPS OM in ein XPS-Dokument oder einen XPS-Stream serialisieren und ein XPS-Paket deserialisieren, um eine XPS OM zu erstellen, die einem Programm den Zugriff auf den Inhalt eines Dokuments ermöglicht.



| Schnittstellenname                                                  | Logische untergeordnete Schnittstellen                                                                                                            | BESCHREIBUNG                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Die vollständige XPS OM, die dem Paket entspricht, das das XPS-Dokument enthält.<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | Keine<br/>                                                                                                                     | Aktiviert die inkrementelle Serialisierung von Dokumentseiten in ein Paket.<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Keine<br/>                                                                                                                     | Greift auf die Dokumentmetadaten zu. <br/>                                                    |



 

## <a name="code-examples"></a>Codebeispiele

Die folgenden Codebeispiele veranschaulichen, wie einige der Paketschnittstellen von einem Programm verwendet werden. Sofern nicht anders angegeben, sind alle iterierten Elemente Parameternamen.

-   [Lesen eines XPS-Dokuments in eine XPS OM](#read-an-xps-document-into-an-xps-om)
-   [Schreiben einer XPS OM in eine XPS-Dokumentdatei](#write-an-xps-om-to-an-xps-document-file)
-   [Zugreifen auf die Dokumentsequenz der XPS OM](#access-the-document-sequence-of-the-xps-om)
-   [Zugreifen auf die CoreProperties des Dokuments](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Lesen eines XPS-Dokuments in eine XPS OM

Aus einem vorhandenen XPS-Dokument, dessen Dateiname in *xpsDocumentFilename* gespeichert ist, erstellt dieses Codebeispiel eine XPS OM, auf die *xpsPackage* verweist.


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Schreiben einer XPS OM in eine XPS-Dokumentdatei

Im folgenden Codebeispiel wird die XPS OM geschrieben, auf die *xpsPackage* verweist. Im Beispiel wird ein XPS-Dokument in der Datei erstellt, deren Name in *fileName* gespeichert ist.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Zugreifen auf die Dokumentsequenz der XPS OM

Das folgende Codebeispiel ruft einen Zeiger auf die [**IXpsOMDocumentSequence-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) ab, die die Dokumentsequenz der XPS OM enthält, die durch *xpsPackage* dargestellt wird.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a>Zugreifen auf die CoreProperties des Dokuments

Das folgende Codebeispiel ruft einen Zeiger auf die [**IXpsOMCoreProperties-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) ab, sodass das Programm auf den Inhalt des CoreProperties-Teils zugreifen kann. In diesem Beispiel wird davon ausgegangen, dass das Dokument in eine XPS OM gelesen wurde, die durch *xpsPackage* dargestellt wird.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der IXpsOMPackageWriter-Schnittstelle](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[Navigieren im XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[**IXpsOMDocumentSequence-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPackage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**IXpsOMCoreProperties-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




