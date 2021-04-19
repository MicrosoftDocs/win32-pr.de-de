---
description: Dieses Thema enthält Informationen über den nativen JPEG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Übersicht über JPEG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349868"
---
# <a name="jpeg-format-overview"></a>Übersicht über JPEG-Format

Dieses Thema enthält Informationen über den nativen JPEG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                                         |
|------------------------|-----------------------------------------|
| Formaler Name (n)         | JPEG (Joint Photographic Experts Group) |
| Dateinamenerweiterung (en) | jpe, JPEG, JPG                          |
| MIME-Typ (MIME type)              | Image/JPEG, Image/jpe, Image/JPG        |
| Spezifikations Unterstützung  | JFIF-Spezifikation 1,02                 |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen JPEG-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatjpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Decoder          | CLSID \_ wicjpgdecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Encoder          | CLSID \_ wicjpeer-Coder     | 1a34f 5C1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Codierungsoptionen

WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene. Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen. Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle. Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

Der JPEG-Codec verwendet grundlegende WIC-Optionen. In der folgenden Tabelle sind die vom systemeigenen JPEG-Codec unterstützten WIC-Encoder-Optionen aufgeführt.



| Eigenschaftsname                                        | VARTYPE           | Wertbereich                                                                       | Standardwert                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0-1,0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | VT \_ UI1           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Sättigung](#luminance-option)                       | VT \_ UI4/VT- \_ Array | 64 Einträge (DCT)                                                                  | Standardmäßige Leuchtkraft Tabelle.                                                       |
| [Chrominance](#chrominance-option)                   | VT \_ UI4/VT- \_ Array | 64 Einträge (DCT)                                                                  | Standardmäßige Chrominanz-Tabelle.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | VT \_ UI1           | [**Wicjppfgycrcbsubsamplingoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | VT \_ bool          | **True** / **False**                                                                | **FALSE**                                                                      |



 

Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.

### <a name="imagequality-option"></a>ImageQuality-Option

Gibt die gewünschte Bild Treue an. 0,0 gibt die niedrigste mögliche Treue an, und 1,0 gibt die höchste Genauigkeit an.

Der Standardwert ist 0,9.

### <a name="bitmaptransform-option"></a>BitmapTransform (Option)

Gibt an, wie das Bild während der Decodierung von Bildern transformiert werden soll. Diese Option muss auf einen der [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) -Enumerationswerte festgelegt werden.

Der Standardwert ist [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="luminance-option"></a>Option "Leuchtkraft"

Gibt die für die Codierung zu verwendende Graustufen Helligkeit-Ebenen-Tabelle an.

### <a name="chrominance-option"></a>Chrominance (Option)

Gibt die für die Codierung zu verwendende Chrominanz-Tabelle an.

### <a name="jpegycrcbsubsampling-option"></a>Jpgycrcbsubsampling (Option)

Gibt das unter Stichproben Verhältnis an, das für die YCrCb-Codierung verwendet wird.

Der Standardwert ist [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).

### <a name="suppressapp0-option"></a>SuppressApp0-Option

Gibt an, ob das Schreiben von App0-Metadaten beim Codieren der Bilddaten unterdrückt werden soll.

Der Standardwert ist **FALSE**.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

Der Native JPEG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei Frame-Decodierung das Hinzufügen von bereitgestellten Optionen für das Decodieren eines bildstreams. Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

 

 
