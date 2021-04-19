---
description: Die ixpsompackagewriter-Schnittstelle erstellt eine XPS-Dokument Datei, in die Anwendungen den Inhalt der ixpsompage-Schnittstellen eines XPS-OMS schreiben können.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Verwenden der ixpsompackagewriter-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8a34a0538ff09cc050ac287d5314be93f0da8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362663"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Verwenden der ixpsompackagewriter-Schnittstelle

Die [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle erstellt eine XPS-Dokument Datei, in die Anwendungen den Inhalt der [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) -Schnittstellen eines XPS-OMS schreiben können. Die [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle ist besonders nützlich, wenn Dokumentinhalte sequenziell verarbeitet oder erstellt werden. Im Gegensatz zu den Methoden " [**Write**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) " und " [**Write-to Stream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) " der [**ixpsompackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) -Schnittstelle, damit die **ixpsompackagewriter** -Schnittstelle verwendet werden kann, muss weder das gesamte "FixedDocument" noch "FixedDocumentSequence" abgeschlossen werden.

## <a name="overview"></a>Übersicht

Die [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle schreibt jeweils eine Seite von der ersten Seite eines XPS-Dokuments in die letzte Seite. Die-Schnittstelle kann verwendet werden, um einfache XPS-Dokument Dateien und auch komplexe XPS-Dokument Dateien zu erstellen, die mehr als ein FixedDocument in der FixedDocumentSequence enthalten. In komplexen XPS-Dokument Dateien werden fixeddocuments auch nacheinander erstellt, beginnend mit dem ersten FixedDocument in FixedDocumentSequence. Die **ixpsompackagewriter** -Schnittstelle unterstützt nicht die Erstellung von Dokument Inhalten in zufälliger Reihenfolge. Verwenden Sie diese z. b., um einen sequenziellen Bericht zu erstellen oder um die Verarbeitung in einem Gerätetreiber Filter auszuführen, bei dem der Inhalt des Dokuments nacheinander an den Treiber übertragen wird.

## <a name="terminology-review"></a>Überprüfung der Terminologie

Eine *XPS-Dokument Datei* ist ein OPC-Paket (Open Packaging Conventions), das der XML Paper Specification entspricht. Aus technischer Sicht erstellt die [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle also ein *OPC-Paket*, aber es ist ein OPC-Paket, das der XML Paper Specification entspricht. Aus diesem Grund werden die Begriffe *XPS-Dokument* und- *Paket* in Diskussionen über XPS-Dokumente häufig austauschbar verwendet.

Das von der [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle erstellte *Paket* enthält die erforderlichen XPS-Dokument Komponenten: eine FixedDocumentSequence, mindestens ein FixedDocument und mindestens eine FixedPage. "FixedDocumentSequence" wird erstellt, wenn die **ixpsompackagewriter** -Schnittstelle instanziiert wird. Jedes Mal, wenn [**ixpsompackagewriter:: startnewdocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) aufgerufen wird, wird ein FixedDocument-Dokument erstellt, und es wird jedes Mal eine FixedPage erstellt, wenn [**ixpsompackagewriter:: addPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) aufgerufen wird. Da die-Schnittstelle den Dokumentinhalt sequenziell schreibt, fügt die **addPage** -Methode die Seite dem zuletzt erstellten FixedDocument-Dokument hinzu.

## <a name="using-the-ixpsompackagewriter-interface"></a>Verwenden der ixpsompackagewriter-Schnittstelle

Im folgenden Verfahren wird beschrieben, wie eine XPS-Dokument Datei mithilfe der [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle erstellt wird. In der Prozedur wird nicht beschrieben, wie eine [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) -Schnittstelle und deren Inhalt instanziiert wird. Weitere Informationen zu **ixpsompage** und zum Hinzufügen von Inhalt zu einer Seite finden Sie unter [XPS OM-Seiten Schnittstellen](xps-object-model-page-interfaces.md) und in den Themen, die im Abschnitt "Siehe auch" aufgeführt sind.

 **Erstellen eines Dokuments**

1.  Instanziieren Sie eine [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle.

    Dadurch wird eine leere "FixedDocumentSequence" im Paket erstellt.

    -   Wenn Sie ein XPS-Dokument in einer Datei erstellen möchten, rufen Sie [**ixpsomobjectfactory:: conatepackageschreiteronfile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile)auf.
    -   Um ein XPS-Dokument in einem Stream zu erstellen, rufen Sie [**ixpsomobjectfactory:: anatepackageschreiteronstream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream)auf.

2.  Starten Sie ein neues Dokument im Paket, indem Sie [**ixpsompackagewriter:: startnewdocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)aufrufen.

    Bevor Sie eine Seite hinzufügen, können Sie [**ixpsompackagewriter:: startnewdocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) aufrufen, um der in Schritt 1 erstellten FixedDocumentSequence ein FixedDocument hinzuzufügen.

3.  Inhalt hinzufügen.
    -   Um dem Dokument eine neue FixedPage hinzuzufügen, wenden Sie [**ixpsompackagewriter:: addPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage)an, und übergeben Sie dabei einen Zeiger auf die [**ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) -Schnittstelle mit dem Inhalt der FixedPage, die Sie hinzufügen möchten.
    -   Um ein neues FixedDocument in der FixedDocumentSequence-Sequenz zu erstellen, rufen Sie [**ixpsompackagewriter:: startnewdocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)auf.
4.  Schließen Sie das Paket und seinen Inhalt, indem Sie [**ixpsompackagewriter:: Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close)aufrufen.

## <a name="advanced-features"></a>Erweiterte Funktionen

Die Methoden der [**ixpsompackagewriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) -Schnittstelle unterstützen auch das Hinzufügen von Ressourcen, Miniaturansichten und Druck Tickets. Diese Dokument Komponenten können auf den Ebenen "Package", "FixedDocumentSequence", "FixedDocument" und "FixedPage" hinzugefügt werden. Weitere Informationen zum Verwenden dieser Schnittstelle zum Drucken finden Sie unter [Drucken eines XPS OM](print-an-xps-om.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der XPS Digital-Signatur-API](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[XPS-Schnittstellen für Schnittstellen](xps-object-model-page-interfaces.md)
</dt> <dt>

[Navigieren im XPS-OM](navigate-the-xps-om.md)
</dt> <dt>

[Arbeiten mit XPS OM-Canvas und visuellen Schnittstellen](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Arbeiten mit XPS-OM-Pfad Schnittstellen](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Arbeiten mit XPS OM-Text, Grafiken und Bild Schnittstellen](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Schnittstellen für XPS-OM-Druck Tickets](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**Ixpsomthumbnailgenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



