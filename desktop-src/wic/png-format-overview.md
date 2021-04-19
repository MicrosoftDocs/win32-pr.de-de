---
description: Dieses Thema enthält Informationen über den systemeigenen PNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Übersicht über PNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360747"
---
# <a name="png-format-overview"></a>Übersicht über PNG-Format

Dieses Thema enthält Informationen über den systemeigenen PNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                                 |
|------------------------|---------------------------------|
| Formaler Name (n)         | PNG (Portable Network Graphics) |
| Dateinamenerweiterung (en) | png                             |
| MIME-Typ (MIME type)              | image/png                       |
| Spezifikations Unterstützung  | PNG-Spezifikation 1,2           |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen PNG-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatpng | 1b7cfaf4-713f-473c-bbcd6137425faeaf |
| Decoder          | CLSID- \_ wicpngdecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Encoder          | CLSID \_ wicpngencoder     | 27949969-876a-41d7-9447568f & 6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 und höher

Ab Windows 8 bietet WIC einen zusätzlichen PNG-Decoder.

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Codierungsoptionen

WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene. Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen. Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle. Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

Der PNG-Codec verwendet grundlegende WIC-Encoder-Optionen. In der folgenden Tabelle werden die vom systemeigenen PNG-Codec unterstützten WIC-Encoder-Optionen aufgelistet.



| Eigenschaftsname   | VARTYPE  | Wertbereich                                                 | Standardwert                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | VT \_ bool | **True** / **False**                                          | **FALSE**                                                        |
| FilterOption    | VT \_ UI1  | [**Wicpngfilteroption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**Wicpngfilterunspezifiziert**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste vorhanden ist, die der Codec nicht unterstützt, wird Sie ignoriert.

### <a name="interlaceoption"></a>InterlaceOption

Gibt an, ob die Bilddaten als Zeilen Sprung codiert werden sollen.

Der Standardwert ist **FALSE**.

### <a name="filteroption"></a>FilterOption

Gibt die für die Bildkomprimierung zu verwendende Filteroption an.

Der Standardwert ist " [**wicpngfilterunspezifiziert**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)".

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

Der Native PNG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei der Frame-Decodierung und fügt Erweiterte Optionen für das Decodieren eines bildstreams hinzu. Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

 

 
