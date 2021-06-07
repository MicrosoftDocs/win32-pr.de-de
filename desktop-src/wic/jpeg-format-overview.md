---
description: Dieses Thema enthält Informationen zum nativen JPEG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Übersicht über das JPEG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444191"
---
# <a name="jpeg-format-overview"></a>Übersicht über das JPEG-Format

Dieses Thema enthält Informationen zum nativen JPEG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



|   Komponente            | BESCHREIBUNG                             |
|------------------------|-----------------------------------------|
| Formale Namen         | JPEG (Joint Photographic Experts Group) |
| Dateinamenerweiterungen | jpe, jpeg, jpg                          |
| MIME-Typ (MIME type)              | image/jpeg, image/jpe, image/jpg        |
| Spezifikationsunterstützung  | JFIF-Spezifikation 1.02                 |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen JPEG-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatJpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Decoder          | CLSID \_ WICJpegDecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Encoder          | CLSID \_ WICJpegEncoder     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Encoderoptionen

WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene. Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen. Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (obwohl sie nicht unbedingt unterstützt werden) oder codecspezifische Optionen, die vom Bildformatcodec entworfen wurden. Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

Der JPEG-Codec verwendet grundlegende WIC-Optionen. In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen JPEG-Codec unterstützt werden.



| Eigenschaftsname                                        | VARTYPE           | Wertbereich                                                                       | Standardwert                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0 - 1.0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | VT \_ UI1           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Sättigung](#luminance-option)                       | VT \_ UI4/VT \_ ARRAY | 64 Einträge (DCT)                                                                  | Standard-Leuchtdichtetabelle.                                                       |
| [Chrominance](#chrominance-option)                   | VT \_ UI4/VT \_ ARRAY | 64 Einträge (DCT)                                                                  | Standard-Chromeinancetabelle.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | VT \_ BOOL          | **TRUE** / **FALSE**                                                                | **FALSE**                                                                      |



 

Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.

### <a name="imagequality-option"></a>ImageQuality-Option

Gibt die gewünschte Bildgenauigkeit an. 0,0 gibt die niedrigste mögliche Genauigkeit und 1,0 die höchste Genauigkeit an.

Der Standardwert ist 0,9.

### <a name="bitmaptransform-option"></a>BitmapTransform-Option

Gibt an, wie das Bild während der Bilddecodierung transformiert werden soll. Diese Option muss auf einen der [**WICBitmapTransformOptions-Enumerationswerte**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) festgelegt werden.

Der Standardwert ist [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="luminance-option"></a>Luminance-Option

Gibt die Graustufen-Helligkeitsebenentabelle an, die für die Codierung verwendet werden soll.

### <a name="chrominance-option"></a>Chromeinance-Option

Gibt die Chromeinancetabelle an, die für die Codierung verwendet werden soll.

### <a name="jpegycrcbsubsampling-option"></a>JpegYCrCbSubsampling-Option

Gibt das Untersamplingverhältnis an, das für die YCrCb-Codierung verwendet werden soll.

Der Standardwert ist [**WICJpegYCrCbSubsampling420.**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)

### <a name="suppressapp0-option"></a>SuppressApp0-Option

Gibt an, ob das Schreiben von App0-Metadaten beim Codieren der Bilddaten unterdrückt werden soll.

Der Standardwert ist **FALSE**.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

Der native JPEG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei der Framedecodierung und fügt freigeschaltete Optionen zum Decodieren eines Bilddatenstroms hinzu. Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

 

 
