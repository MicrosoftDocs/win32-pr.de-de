---
description: Die IXpsOMPackageWriter-Schnittstelle erstellt eine XPS-Dokumentdatei, in die Anwendungen den Inhalt der IXpsOMPage-Schnittstellen einer XPS OM schreiben können.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Verwenden der IXpsOMPackageWriter-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a4437f939821b826fa0d5c30407777b7d44c5d03c236f4ef850d52145b4f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098702"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Verwenden der IXpsOMPackageWriter-Schnittstelle

Die [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) erstellt eine XPS-Dokumentdatei, in die Anwendungen den Inhalt der [**IXpsOMPage-Schnittstellen**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) einer XPS OM schreiben können. Die [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) ist besonders nützlich, wenn Dokumentinhalte sequenziell verarbeitet oder erstellt werden. Im Gegensatz zu den [**WriteToFile-**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) und [**WriteToStream-Methoden**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) der [**IXpsOMPackage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) muss für die **IXpsOMPackageWriter-Schnittstelle** weder das gesamte FixedDocument noch fixedDocumentSequence verwendet werden.

## <a name="overview"></a>Übersicht

Die [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) schreibt jeweils eine Seite von der ersten Seite eines XPS-Dokuments bis zur letzten. Die -Schnittstelle kann verwendet werden, um einfache XPS-Dokumentdateien und auch komplexe XPS-Dokumentdateien zu erstellen, die mehr als ein FixedDocument in fixedDocumentSequence enthalten. In komplexen XPS-Dokumentdateien werden die FixedDocuments ebenfalls nacheinander erstellt, beginnend mit dem ersten FixedDocument in FixedDocumentSequence. Die **IXpsOMPackageWriter-Schnittstelle** unterstützt die Erstellung von Dokumentinhalten nicht in zufälliger Reihenfolge. Verwenden Sie ihn beispielsweise, um einen sequenziellen Bericht zu erstellen oder die Verarbeitung in einem Gerätetreiberfilter durchzuführen, in dem der Dokumentinhalt nacheinander an den Treiber übertragen wird.

## <a name="terminology-review"></a>Terminologieüberprüfung

Eine *XPS-Dokumentdatei* ist ein OPC-Paket (Open Packaging-Konventionen), das dem XML Paper Specification entspricht. Technisch gesehen erstellt die [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) ein *OPC-Paket,* aber es ist ein OPC-Paket, das dem XML Paper Specification entspricht. Aus diesem Grund werden in Diskussionen zu XPS-Dokumenten die Begriffe *XPS-Dokument* und *-Paket* häufig austauschbar verwendet.

Das von der [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) erstellte *Paket* enthält die erforderlichen XPS-Dokumentkomponenten: FixedDocumentSequence, mindestens ein FixedDocument und mindestens eine FixedPage. FixedDocumentSequence wird erstellt, wenn die **IXpsOMPackageWriter-Schnittstelle** instanziiert wird. Ein FixedDocument wird jedes Mal erstellt, wenn [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) aufgerufen wird, und bei jedem Aufruf von [**IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) wird eine FixedPage erstellt. Da die Schnittstelle den Dokumentinhalt sequenziell schreibt, fügt die **AddPage-Methode** die Seite dem zuletzt erstellten FixedDocument hinzu.

## <a name="using-the-ixpsompackagewriter-interface"></a>Verwenden der IXpsOMPackageWriter-Schnittstelle

Im folgenden Verfahren wird beschrieben, wie Sie eine XPS-Dokumentdatei mithilfe der [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) erstellen. Die Prozedur beschreibt nicht, wie eine [**IXpsOMPage-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) und deren Inhalt instanziiert werden. Weitere Informationen zu **IXpsOMPage** und zum Hinzufügen von Inhalten zu einer Seite finden Sie unter [XPS OM-Seitenschnittstellen](xps-object-model-page-interfaces.md) und in den Themen, die im Abschnitt Siehe auch aufgeführt sind.

 **Erstellen eines Dokuments**

1.  Instanziieren Sie eine [**IXpsOMPackageWriter-Schnittstelle.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)

    Dadurch wird eine leere FixedDocumentSequence im Paket erstellt.

    -   Um ein XPS-Dokument in einer Datei zu erstellen, rufen [**Sie IXpsOMObjectFactory::CreatePackageWriterOnFile auf.**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile)
    -   Um ein XPS-Dokument in einem Stream zu erstellen, rufen [**Sie IXpsOMObjectFactory::CreatePackageWriterOnStream auf.**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream)

2.  Starten Sie ein neues Dokument im Paket, indem [**Sie IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)aufrufen.

    Rufen Sie vor dem Hinzufügen einer Seite [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) auf, um dem in Schritt 1 erstellten FixedDocumentSequence ein FixedDocument hinzuzufügen.

3.  Fügen Sie Inhalt hinzu.
    -   Um dem Dokument eine neue FixedPage hinzuzufügen, rufen [**Sie IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage)auf und übergeben ihm einen Zeiger auf die [**IXpsOMPage-Schnittstelle,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) die den Inhalt der FixedPage enthält, die Sie hinzufügen möchten.
    -   Um ein neues FixedDocument in FixedDocumentSequence zu erstellen, rufen [**Sie IXpsOMPackageWriter::StartNewDocument auf.**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)
4.  Schließen Sie das Paket und seinen Inhalt, indem [**Sie IXpsOMPackageWriter::Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close)aufrufen.

## <a name="advanced-features"></a>Erweiterte Funktionen

Die Methoden der [**IXpsOMPackageWriter-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) unterstützen auch das Hinzufügen von Ressourcen, Miniaturansichten und Drucktickets. Diese Dokumentkomponenten können auf der Paket-, FixedDocumentSequence-, FixedDocument- und FixedPage-Ebene hinzugefügt werden. Weitere Informationen zur Verwendung dieser Schnittstelle zum Drucken finden Sie unter [Drucken eines XPS OM.](print-an-xps-om.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der XPS Digital-Signatur-API](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[XPS OM-Seitenschnittstellen](xps-object-model-page-interfaces.md)
</dt> <dt>

[Navigieren im XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[Arbeiten mit XPS OM Canvas und visuellen Schnittstellen](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Arbeiten mit XPS OM-Pfadschnittstellen](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Arbeiten mit XPS OM-Schnittstellen für Text, Grafiken und Bilder](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[XPS OM–Druckticketschnittstellen](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[REFERENZ ZUR XPS-Dokument-API](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



