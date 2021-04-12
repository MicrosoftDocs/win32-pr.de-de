---
description: Dieses Thema enthält Informationen über den nativen DNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Übersicht über das DNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345818"
---
# <a name="dng-format-overview"></a>Übersicht über das DNG-Format

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Dieses Thema enthält Informationen über den nativen DNG-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

-   [Codec-Identität](#codec-identity)
-   [Decodierung](#decoding)

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                                                      |
|------------------------|------------------------------------------------------|
| Formaler Name (n)         | Digitale negative Zahl (DNG)                               |
| Dateinamenerweiterung (en) | .dng                                                 |
| MIME-Typ (en)           | Bild/DNG                                            |
| Spezifikations Unterstützung  | Digital Negative (DNG)-Spezifikations Version 1.4.0.0 |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen DNG-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatadng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Decoder          | CLSID- \_ wicadngdecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

Der Decoder unterstützt das Decodieren von Rohdaten Sensordaten nicht und unterstützt nur Dateien mit einer nicht unformatierten Bilddarstellung, die in eine IFD mit einem newsubfiletype gleich 1 eingebettet ist.

 

 



