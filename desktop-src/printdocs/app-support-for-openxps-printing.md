---
description: Openxps ist das Open XML Paper Specification-Format für Dokumente, das auf der Standardspezifikation der Europäischen Verpackungshersteller (ECMA) basiert.
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: App-Unterstützung für openxps-Druck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351658"
---
# <a name="app-support-for-openxps-printing"></a>App-Unterstützung für openxps-Druck

Openxps ist das Open XML Paper Specification-Format für Dokumente, das auf der Standardspezifikation der Europäischen Computer Hersteller Zuordnungen (ECMA) basiert.

Windows 8 bietet vollständige Unterstützung für den openxps-Druck über das V4-Druckertreiber Modell, parallel mit der kontinuierlichen Unterstützung für das Microsoft XPS-Format. Dieses Thema konzentriert sich auf den Teil dieser Unterstützung, der für Entwickler von Windows-Anwendungen relevant ist. Informationen zu den Treiber Anforderungen für openxps-Unterstützung finden Sie unter [Treiberunterstützung für openxps](/windows-hardware/drivers/print/printer-driver-overview).

## <a name="sending-xps-data-to-the-print-system"></a>Senden von XPS-Daten an das Druck System

Es wird empfohlen, dass Sie [**iprintdocumentpackagetarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) verwenden, um alle XPS-Druckaufträge an das Drucksystem zu senden. **Iprintdocumentpackagetarget** akzeptiert das XPS-Objektmodell (OM) ohne Serialisierung und trägt so zur Verbesserung der Gesamtleistung bei.

Im folgenden finden Sie eine kurze Zusammenfassung der **iprintdocumentpackagetarget** -Schnittstelle:

-   Diese Schnittstelle unterstützt das Drucken aus angepassten Lösungen und Desktop Anwendungen.

-   Bei Desktops-apps kann dies anstelle von [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1)verwendet werden.

-   Verfügbar unter Windows 7 mit Service Pack 1 (SP1) + Platt Form Update und Windows 8.

-   Fügen Sie " *documenttarget. h* " in Projekte ein, um diese APIs zu verwenden.

Anwendungen, die openxps-Dokumente verwenden, sollten beachten, dass der MIME-Typ für openxps wie folgt aussieht:

<dl> Anwendungs- \\ oxps  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>Senden von openxps-Daten an die XPS-Druck-API

Für openxps-spezifisch akzeptiert XPS OM sowohl msxps als auch openxps und stellt Methoden für die Konvertierung und Serialisierung in beide Formate bereit. Dies ermöglicht es Anwendungsentwicklern, bei Bedarf agnostisch des Ziel Treibers zu sein. Dies bedeutet auch, dass App-Entwickler immer Druckaufträge als XPS OM an entweder StartXpsPrintJob1 oder idocumentpackagetarget übermitteln können und dabei wissen, dass das Drucksystem jede erforderliche Konvertierung verarbeitet.

Natürlich wird durch das verhindern der Konvertierung zwischen XPS-Formaten die End-to-End-Leistung verbessert. Der Entwickler kann den folgenden Registrierungsschlüssel aus der Anwendung überprüfen, um das bevorzugte XPS-Format des Ziel Druckertreibers zu ermitteln:

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

Sobald das bevorzugte XPS-Format festgelegt wurde, kann die Anwendung XPS OM-Objekte bereitstellen, für die keine Konvertierung erforderlich ist. Besonders Hinweis ist die Verwendung von HD-Foto in msxps und jpeer-XR in openxps. Die Konvertierung von jpgxr in HD Photo ist relativ einfach, da der Hauptunterschied in dieser Konvertierung darin besteht, dass das HD-Foto vier Steuerungs Bits ignoriert, die von jpeer GXR benötigt werden. Allerdings muss bei der Umstellung von HD-Fotos in jpgxr das gesamte Bild erneut codiert werden, um die erforderlichen Steuerungs Bits zu generieren. Dadurch wird die Kompatibilität mit openxps durch das Bereitstellen von jpeer-XR-Images für hochauflösende Images sichergestellt, und die Konvertierungs Kosten des Images für msxps werden minimiert.

Der *xpsobjectmodel \_ 1. h* -Header definiert die zusätzlichen APIs und Objekte für openxps. Und die IXpsOMObjectFactory1-Schnittstelle stellt zusätzliche Methoden für die Bild Konvertierung bereit. Hier ist die Syntax:


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



Windows 8 bietet die folgenden neuen und aktualisierten Enumerationen.

Neue Enumeration:

<dl>

[**XPS \_ - \_ Dokumenttyp**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

Aktualisierte Enumeration

<dl>

[**XPS \_ - \_ Bildtyp**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

Die neuen GetDocumentType-Methoden ermöglichen es einer Anwendung, das XPS-Format von Dokumenten zu bestimmen. Diese sind in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)und [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1)verfügbar. Im folgenden finden Sie eine Liste der Methoden.

<dl>

[**IXpsOMObjectFactory1:: getdocumenttypefromfile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1:: getdocumenttypefromstream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

Windows 8 bietet die folgenden neuen Fehlercodes für die Unterstützung von openxps:

<dl> nicht \_ \_ übereinstimmender XPS- \_ Namespace. <dl> Dieser Fehler wird zurückgegeben, wenn ein nicht übereinstimmender Namespace vorhanden ist.  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> Dieser Fehler wird zurückgegeben, wenn msxps absolute URIs in internen verweisen verwendet oder versucht, interne Verweise zu verwenden, um im Stream zu serialisieren. Dies liegt daran, dass XPS OM relative URIs generiert. Obwohl msxps sowohl relative als auch absolute URIs unterstützt, erfordert openxps relative URIs.  
</dl> </dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Treiberunterstützung für openxps](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**Iprintdocumentpackagetarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1:: getdocumenttypefromfile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1:: getdocumenttypefromstream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**XPS \_ - \_ Dokumenttyp**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**XPS \_ - \_ Bildtyp**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
