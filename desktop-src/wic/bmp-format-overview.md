---
description: Dieses Thema enthält Informationen über den systemeigenen BMP-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Übersicht zum BMP-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756912"
---
# <a name="bmp-format-overview"></a>Übersicht zum BMP-Format

Dieses Thema enthält Informationen über den systemeigenen BMP-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                       |
|------------------------|-----------------------|
| Formaler Name (n)         | Windows-Bitmap-Format |
| Dateinamenerweiterung (en) | BMP, DIB              |
| MIME-Typ (MIME type)              | image/bmp             |
| Spezifikations Unterstützung  | BMP-Spezifikation V5  |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen BMP-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatbmp | 0af1d87e-Fcfe-4188-bdeba7906471cbe3 |
| Decoder          | CLSID \_ wicbmpdecoder     | 6b462062-7cbf-400D-9F db813dd10f 2778 |
| Encoder          | CLSID \_ wicbmpencoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert und ist daher im Wesentlichen identisch mit der Bildcodierung für WIC-fähige Codecs. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Codierungsoptionen

WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene. Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen. Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle. Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für die WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

In der folgenden Tabelle sind die vom systemeigenen BMP-Codec unterstützten WIC-Encoder-Optionen aufgeführt.



| Eigenschaftsname               | VARTYPE      | Wertbereich                      | Standardwert      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **VT \_ bool** | **Variant \_ true/Variant \_ false** | **Variant \_ false** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Gibt an, ob das Codieren von Daten im GUID- \_ WICPixelFormat32bppBGRA Pixel Format zulässig ist. Wenn diese Option auf **Variant \_ true** festgelegt ist, wird die BMP mit einem BITMAPV5HEADER-Header geschrieben.

Der Standardwert ist **Variant \_ false**.

Wenn eine Encoder-Option in der IPropertyBag2-Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.

Hinweis bei Windows-BMP-Dateien mit 16-Bit-und 32-Bit-Dateien ignoriert der BMP-Codec alle Alphakanäle, da viele Legacy Bilddateien ungültige Daten in diesem zusätzlichen Kanal enthalten. Ab Windows 8 werden 32-Bit-Windows-BMP-Dateien, die mithilfe von **BITMAPV5HEADER** mit gültigem Alphakanal Inhalt geschrieben wurden, als WICPixelFormat32bppBGRA gelesen.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

 

 
