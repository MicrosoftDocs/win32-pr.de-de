---
description: Dieses Thema enthält Informationen über den nativen ICO-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Übersicht über ICO-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360814"
---
# <a name="ico-format-overview"></a>Übersicht über ICO-Format

Dieses Thema enthält Informationen über den nativen ICO-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                   |
|------------------------|-------------------|
| Formaler Name (n)         | Symbol Format (ICO) |
| Dateinamenerweiterung (en) | ICO               |
| MIME-Typ (MIME type)              | Image/ICO         |
| Spezifikations Unterstützung  |                   |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen ICO-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatico | a3a860c4-338f-4c17-919afba4b5628f |
| Decoder          | CLSID- \_ wicikodecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Encoder          | NICHT VERFÜGBAR            | NICHT VERFÜGBAR                       |



 

## <a name="encoding"></a>Codierung

WIC stellt keinen systemeigenen ICO-Image Encoder bereit.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

 

 



