---
title: Die Kanal Zuordnung
description: Die Kanal Zuordnung
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Kanal Zuordnung
- Kanal Zuordnung
- MIDI-Mapper, Kanalnachrichten
- MIDI-Kanal Meldungen
- Kanal Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100751"
---
# <a name="the-channel-map"></a>Die Kanal Zuordnung

Die Kanal Zuordnung wirkt sich auf alle MIDI-Kanalnachrichten aus. Zu den Nachrichten von MIDI-Kanälen gehören Notiz-on, Note-Off, polyonic-after-afterberührungs, Steuerelement Änderung, Programmänderung, Channel-afterberührungs-und Nachrichten-Änderungs Meldungen. Der MIDI-Mapper verwendet eine einzelne Kanal Zuordnung mit einem Eintrag für jeden der 16 MIDI-Kanäle. Jeder Kanal Zuordnungs Eintrag gibt Folgendes an:

-   Ein Zielchannel für die MIDI-Nachricht.
-   Ein Ziel Ausgabegerät für die MIDI-Nachricht
-   Eine optionale patchkarte, die andere mögliche Änderungen für die MIDI-Nachricht angibt.

Der Zielchannel ist auf einen der 16 MIDI-Kanäle festgelegt. Die Nachrichten werden für die einzelnen neuen Kanal Zuweisungen geändert. Wenn z. b. der Ziel Kanal Eintrag für den MIDI-Kanal 4 auf 6 festgelegt ist, werden alle an Channel 4 gesendeten MIDI-Nachrichten Channel 6 zugeordnet, wie in der folgenden Abbildung dargestellt.

![zugeordnetes-](images/mmap-a05.gif)

In diesem Beispiel ist das MIDI-Status Byte 0x93 0x95 zugeordnet. Die niedrige Reihenfolge eines "MIDI Status Byte" gibt die Nummer des Kanals an. Quell Kanäle werden entweder auf "aktiv" oder "inaktiv" gesetzt. An inaktive Quell Kanäle gesendete Nachrichten werden ignoriert, sodass ein inaktiver Kanal in Kraft tritt oder ausgeschaltet ist.

Das Ziel Ausgabegerät ist auf eines der verfügbaren MIDI-Ausgabegeräte festgelegt. Bei einem Ausgabegerät vom Typ "MIDI" kann es sich um einen internen Synthesizer oder einen physischen, von einem Port

Bei den Systemnachrichten von System-/0xF0-und 0xFF-Meldungen handelt es sich um eine MIDI-Nachricht Es ist kein Kanal mit den Systemnachrichten von MIDI verknüpft und kann daher nicht zugeordnet werden. MIDI-Systemmeldungen werden an alle in einer Kanal Zuordnung aufgeführten in einer Kanal Zuordnung aufgeführten in einer Kanal Zuordnung aufgeführten-

 

 




