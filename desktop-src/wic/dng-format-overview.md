---
description: Dieses Thema enthält Informationen zum nativen DNG-Codec, der über Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Übersicht über das DNG-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32719e3fa9f45802058708e83635e52e287524496ae49f13f2168362358a7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204377"
---
# <a name="dng-format-overview"></a>Übersicht über das DNG-Format

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Dieses Thema enthält Informationen zum nativen DNG-Codec, der über Windows Imaging Component (WIC) verfügbar ist.

-   [Codec-Identität](#codec-identity)
-   [Decodierung](#decoding)

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



|     Komponente          |  Beschreibung                                         |
|------------------------|------------------------------------------------------|
| Formale Namen         | Digital Negative (DNG)                               |
| Dateinamenerweiterungen | .dng                                                 |
| MIME-Typen           | image/DNG                                            |
| Spezifikationsunterstützung  | Digital Negative (DNG) Specification Version 1.4.0.0 |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen DNG-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Decoder          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-API ist so konzipiert, dass sie codecunabhängig ist, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

Der Decoder unterstützt keine Decodierung von Sensorrohdaten und nur Dateien mit einer nicht rohen Bilddarstellung, die in eine IFD mit NewSubFileType gleich 1 eingebettet ist.

 

 



