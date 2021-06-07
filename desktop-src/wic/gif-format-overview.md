---
description: Dieses Thema enthält Informationen zum nativen GIF-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Übersicht über das GIF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444451"
---
# <a name="gif-format-overview"></a>Übersicht über das GIF-Format

Dieses Thema enthält Informationen zum nativen GIF-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



|  Komponente             | BESCHREIBUNG                           |
|------------------------|---------------------------------------|
| Formale Namen         | Graphics Interchange Format 89a (GIF) |
| Dateinamenerweiterungen | GIF                                   |
| MIME-Typ (MIME type)              | image/gif                             |
| Spezifikationsunterstützung  | GIF-Spezifikation 89a/89m             |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen GIF-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatGif | 1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Decoder          | CLSID \_ WICGifDecoder     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Encoder          | CLSID \_ WICGifEncoder     | 114f5598-0b22-40a0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Encoderoptionen

WIC-fähige Codecs unterscheiden sich auf Codierungsoptionenebene. Encoderoptionen spiegeln die Funktionen eines Bildencoders wider, und jeder native Codec unterstützt eine Reihe dieser Encoderoptionen. Encoderoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (obwohl sie nicht unbedingt unterstützt werden) oder codecspezifische Optionen, die vom Bildformatcodec entworfen wurden. Um diese Codierungsoptionen während des Codierungsprozesses zu verwalten, verwendet WIC die [**IPropertyBag2-Schnittstelle**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Weitere Informationen zur Verwendung der **IPropertyBag2-Schnittstelle** für die WIC-Codierung finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

Der GIF-Encoder unterstützt keine grundlegenden WIC-Optionen und stellt keine benutzerdefinierten Encoderoptionen bereit. Wenn eine Encoderoption in der [**IPropertyBag2-Optionsliste**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) enthalten ist, wird sie ignoriert.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

 

 
