---
description: OpenXPS ist das Open XML Paper Specification-Format für Dokumente und basiert auf der ECMA-Standardspezifikation (European Makers Association).
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: App-Unterstützung für OpenXPS-Druck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c939b954842bbdfe2bb018c25e96278b792397181c6f1e7aba1e9afb20207e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868583"
---
# <a name="app-support-for-openxps-printing"></a>App-Unterstützung für OpenXPS-Druck

OpenXPS ist das Open XML Paper Specification-Format für Dokumente und basiert auf der ECMA-Standardspezifikation (European Computer Manufacturers Association).

Windows 8 bietet vollständige Unterstützung für OpenXPS-Druck über das v4-Druckertreibermodell, und bietet auch weiterhin Unterstützung für das Microsoft XPS-Format. Und dieses Thema konzentriert sich auf den Teil dieser Unterstützung, der für Windows Anwendungsentwickler relevant ist. Informationen zu den Treiberanforderungen für die OpenXPS-Unterstützung finden Sie unter [Treiberunterstützung für OpenXPS.](/windows-hardware/drivers/print/printer-driver-overview)

## <a name="sending-xps-data-to-the-print-system"></a>Senden von XPS-Daten an das Drucksystem

Es wird empfohlen, [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) zum Senden aller XPS-Druckaufträge an das Drucksystem zu verwenden. **IPrintDocumentPackageTarget** akzeptiert das XPS-Objektmodell (OM) ohne Serialisierung und trägt so zur Verbesserung der Gesamtleistung bei.

Hier ist eine kurze Zusammenfassung der **IPrintDocumentPackageTarget-Schnittstelle:**

-   Diese Schnittstelle unterstützt das Drucken von angepassten Lösungen sowie von Desktopanwendungen.

-   Für Desktop-Apps kann dies anstelle von [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1)verwendet werden.

-   Verfügbar auf Windows 7 mit Service Pack 1 (SP1) + Plattformupdate und Windows 8.

-   Schließen Sie *DocumentTarget.h* in Projekte ein, um diese APIs zu verwenden.

Anwendungen, die OpenXPS-Dokumente nutzen, sollten beachten, dass der MIME-Typ für OpenXPS wie folgt lautet:

<dl> \\Anwendungsoxps  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>Senden von OpenXPS-Daten an die XPS-Druck-API

Spezifisch für OpenXPS akzeptiert XPS OM sowohl MSXPS als auch OpenXPS und stellt Methoden für die Konvertierung und Serialisierung in beide Formate bereit. Dadurch können Anwendungsentwickler bei Bedarf vom Zieltreiber unabhängig sein. Dies bedeutet auch, dass App-Entwickler Druckaufträge immer als XPS OM an StartXpsPrintJob1 oder IDocumentPackageTarget übermitteln können, da sie wissen, dass das Drucksystem alle erforderlichen Konvertierungen verarbeitet.

Natürlich verbessert das Verhindern der Konvertierung zwischen XPS-Formaten die End-to-End-Leistung. In der Anwendung kann der Entwickler den folgenden Registrierungsschlüssel überprüfen, um das bevorzugte XPS-Format des Zieldrucktreibers zu ermitteln:

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

Sobald das bevorzugte XPS-Format bestimmt wurde, kann die Anwendung XPS OM-Objekte bereitstellen, die keine Konvertierung erfordern. Besonders zu beachten ist die Verwendung von HD Photo in MSXPS und JPEGXR in OpenXPS. Die Konvertierung von JPEGXR in HD Photo ist relativ einfach, da der Hauptunterschied bei dieser Konvertierung darin besteht, dass HD Photo 4 Steuerbits ignoriert, die JPEGXR erfordert. Die Konvertierung von HD Photo in JPEGXR erfordert jedoch, dass das gesamte Bild neu codiert wird, um die erforderlichen Steuerbits zu generieren. Daher wird durch die Bereitstellung von JPEGXR-Bildern für Bilder mit hoher Auflösung die Kompatibilität mit OpenXPS sichergestellt und die Konvertierungskosten des Bilds für MSXPS minimiert.

Der *Header Xpsobjectmodel \_ 1.h* definiert die zusätzlichen APIs und Objekte für OpenXPS. Und die IXpsOMObjectFactory1-Schnittstelle stellt zusätzliche Methoden für die Bildkonvertierung bereit. Dies ist die Syntax:


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



Windows 8 stellt die folgenden neuen und aktualisierten Enumerationen bereit.

Neue Enumeration:

<dl>

[**\_XPS-DOKUMENTTYP \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

Aktualisierte Enumeration

<dl>

[**\_XPS-IMAGETYP \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

Mit den neuen GetDocumentType-Methoden kann eine Anwendung das XPS-Format von Dokumenten bestimmen. Diese sind in [**IXpsOMObjectFactory1,**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1) [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)und [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1)verfügbar. Im Folgenden finden Sie eine Liste der Methoden.

<dl>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1::GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1::GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

Windows 8 stellt die folgenden neuen Fehlercodes zur Unterstützung von OpenXPS bereit:

<dl> NICHT ÜBEREINSTIMMENDER XPS \_ \_ \_ E-NAMESPACE. <dl> Dieser Fehler wird zurückgegeben, wenn ein nicht übereinstimmender Namespace vorhanden ist.  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> Dieser Fehler wird zurückgegeben, wenn MSXPS absolute URIs in internen Verweisen verwendet oder versucht, interne Verweise zum Serialisieren im Stream zu verwenden. Das liegt daran, dass XPS OM relative URIs generiert. Obwohl MSXPS sowohl relative als auch absolute URIs unterstützt, erfordert OpenXPS relative URIs.  
</dl> </dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Treiberunterstützung für OpenXPS](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1::GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1::GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**\_XPS-DOKUMENTTYP \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**\_XPS-IMAGETYP \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
