---
description: Metadatenunterstützung
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Metadatenunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351416"
---
# <a name="metadata-support"></a>Metadatenunterstützung

Unformatierte Formate sollten auch allgemeine metadatenlese-und Schreib Szenarien für Images in Windows unterstützen. Microsoft hat eine Reihe von systemeigenen metadatenanbietern für die austauschbare Image Datei (EXIF), den International Press Telecommunications Council (IPTC) und die Extensible Metadata Platform (XMP)-Metadaten entwickelt, die derzeit nur für TIFF-und JPEG-Container aufgerufen werden. Wenn das RAW-Image in einem dieser Containerformate gespeichert wird, wird empfohlen, die integrierten Metadatenanbieter von Windows zu verwenden. Der Codec-Autor ist jedoch dafür verantwortlich, dies ordnungsgemäß zu konfigurieren. Bei unformatierten Dateien, die nicht auf einem TIFF-Container basieren, ist es möglicherweise notwendig, EXIF-, IPTC-oder XMP-Writer zu implementieren, da die integrierten Reader und Writer erwarten, dass die Daten mit den Layout-Spezifikationen von EXIF, IPTC und XMP auf dem Datenträger übereinstimmen. Codec-Autoren können auch Ihre eigenen Anbieter für benutzerdefinierte Metadaten implementieren.

Aufgrund der Architektur von Windows Imaging Component (WIC) können metadatenwriter nur über eine Instanz eines Bild Encoders aufgerufen werden. Daher sollten Besitzer von rohformaten mindestens einen "Stub" [**wicrawparameterset. wicautoadjustedparameterset**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) -Encoder erstellen, auch wenn die tatsächliche Codierung von Pixeln in ein RAW-Format nicht implementiert ist. Der Codec-Autor muss die richtigen Metadatenhandler aufrufen:

-   [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) für den Decoder und den Frame Decoder entsprechend.
-   [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sowohl für den Encoder als auch den Frame Encoder.

Zur Unterstützung aller erwarteten Szenarien bei der Abbild Erstellung von Anwendungen in Windows Vista wird empfohlen, dass Codec-Anbieter mindestens Folgendes unterstützen:

-   EXIF-Lesevorgang
-   Partieller EXIF-Schreibvorgang (um Updates zum Erfassen von Datum und Uhrzeit zuzulassen)
-   XMP-Lese-und-Schreibvorgänge (einschließlich optional IPTC-Kern für XMP)
-   IPTC IIMv4 lesen und schreiben

Der größte Teil des metadatenzugriffs (sowohl Lese-als auch Schreibzugriff) in Windows Vista erfolgt über die [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -oder [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) -Schnittstelle. Um an der Windows Vista-metadatenumgebung teilnehmen zu können, müssen unformatierte Codec-Autoren die [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode und die [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) -Methode implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



