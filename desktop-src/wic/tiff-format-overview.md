---
description: Dieses Thema enthält Informationen zum nativen TIFF-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Übersicht über das TIFF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444421"
---
# <a name="tiff-format-overview"></a>Übersicht über das TIFF-Format

Dieses Thema enthält Informationen zum nativen TIFF-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.

-   [Codec-Identität](#codec-identity)
-   [Codieren](#encoding)
    -   [Encoderoptionen](#encoder-options)
-   [Decodierung](#decoding)

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Codec-Identifikationsinformationen.



|   Komponente            |   BESCHREIBUNG                   |
|------------------------|---------------------------------|
| Formale Namen         | TIFF (Tagged Image File Format) |
| Dateinamenerweiterung(en) | tiff, tif                       |
| MIME-Typen           | image/tiff, image/tif           |
| Spezifikationsunterstützung  | TIFF-Spezifikation 6.0          |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen TIFF-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Containerformat | GUID \_ ContainerFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Decoder          | CLSID \_ WICTiffDecoder     | b54e85d9-fe23-499f-8b886acea7137502b |
| Encoder          | CLSID \_ WICTiffEncoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist codecunabhängig, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie unter Übersicht über [die Codierung.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Encoderoptionen

WIC-fähige Codecs unterscheiden sich auf der Ebene der Codierungsoption. Encoderoptionen spiegeln die Funktionen eines Bildencoder wider, und jeder native Codec unterstützt einen Satz dieser Encoderoptionen. Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes (wenn auch nicht unbedingt unterstützt) oder codecspezifische Optionen verfügbar sind, die vom Bildformatcodec entworfen wurden. Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie unter Übersicht über [die Codierung.](-wic-creating-encoder.md)

Der TIFF-Codec verwendet grundlegende WIC-Optionen. In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen TIFF-Codec unterstützt werden.

| Eigenschaftsname         | VARTYPE | Wertbereich | Standardwert    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0 - 1.0     | 0                |
| TiffCompressionMethod | VT \_ UI1 | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.

### <a name="compressionquality-option"></a>CompressionQuality-Option

Gibt die gewünschte Komprimierungsqualität an. 0.0 gibt das am wenigsten effiziente Komprimierungsschema an. In der Regel führt dieses Schema zu einer schnelleren Codierung, aber zu einer größeren Ausgabe. Der Wert 1.0 gibt das effizienteste verfügbare Komprimierungsschema an. In der Regel führt dieses Schema zu einer längeren Codierung, erzeugt jedoch eine kleinere Ausgabe.

Der Standardwert ist 0.

### <a name="tiffcompressionmethod-option"></a>TiffCompressionMethod-Option

Gibt die TIFF-Komprimierungsmethode an.

Der Standardwert ist [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-APIs sind codecunabhängig, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der [Übersicht über die Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

 

 
