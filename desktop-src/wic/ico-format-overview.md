---
description: Dieses Thema enthält Informationen zum nativen ICO-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Übersicht über das ICO-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444470"
---
# <a name="ico-format-overview"></a>Übersicht über das ICO-Format

Dieses Thema enthält Informationen zum nativen ICO-Codec, der über Windows-Bilderstellungskomponente (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



|   Komponente            | BESCHREIBUNG       |
|------------------------|-------------------|
| Formale Namen         | Symbolformat (ICO) |
| Dateinamenerweiterungen | Ico               |
| MIME-Typ (MIME type)              | image/ico         |
| Spezifikationsunterstützung  |                   |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen ICO-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Decoder          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Encoder          | NICHT VERFÜGBAR            | NICHT VERFÜGBAR                       |



 

## <a name="encoding"></a>Codierung

WIC stellt keinen nativen ICO-Imageencoder bereit.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

 

 



