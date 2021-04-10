---
title: Auswählen von Bitraten
description: Auswählen von Bitraten
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- Profile, auswählen von Bitraten
- Profile, Bitraten
- Codecs, auswählen von Bitraten
- Codecs, Bitraten
- Profile, auswählen von Bitraten
- Codecs, auswählen von Bitraten
- Bitraten, auswählen
- Bitraten, profile
- Bitraten, Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309160"
---
# <a name="selecting-bit-rates"></a>Auswählen von Bitraten

Bei Dateien, die über ein Netzwerk gestreamt werden, müssen Sie sorgfältig überlegen, welche Bitraten Sie verwenden sollten. In den meisten Fällen können Sie die Bitraten aller Streams in einer Datei hinzufügen, um eine allgemeine Vorstellung von der verfügbaren Bandbreite zu erhalten, die zum Streamen der Datei erforderlich ist. Eine bestimmte Menge an mehr Aufwand ist jedoch auch für jeden Stream erforderlich. Dieser mehr Aufwand wird in der folgenden Tabelle zusammengefasst.



| Bitraten Bereich (Kbit/s) | Zusätzliche Bandbreite für mehr Aufwand erforderlich (Kbit/s) |
|-----------------------|---------------------------------------------------|
| 10 – 16               | 3                                                 |
| 17 – 30               | 4                                                 |
| 31 – 45               | 5                                                 |
| 46 – 70               | 6                                                 |
| 71 – 225              | 7                                                 |
| >225               | 9                                                 |



 

Der für einen Datenstrom erforderliche normale Aufwand nimmt keine Dateneinheiten Erweiterungen in Betracht. Jede dateneinheits Erweiterung fügt der Größe des Beispiels hinzu, an das Sie angefügt ist. Abhängig vom Typ der dateneinheits Erweiterung kann dadurch die Bitrate für den Stream erheblich erhöht werden.

Sie müssen auch Bedenken, dass die theoretische maximale Bandbreite, die über eine Netzwerkverbindung verfügbar ist, keine praktische Zielbitrate ist. Die durchschnittliche verfügbare Bandbreite für eine beliebige Verbindung ist aufgrund des Netzwerkverkehrs und vieler anderer Faktoren eine kurze Bandbreitenkapazität für die Verbindung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwerfen von Profilen**](designing-profiles.md)
</dt> </dl>

 

 




