---
description: Dieses Thema enthält Informationen zum nativen BMP-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Übersicht über das BMP-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444961"
---
# <a name="bmp-format-overview"></a>Übersicht über das BMP-Format

Dieses Thema enthält Informationen zum nativen BMP-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



| Komponente              | BESCHREIBUNG           |
|------------------------|-----------------------|
| Formale Namen         | Windows Bitmap-Format |
| Dateinamenerweiterungen | bmp, dib              |
| MIME-Typ (MIME type)              | image/bmp             |
| Spezifikationsunterstützung  | BMP-Spezifikation v5  |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen BMP-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Decoder          | CLSID \_ WICBmpDecoder     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| Encoder          | CLSID \_ WICBmpEncoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist. Daher ist die Bildcodierung für WIC-fähige Codecs im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Encoderoptionen

WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene. Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen. Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes (jedoch nicht unbedingt unterstützt) oder codecspezifische Optionen verfügbar sind, die vom Bildformatcodec entworfen wurden. Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen BMP-Codec unterstützt werden.



| Eigenschaftsname               | VARTYPE      | Wertbereich                      | Standardwert      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **VT \_ BOOL** | **VARIANT \_ TRUE/VARIANT \_ FALSE** | **VARIANT \_ FALSE** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Gibt an, ob Codierungsdaten im \_ GUID-Format WICPixelFormat32bppBGRA-Pixel zulässig sind. Wenn diese Option auf **VARIANT \_ TRUE** festgelegt ist, wird der BMP mit einem BITMAPV5HEADER-Header geschrieben.

Der Standardwert ist **VARIANT \_ FALSE.**

Wenn eine Encoderoption in der IPropertyBag2-Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.

Beachten Sie, dass der BMP-Codec bei 16-Bit- und 32-Bit-Windows-BMP-Dateien alle Alphakanäle ignoriert, da viele Legacyimagedateien ungültige Daten in diesem zusätzlichen Kanal enthalten. Ab Windows 8 werden 32-Bit-Windows-BMP-Dateien, die mit **BITMAPV5HEADER** mit gültigem Alphakanalinhalt geschrieben wurden, als WICPixelFormat32bppBGRA gelesen.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

 

 
