---
title: Schlüssel Zuordnungen
description: Schlüssel Zuordnungen
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Schlüssel Zuordnungen
- Schlüssel Zuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947567"
---
# <a name="key-maps"></a>Schlüssel Zuordnungen

Jedem Eintrag in der patchzuordnungs-Übersetzungstabelle ist eine zugeordnete Schlüssel Zuordnung zugeordnet. Schlüssel Zuordnungen betreffen die Nachrichten "Note-on", "Note-Off" und "Polyphonic-after-afternote". Eine Schlüssel Zuordnung verfügt über eine Übersetzungstabelle mit einem Eintrag für jeden der 128-Schlüsselwerte. Wenn der Eintrag für den Schlüsselwert 60 z. b. 72 ist, ändert der MIDI-Mapper die Informationen zu "MIDI Note-on", wie in der folgenden Abbildung dargestellt.

![Bild von MIDI-Mapper](images/mmap-a06.gif)

Schlüssel Zuordnungen sind bei Synthesizern nützlich, die über Schlüssel basierte Percussion-Instrumente verfügen, denen jeweils ein bestimmter Percussion-Sound zugewiesen ist. Schlüssel Zuordnungen werden in der Regel dem ersten Patch in den patchmaps auf den Percussion-Kanälen (10 und 16) zugewiesen.

 

 




