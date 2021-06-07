---
description: Dieses Thema enthält Informationen zum nativen PNG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Übersicht über das PNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444441"
---
# <a name="png-format-overview"></a>Übersicht über das PNG-Format

Dieses Thema enthält Informationen zum nativen PNG-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



|     Komponente          | BESCHREIBUNG                     |
|------------------------|---------------------------------|
| Formale Namen         | PNG (Portable Network Graphics) |
| Dateinamenerweiterungen | png                             |
| MIME-Typ (MIME type)              | image/png                       |
| Spezifikationsunterstützung  | PNG-Spezifikation 1.2           |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen PNG-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatPng | 1b7cfaf4-713f-473c-mussd6137425faeaf |
| Decoder          | CLSID \_ WICPngDecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Encoder          | CLSID \_ WICPngEncoder     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 und höher

Ab Windows 8 WIC wird ein zusätzlicher PNG-Decoder bereitgestellt.

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Encoderoptionen

WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene. Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen. Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes (jedoch nicht unbedingt unterstützt) oder codecspezifische Optionen verfügbar sind, die vom Bildformatcodec entworfen wurden. Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

Der PNG-Codec verwendet grundlegende WIC-Encoderoptionen. In der folgenden Tabelle sind die WIC-Encoderoptionen aufgeführt, die vom nativen PNG-Codec unterstützt werden.



| Eigenschaftsname   | VARTYPE  | Wertbereich                                                 | Standardwert                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | VT \_ BOOL | **TRUE** / **FALSE**                                          | **FALSE**                                                        |
| FilterOption    | VT \_ UI1  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) vorhanden ist, die der Codec nicht unterstützt, wird sie ignoriert.

### <a name="interlaceoption"></a>InterlaceOption

Gibt an, ob die Bilddaten als Interlacing codiert werden sollen.

Der Standardwert ist **FALSE**.

### <a name="filteroption"></a>FilterOption

Gibt die Filteroption an, die für die Bildkomprimierung verwendet werden soll.

Der Standardwert ist [**WICPngFilterUnspecified.**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

Der native PNG-Codec unterstützt auch [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) bei der Framedecodierung und fügt erweiterte Optionen zum Decodieren eines Bilddatenstroms hinzu. Weitere Informationen zu diesen erweiterten Optionen finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

 

 
