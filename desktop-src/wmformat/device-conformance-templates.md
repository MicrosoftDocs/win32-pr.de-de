---
title: Geräte Konformitäts Vorlagen
description: Geräte Konformitäts Vorlagen
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media-Format-SDK, Geräte Konformitäts Vorlagen
- Codecs, Geräte Konformitäts Vorlagen
- Geräte Konformitäts Vorlagen, Informationen zu
- Vorlagen, Geräte Konformitäts Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311274"
---
# <a name="device-conformance-templates"></a>Geräte Konformitäts Vorlagen

Die Codecs der Windows Media 9-Serie unterstützen Geräte Konformitäts Vorlagen, bei denen es sich um definierte Bereiche von Datenstrom-Konfigurationseinstellungen und Codec-Algorithmen handelt. Jede Vorlage definiert die Wertebereiche, die für bestimmte Geräte geeignet sind.

In der Vergangenheit arbeiteten die Hardwarehersteller, die Geräte, die in der Lage waren, ASF-Dateien zu spielen, alle an Ihren eigenen Standards. Dies führte zu den weitgehend unterschiedlichen Funktionen auf ähnlichen Geräten, die heute fortgesetzt werden.

Mit den Geräte Konformitäts Vorlagen legen die Windows Media Codecs eine gemeinsame Basis für ähnliche Geräte fest. Hardware Hersteller können angeben, welchen Vorlagen Ihre Geräte entsprechen. so können Inhalts Ersteller ihre Dateien zuverlässiger auf das Lesen von Geräten ausrichten. Außerdem ist es für Player Anwendungen einfacher zu bestimmen, ob eine Datei für das Gerät ungeeignet ist, bevor versucht wird, Sie wiederzugeben.

Eine Vorlage für die Geräte Konformität wird durch eine Zeichenfolge identifiziert, die als Metadatenattribut gespeichert ist, das dem Stream zugeordnet ist, für den die Vorlage gilt. Eine Liste der Vorlagen und deren Zeichen folgen und Parameter finden Sie unter [Geräte](device-conformance-template-parameters.md)Übereinstimmungs-Vorlagen Parameter.

Geräte Konformitäts Vorlagen werden für alle Windows Media 9-und spätere Codecs unterstützt, mit Ausnahme der Windows Media Video 9-Bildschirm Codecs und des Windows Media Audio 9-Codec ohne Verlust.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Codec-Features**](codec-features.md)
</dt> <dt>

[**Arbeiten mit Geräte Konformitäts Vorlagen**](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




