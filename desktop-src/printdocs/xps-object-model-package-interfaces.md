---
description: Die Paket Schnittstellen stellen die oberste Ebene des XPS-OMS dar, die einer XPS-Dokument Datei entspricht.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: XPS-OM-Paket Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863916"
---
# <a name="xps-om-package-interfaces"></a>XPS-OM-Paket Schnittstellen

Die Paket Schnittstellen stellen die oberste Ebene des XPS-OMS dar, die einer XPS-Dokument Datei entspricht. Diese Schnittstellen enthalten Methoden, die ein XPS-om in ein XPS-Dokument oder einen XPS-Stream Serialisieren und ein XPS-Paket deserialisieren, um ein XPS-OM zu erstellen, das einem Programm den Zugriff auf den Inhalt eines Dokuments ermöglicht.



| Schnittstellen Name                                                  | Logische untergeordnete Schnittstellen                                                                                                            | BESCHREIBUNG                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**Ixpsomcoreproperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Das gesamte XPS-OM, das dem Paket entspricht, das das XPS-Dokument enthält.<br/> |
| [**Ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | Keine<br/>                                                                                                                     | Aktiviert die inkrementelle Serialisierung von Dokument Seiten zu einem Paket.<br/>                   |
| [**Ixpsomcoreproperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Keine<br/>                                                                                                                     | Greift auf die Dokument Metadaten zu. <br/>                                                    |



 

## <a name="code-examples"></a>Codebeispiele

Die folgenden Codebeispiele veranschaulichen, wie einige der Paket Schnittstellen von einem Programm verwendet werden. Sofern nicht anders angegeben, sind alle kursiv formatierten Elemente Parameternamen.

-   [Lesen eines XPS-Dokuments in ein XPS-OM](#read-an-xps-document-into-an-xps-om)
-   [Schreiben eines XPS-Maps in eine XPS-Dokument Datei](#write-an-xps-om-to-an-xps-document-file)
-   [Zugreifen auf die Dokument Sequenz des XPS-OMS](#access-the-document-sequence-of-the-xps-om)
-   [Zugreifen auf die coreproperties des Dokuments](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Lesen eines XPS-Dokuments in ein XPS-OM

In einem vorhandenen XPS-Dokument, dessen Dateiname in *xpsdocumentfilename* gespeichert ist, wird in diesem Codebeispiel ein XPS-OM erstellt, auf das von *xpspackage* verwiesen wird.


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



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Schreiben eines XPS-Maps in eine XPS-Dokument Datei

Im folgenden Codebeispiel wird das XPS-OM geschrieben, auf das von *xpspackage* verwiesen wird. Im Beispiel wird ein XPS-Dokument in der Datei erstellt, deren Name in *filename* gespeichert ist.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Zugreifen auf die Dokument Sequenz des XPS-OMS

Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) -Schnittstelle abgerufen, die die Dokument Sequenz des durch *xpspackage* dargestellten XPS-OMS enthält.


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



### <a name="access-the-documents-coreproperties"></a>Zugreifen auf die coreproperties des Dokuments

Im folgenden Codebeispiel wird ein Zeiger auf die [**ixpsomcoreproperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) -Schnittstelle abgerufen, sodass das Programm auf den Inhalt des coreproperties-Teils zugreifen kann. Im Beispiel wird davon ausgegangen, dass das Dokument in ein XPS-OM gelesen wurde, das durch *xpspackage* dargestellt wird.


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

[Verwenden der ixpsompackagewriter-Schnittstelle](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[Navigieren im XPS-OM](navigate-the-xps-om.md)
</dt> <dt>

[**Ixpsomdocumentsequence-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Ixpsompackage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Ixpsompackagewriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Ixpsomcoreproperties-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




