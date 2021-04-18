---
description: Dieses Thema enthält Informationen über den nativen TIFF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Übersicht über TIFF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366143"
---
# <a name="tiff-format-overview"></a>Übersicht über TIFF-Format

Dieses Thema enthält Informationen über den nativen TIFF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

-   [Codec-Identität](#codec-identity)
-   [Codieren](#encoding)
    -   [Codierungsoptionen](#encoder-options)
-   [Decodierung](#decoding)

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                                 |
|------------------------|---------------------------------|
| Formaler Name (n)         | TIFF (Tagged Image File Format) |
| Dateinamenerweiterung (en) | TIFF, TIF                       |
| MIME-Typ (en)           | Bild/TIFF, Bild/TIF           |
| Spezifikations Unterstützung  | TIFF-Spezifikation 6,0          |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen TIFF-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Container Format | GUID \_ containerformattiff | 163bcc30-e2e9-4f 0B-961da3e9sdb788a3  |
| Decoder          | CLSID \_ wictiffdecoder     | b54e85d9-FE23-499f-8b886acea7137502b |
| Encoder          | CLSID- \_ wictiffencoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Codierungsoptionen

WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene. Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen. Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle. Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

Der TIFF-Codec verwendet grundlegende WIC-Optionen. In der folgenden Tabelle sind die vom systemeigenen TIFF-Codec unterstützten WIC-Encoder-Optionen aufgeführt.

| Eigenschaftsname         | VARTYPE | Wertbereich | Standardwert    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0-1,0     | 0                |
| TiffCompressionMethod | VT \_ UI1 | [**Wictiffcompressionoption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**Wictiffcompressiondontcare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.

### <a name="compressionquality-option"></a>CompressionQuality (Option)

Gibt die gewünschte Komprimierungs Qualität an. 0,0 gibt das am wenigsten effiziente verfügbare Komprimierungs Schema an. In der Regel führt dieses Schema zu einer schnelleren Codierung, aber eine größere Ausgabe. Der Wert 1,0 gibt das effizienteste verfügbare Komprimierungs Schema an. In der Regel führt dieses Schema zu einer längeren Codierung, erzeugt jedoch eine geringere Ausgabe.

Der Standardwert ist 0.

### <a name="tiffcompressionmethod-option"></a>Tiffcompressionmethod (Option)

Gibt die TIFF-Komprimierungs Methode an.

Der Standardwert ist [**wictiffcompressiondontcare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-APIs sind als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

 

 
