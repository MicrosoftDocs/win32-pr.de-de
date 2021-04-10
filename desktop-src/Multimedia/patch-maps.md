---
title: Patchzuordnungen
description: Patchzuordnungen
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, patchmaps
- patchzuordnungen
- 'MIDI-Programm: Änderungs Meldungen'
- MIDI-volumecontroller-Meldungen
- Programm-Änderungs Meldungen
- volumecontroller-Meldungen
- MIDI-Mapper, Programm-Änderungs Meldungen
- MIDI-Mapper, volumecontroller-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309851"
---
# <a name="patch-maps"></a>Patchzuordnungen

Jedem Kanal Zuordnungs Eintrag kann eine zugeordnete patchkarte zugeordnet sein. Patchzuordnungen wirken sich auf die Nachrichten von MIDI-Programmänderungen und Volume Controller aus. Programm-Änderungs Meldungen weisen einen Synthesizer an, den instrumentierungsound (Patch) für einen angegebenen Kanal zu ändern. Volumecontroller-Meldungen legen das Volume für einen Kanal fest.

Eine patchkarte verfügt über eine Übersetzungstabelle mit einem Eintrag für jeden der 128-Programm Änderungs Werte. Jede patchzuordnung gibt Folgendes an:

-   Ein Zielprogramm: Ändern Sie den Wert.
-   Ein volumeskalar. (Weitere Informationen finden Sie [unter Volume Scalar](the-volume-scalar.md).)
-   Eine optionale Schlüssel Zuordnung. (Weitere Informationen finden Sie unter [Key Maps](key-maps.md).)

Beim Empfang von Programm Änderungs Meldungen durch den MIDI-Mapper wird der Wert des Zielprogramms-ändern in der Nachricht durch den Wert für den Programm Änderungs Wert ersetzt. Wenn das Zielprogramm z. b. den Wert für Programmänderung 16 auf 18 festgelegt ist, ändert der MIDI-Mapper die Programm Änderungs Nachricht des Pakets, wie in der folgenden Abbildung dargestellt.

![Bild von MIDI-Mapper](images/mmap-a03.gif)

 

 




