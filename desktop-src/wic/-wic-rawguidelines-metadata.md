---
description: Metadatenunterstützung
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Metadatenunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa706c3529a6c5efa0e453f7f3e181a6d6a82e0523d9ea3610dc992434856c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667337"
---
# <a name="metadata-support"></a>Metadatenunterstützung

RAW-Formate sollten auch die gängigen Lese- und Schreibszenarien für Metadaten für Bilder in Windows unterstützen. Microsoft hat eine Reihe nativer Metadatenanbieter für exchangeable Image file (EXIF), International Press Telecommunications Council (IPTC) und XMP-Metadaten (Extensible Metadata Platform) entwickelt, die derzeit nur für TIFF- und JPEG-Container aufgerufen werden. Wenn das RAW-Image in einem dieser Containerformate gespeichert wird, wird empfohlen, die Windows integrierten Metadatenanbieter zu verwenden. Der Codecautor ist jedoch dafür verantwortlich, dies ordnungsgemäß zu konfigurieren. Für RAW-Dateien, die nicht auf einem TIFF-Container basieren, kann es erforderlich sein, EXIF-, IPTC- oder XMP-Writer zu implementieren, da die integrierten Reader und Writer erwarten, dass die Daten den Layoutspezifikationen EXIF, IPTC und XMP auf dem Datenträger entsprechen. Codecautoren können auch eigene Anbieter für benutzerdefinierte Metadaten implementieren.

Aufgrund der Architektur von Windows Imaging Component (WIC) können Metadatenwriter nur über eine Instanz eines Imageencoders aufgerufen werden. Daher sollten RAW-Formatbesitzer mindestens einen [**WICRawParameterSet.WICAutoAdjustedParameterSet-Encoder**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) "stub" erstellen, auch wenn die tatsächliche Codierung von Pixeln in ein RAW-Format nicht implementiert ist. Der Codecautor muss die richtigen Metadatenhandler aufrufen:

-   [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) für den Decoder und den Framedecoder nach Bedarf.
-   [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) für den Encoder und den Frameencoder nach Bedarf.

Um alle erwarteten Szenarien bei der Imageerstellung von Anwendungen in Windows Vista zu unterstützen, wird empfohlen, dass Codecanbieter mindestens Folgendes unterstützen:

-   EXIF-Lesedauer
-   Partieller EXIF-Schreibvorgang (um Aktualisierungen der Erfassung von Datum und Uhrzeit zu ermöglichen)
-   XMP-Lese- und -Schreibzugriff (einschließlich optional IPTC Core für XMP)
-   IPTC IIMv4: Lesen und Schreiben

Der Großteil des Metadatenzugriffs (Sowohl Lesen als auch Schreiben) in Windows Vista erfolgt über die [**IWICMetadataQueryReader-**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) oder [**IWICMetadataQueryWriter-Schnittstelle.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) Daher müssen RAW-Codecautoren die [**Methoden IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode):: GetMetadataQueryReader und [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) und IWICBitmapFrameEncode ::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) implementieren, um an den Windows Vista-Metadaten teilzunehmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guidelines for Camera RAW Image Formats](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



