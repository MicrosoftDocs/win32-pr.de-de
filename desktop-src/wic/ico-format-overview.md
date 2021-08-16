---
description: Dieses Thema enthält Informationen zum nativen ICO-Codec, der über Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Übersicht über das ICO-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf90f0a31beb2d004dcb43e08cb0b6b1539021071ff2cb3302b3076033bc833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204070"
---
# <a name="ico-format-overview"></a>Übersicht über das ICO-Format

Dieses Thema enthält Informationen zum nativen ICO-Codec, der über Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Codec-Identifikationsinformationen.



|   Komponente            | Beschreibung       |
|------------------------|-------------------|
| Formale Namen         | Symbolformat (ICO) |
| Dateinamenerweiterung(en) | Ico               |
| MIME-Typ (MIME type)              | image/ico         |
| Spezifikationsunterstützung  |                   |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen ICO-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Decoder          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Encoder          | NICHT VERFÜGBAR            | NICHT VERFÜGBAR                       |



 

## <a name="encoding"></a>Codierung

WIC stellt keinen nativen ICO-Bildencoder zur Verfügung.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist codecunabhängig, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht [über die Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

 

 



