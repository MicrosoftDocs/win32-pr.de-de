---
description: In diesem Abschnitt der Themen finden Entwickler Anleitungen zum Implementieren von Bild Dateiformaten-Codecs, die innerhalb des WIC-Frameworks (Windows Imaging Component) funktionieren.
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Schreiben eines WIC-Enabled Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865551"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>Schreiben eines WIC-Enabled Codecs

In diesem Abschnitt der Themen finden Entwickler Anleitungen zum Implementieren von Bild Dateiformaten-Codecs, die innerhalb des WIC-Frameworks (Windows Imaging Component) funktionieren.

<dl>

[Introduction (Einführung)](-wic-howtowriteacodec-intro.md)  
[Funktionsweise der Windows Imaging Component (WIC)](-wic-howwicworks.md)  
<dl>

[Ermittlung und Schiedsgerichtsbarkeit](-wic-howwicworks.md)  
[Decodierung](-wic-howwicworks.md)  
[Codieren](-wic-howwicworks.md)  
[Die Lebensdauer eines Codecs.](-wic-howwicworks.md)  
[Gewusst wie: WIC-Aktivieren eines Codecs](-wic-howwicworks.md)  
[Multithread-Apartment Unterstützung in WIC](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementieren eines WIC-Enabled Decoders</a><dl>

[Decoder-Schnittstellen](-wic-decoderinterfaces.md)<dl>

[IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[IWICBitmapSource](-wic-imp-iwicbitmapsource.md)  
[IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)  
[IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementieren eines WIC-Enabled Encoders</a>  
<dl>

[Encoder-Schnittstellen](-wic-encoderinterfaces.md)  
<dl>

[Iwicbitmapcoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec-Installation und-Registrierung</a>  
<dl>

[Registrieren eines Codecs](-wic-codecinstallandreg.md)  
<dl>

[Allgemeine Register Einträge](-wic-generalregentries.md)  
[Codierungs spezifische Registrierungseinträge](-wic-encoderregentries.md)  
<dl>

[Registrieren eines Container Formats mit metadatenwritern](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">Codierungs spezifische Registrierungseinträge</a>  
<dl>

[Registrieren eines neuen Container Formats mit metadatenlesern](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">Integration in Windows Vista Photogallery und Explorer</a>  
<dl>

[Windows-Eigenschaften Speicher](-wic-integrationregentries.md)  
[Windows Vista-Fotogalerie](-wic-integrationregentries.md)  
[Windows Vista-Miniaturansicht-Cache](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Aktualisieren des Miniatur Ansichts Caches bei der Installation eines Codecs</a> [, der Ihren WIC-Enabled Codec für Benutzer zur Verfügung stellt](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Einführung (Schreiben eines WIC-Enabled Codecs)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



