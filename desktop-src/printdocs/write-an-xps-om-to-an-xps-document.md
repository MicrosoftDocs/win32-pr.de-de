---
description: Beschreibt, wie der Inhalt einer XPS OM in ein Programm in eine XPS-Dokumentdatei geschrieben wird.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Schreiben einer XPS OM in ein XPS-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f6ef79f592ad241e54e9a01fb5e4fe72cc41573e75c78f347109cdfb1c6f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098557"
---
# <a name="write-an-xps-om-to-an-xps-document"></a>Schreiben einer XPS OM in ein XPS-Dokument

Beschreibt, wie der Inhalt einer XPS OM in ein Programm in eine XPS-Dokumentdatei geschrieben wird.

Wenn ein Programm über eine XPS OM verfügt, die ein vollständiges Dokument enthält, kann das Programm die XPS OM als XPS-Dokument in eine Datei schreiben, indem die [**WriteToFile-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) der [**IXpsOMPackage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) aufgerufen wird.

Bevor Sie diese Codebeispiele in einem Programm verwenden, lesen Sie den Haftungsausschluss unter [Common XPS Document Programming Tasks (Allgemeine XPS-Dokumentprogrammierungsaufgaben).](common-xps-document-tasks.md)

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>Schreiben einer vollständigen XPS OM in ein XPS-Dokument

Nachdem Sie den Inhalt einer XPS OM festgelegt haben, können Sie die XPS OM in einer Datei als XPS-Dokument speichern, indem Sie die [**WriteToFile-Methode**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) der [**IXpsOMPackage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) aufrufen.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> Das Schreiben einer XPS OM in eine Datei oder einen Stream erstellt nicht automatisch eine Miniaturansicht für das XPS-Dokument. Verwenden Sie die [**IXpsOMThumbnailGenerator-Schnittstelle,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) um eine Miniaturansicht des XPS-Dokuments zu erstellen.

 

## <a name="incrementally-writing-an-xps-document"></a>Inkrementelles Schreiben eines XPS-Dokuments

Die [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) kann verwendet werden, um die Teile eines XPS-Dokuments inkrementell zu schreiben. Beispielsweise, wenn die Dokumentteile nacheinander erstellt oder verarbeitet werden.

> [!Note]  
> Das Schreiben einer XPS OM in eine Datei oder einen Stream erstellt nicht automatisch eine Miniaturansicht für das XPS-Dokument. Verwenden Sie die [**IXpsOMThumbnailGenerator-Schnittstelle,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) um eine Miniaturansicht des XPS-Dokuments zu erstellen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Drucken einer XPS OM](print-an-xps-om.md)
</dt> <dt>

**Wird in diesem Abschnitt verwendet**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren einer XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[REFERENZ ZUR XPS-Dokument-API](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
