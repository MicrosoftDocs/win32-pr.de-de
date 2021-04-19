---
description: 'Vollständigkeit der Features: Empfohlene Schnittstellen'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Vollständigkeit der Features: Empfohlene Schnittstellen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352232"
---
# <a name="feature-completeness-recommended-interfaces"></a>Vollständigkeit der Features: Empfohlene Schnittstellen

In der folgenden Tabelle sind die WIC-Schnittstellen (Windows Imaging Component, Windows Imaging Component) aufgelistet, die von den



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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></td>
<td>Decoder</td>
<td>Stellt den Startpunkt für das Decodieren einer Bilddatei dar. Bietet Zugriff auf Eigenschaften auf Container Ebene wie Miniaturansichten, Frames und Palette.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></td>
<td>Decoder</td>
<td>Stellt einen bestimmten Bild Rahmen innerhalb des Containers dar, der Zugriff auf Eigenschaften auf Frame-Ebene bereitstellt. Dies ist die Schnittstelle, die die eigentlichen Bildbits decodiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></td>
<td>Decoder</td>
<td>Erforderlich für das Auflisten und durchlaufen von metadatenblöcken und das Aufrufen der entsprechenden metadatenleser beim Lesen aus einer Bilddatei. <br/>
<blockquote>
[!Note]<br />
Wenn das RAW-Container-Format TIFF-kompatibel ist oder zum Speichern von EXIF-oder XMP-Metadaten Standard-ifds oder-Spalten verwendet, können die Codec-Autoren die integrierten metadatenleser aufrufen, anstatt Sie zu schreiben.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></td>
<td>Decoder</td>
<td>Ermöglicht dem Aufrufer, die gewünschte Skalierung, das Zuschneiden, das Drehen oder das Pixel Format für das decodierte Bild anzugeben, wodurch die decoderleistung erheblich verbessert werden kann. Beispielsweise wird von den Decodern von Microsoft JPEG und Wireless Datagram Protocol (WDP) ein Pyramiden Optimierungs Schema verwendet, um eine schnellere Decodierung zu erreichen, wenn die Zielbitmap kleiner als die Quell Bitmap ist. Windows Vista (und höher) versucht, diese Schnittstelle zu verwenden, um eine &quot; schnelle &quot; Vorschau von einem RAW-Image zu extrahieren, wenn die eingebettete Vorschau fehlt oder in der größten Dimension weniger als 1.024 Pixel.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></td>
<td>Decoder</td>
<td>Erforderlich für Rohdaten Formate. Macht Parameter verfügbar, die für die Rohbild Verarbeitung spezifisch sind. Unformatierte Codecs sollten so viele dieser Parameter unterstützen, wie Sie auf den Codec angewendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>Iwicbitmapcoder</strong></a></td>
<td>Encoder</td>
<td>Stellt den Startpunkt für das Codieren einer Bilddatei dar. Diese Schnittstelle wird verwendet, um Eigenschaften auf Container Ebene festzulegen, z. b. Miniaturansichten, Frames und Palette. Außerdem müssen Sie einen metadatenwriter aufrufen, um die metadatenpersistenz in der Bilddatei zu aktivieren. Aus diesen Gründen ist diese Schnittstelle notwendig, auch wenn die Codierung der primären Bitmap in das RAW-Format nicht unterstützt wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></td>
<td>Encoder</td>
<td>Stellt einen bestimmten Bild Rahmen innerhalb des Containers dar. Diese Schnittstelle wird verwendet, um die eigentlichen Bildbits zu codieren und um die einzelnen Frame-Metadaten und-Eigenschaften festzulegen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></td>
<td>Encoder</td>
<td>Erforderlich zum Durchlaufen von metadatenblöcken und zum Aufrufen der entsprechenden metadatenschreiber beim Serialisieren einer Bilddatei.<br/>
<blockquote>
[!Note]<br />
Wenn das RAW-Containerformat TIFF-kompatibel ist, können Codec-Autoren die integrierten metadatenwriter aufrufen, anstatt Sie selbst zu schreiben.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

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

 

 




