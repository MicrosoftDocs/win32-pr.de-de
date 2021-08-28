---
description: 'Funktionsvollständigkeit: Empfohlene Schnittstellen'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Funktionsvollständigkeit: Empfohlene Schnittstellen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c819f56b9343eab8326eb755d86280bde242a01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473826"
---
# <a name="feature-completeness-recommended-interfaces"></a>Funktionsvollständigkeit: Empfohlene Schnittstellen

In der folgenden Tabelle sind die Windows WIC-Schnittstellen (Imaging Component) aufgeführt, die RAW-Codecs implementieren sollten.




| Schnittstelle | Erforderlich für | BESCHREIBUNG | 
|-----------|--------------|-------------|
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>Iwicbitmapdecoder</strong></a> | Decoder | Stellt den Ausgangspunkt zum Decodieren einer Bilddatei dar. Bietet Zugriff auf Eigenschaften auf Containerebene wie Miniaturansichten, Frames und Paletten.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>Iwicbitmapframedecode</strong></a> | Decoder | Stellt einen bestimmten Bildrahmen innerhalb des Containers dar, der Zugriff auf Eigenschaften auf Frameebene bietet. Dies ist die Schnittstelle, die die tatsächlichen Bildbits decodiert.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>Iwicmetadatablockreader</strong></a> | Decoder | Erforderlich zum Auflisten und Durchlaufen von Metadatenblöcken und zum Aufrufen der entsprechenden Metadatenleser beim Lesen aus einer Bilddatei. <br /><blockquote>[!Note]<br />Wenn das RAW-Containerformat TIFF-kompatibel ist oder STANDARD-IFDs oder IRBs zum Speichern von EXIF- oder XMP-Metadaten verwendet, können Codecautoren die integrierten Metadatenleser aufrufen, anstatt ihre eigenen zu schreiben.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a> | Decoder | Ermöglicht es dem Aufrufer, das gewünschte Skalierungs-, Zuschneide-, Dreh- oder Pixelformat für das decodierte Bild anzugeben, was die Decoderleistung erheblich verbessern kann. Beispielsweise verwenden die JPEG- und WDP-Decoder (Wireless Datagram Protocol) von Microsoft ein Pyramidenoptimierungsschema, um eine schnellere Decodierung zu erreichen, wenn die Zielbitmap kleiner als die Quellbitmap ist. Windows Vista (und höher) versucht, diese Schnittstelle zu verwenden, um eine "schnelle" Vorschau aus einem RAW-Bild zu extrahieren, wenn die eingebettete Vorschau in der größten Dimension fehlt oder kleiner als 1.024 Pixel ist.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a> | Decoder | Erforderlich für RAW-Formate. Macht Parameter verfügbar, die spezifisch für die RAW-Bildverarbeitung sind. RAW-Codecs sollten so viele dieser Parameter unterstützen, wie sie für den Codec gelten.<br /> | 
| <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a> | Encoder | Stellt den Ausgangspunkt für die Codierung einer Bilddatei dar. Diese Schnittstelle wird zum Festlegen von Eigenschaften auf Containerebene verwendet, z. B. Miniaturansichten, Frames und Paletten. Es ist auch erforderlich, einen Metadatenwriter aufzurufen, um Metadatenpersistenz für die Bilddatei zu aktivieren. Aus diesen Gründen ist diese Schnittstelle auch dann erforderlich, wenn die Codierung der primären Bitmap in das RAW-Format nicht unterstützt wird.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a> | Encoder | Stellt einen bestimmten Bildrahmen innerhalb des Containers dar. Diese Schnittstelle wird verwendet, um die tatsächlichen Bildbits zu codieren und Metadaten und Eigenschaften pro Frame festzulegen.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> | Encoder | Erforderlich für das Durchlaufen von Metadatenblöcken und das Aufrufen der entsprechenden Metadatenwriter beim Serialisieren einer Bilddatei.<br /><blockquote>[!Note]<br />Wenn das RAW-Containerformat TIFF-kompatibel ist, können Codecautoren die integrierten Metadatenwriter aufrufen, anstatt ihre eigenen zu schreiben.</blockquote><br /><br /> | 




 

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

 

 




