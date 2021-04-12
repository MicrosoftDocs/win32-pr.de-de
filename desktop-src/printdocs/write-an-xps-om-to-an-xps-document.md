---
description: Beschreibt, wie der Inhalt eines XPS-om in einem Programm in eine XPS-Dokument Datei geschrieben wird.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Schreiben eines XPS-om in ein XPS-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216868"
---
# <a name="write-an-xps-om-to-an-xps-document"></a>Schreiben eines XPS-om in ein XPS-Dokument

Beschreibt, wie der Inhalt eines XPS-om in einem Programm in eine XPS-Dokument Datei geschrieben wird.

Wenn ein Programm über ein XPS-OM verfügt, das ein umfassendes Dokument enthält, kann das Programm das XPS-om in eine Datei als XPS-Dokument schreiben, indem die Methode " [**Write-ToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) " der [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) -Schnittstelle aufgerufen wird.

Bevor Sie diese Codebeispiele in einem Programm verwenden, lesen Sie den Haftungsausschluss in [Allgemeine XPS-Dokument Programmieraufgaben](common-xps-document-tasks.md).

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>Schreiben eines kompletten XPS-om in ein XPS-Dokument

Nachdem Sie den Inhalt eines XPS-Maps festgelegt haben, können Sie das XPS-OM als XPS-Dokument in einer Datei speichern, indem Sie die Methode " [**Write-ToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) " der [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) -Schnittstelle aufrufen.


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
> Wenn Sie ein XPS-om in eine Datei oder einen Stream schreiben, wird nicht automatisch eine Miniaturansicht für das XPS-Dokument erstellt. Verwenden Sie zum Erstellen einer Miniaturansicht des XPS-Dokuments die [**ixpsomthumbnailgenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) -Schnittstelle.

 

## <a name="incrementally-writing-an-xps-document"></a>Inkrementelles Schreiben eines XPS-Dokuments

Die [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle kann verwendet werden, um die Teile eines XPS-Dokuments inkrementell zu schreiben; beispielsweise, wenn die Dokument Teile nacheinander erstellt oder verarbeitet werden.

> [!Note]  
> Wenn Sie ein XPS-om in eine Datei oder einen Stream schreiben, wird nicht automatisch eine Miniaturansicht für das XPS-Dokument erstellt. Verwenden Sie zum Erstellen einer Miniaturansicht des XPS-Dokuments die [**ixpsomthumbnailgenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) -Schnittstelle.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Drucken eines XPS-OM](print-an-xps-om.md)
</dt> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**Iopcparamei**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**Ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Ixpsomthumbnailgenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Initialisieren eines XPS-OMS](xps-object-model-initialization.md)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
