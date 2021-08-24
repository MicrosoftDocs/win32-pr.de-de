---
description: 'Funktionserfändigung: Empfohlene Schnittstellen'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Funktionserfändigung: Empfohlene Schnittstellen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f54c7ec814d941a1f9c852408123f016182b2891ecf1965c3c3a98c768af210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811640"
---
# <a name="feature-completeness-recommended-interfaces"></a>Funktionserfändigung: Empfohlene Schnittstellen

In der folgenden Tabelle sind die Windows WIC-Schnittstellen (Imaging Component) aufgeführt, die RAW-Codecs implementieren sollten.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Schnittstelle</th>
<th>Erforderlich für</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>Iwicbitmapdecoder</strong></a></td>
<td>Decoder</td>
<td>Stellt den Ausgangspunkt für das Decodieren einer Bilddatei dar. Bietet Zugriff auf Eigenschaften auf Containerebene wie Miniaturansichten, Frames und Palette.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>Iwicbitmapframedecode</strong></a></td>
<td>Decoder</td>
<td>Stellt einen bestimmten Bildrahmen innerhalb des Containers dar, der Zugriff auf Eigenschaften auf Frameebene bietet. Dies ist die Schnittstelle, die die tatsächlichen Bildbits decodiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>Iwicmetadatablockreader</strong></a></td>
<td>Decoder</td>
<td>Erforderlich zum Aufzählen und Iterieren von Metadatenblöcken und zum Aufrufen der entsprechenden Metadatenleser beim Lesen aus einer Bilddatei. <br/>
<blockquote>
[!Note]<br />
Wenn das RAW-Containerformat TIFF-kompatibel ist oder STANDARD-IFDs oder IRBs zum Speichern von EXIF- oder XMP-Metadaten verwendet, können Codecautoren die integrierten Metadatenleser aufrufen, anstatt eigene zu schreiben.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></td>
<td>Decoder</td>
<td>Ermöglicht es dem Aufrufer, das gewünschte Skalierungs-, Zuschneide-, Drehungs- oder Pixelformat für das decodierte Bild anzugeben, wodurch die Decoderleistung erheblich verbessert werden kann. Beispielsweise verwenden die JPEG- und WDP-Decoder (Wireless Datagram Protocol) von Microsoft ein Pyramidenoptimierungsschema, um eine schnellere Decodierung zu erzielen, wenn die Zielbitmap kleiner als die Quellbitmap ist. Windows Vista (und höher) versucht, diese Schnittstelle zu verwenden, um eine schnelle Vorschau aus einem RAW-Bild zu extrahieren, wenn die eingebettete Vorschau in der größten Dimension fehlt oder weniger als &quot; &quot; 1.024 Pixel beträgt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></td>
<td>Decoder</td>
<td>Erforderlich für RAW-Formate. Macht Parameter verfügbar, die für die RAW-Bildverarbeitung spezifisch sind. RAW-Codecs sollten so viele dieser Parameter unterstützen, wie für den Codec gelten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></td>
<td>Encoder</td>
<td>Stellt den Ausgangspunkt für die Codierung einer Bilddatei dar. Diese Schnittstelle wird zum Festlegen von Eigenschaften auf Containerebene verwendet, z. B. Miniaturansichten, Frames und Paletten. Außerdem muss ein Metadatenwriter aufgerufen werden, um die Metadatenpersistenz für die Bilddatei zu aktivieren. Aus diesen Gründen ist diese Schnittstelle auch dann erforderlich, wenn die Codierung der primären Bitmap in das RAW-Format nicht unterstützt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></td>
<td>Encoder</td>
<td>Stellt einen bestimmten Bildrahmen innerhalb des Containers dar. Diese Schnittstelle wird verwendet, um die tatsächlichen Bildbits zu codieren und Pro-Frame-Metadaten und -Eigenschaften zu festlegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></td>
<td>Encoder</td>
<td>Erforderlich für das Iterieren von Metadatenblöcken und das Aufrufen der entsprechenden Metadatenschreiber beim Serialisieren einer Bilddatei.<br/>
<blockquote>
[!Note]<br />
Wenn das RAW-Containerformat TIFF-kompatibel ist, können Codecautoren die integrierten Metadatenschreiber aufrufen, anstatt eigene zu schreiben.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

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

 

 




