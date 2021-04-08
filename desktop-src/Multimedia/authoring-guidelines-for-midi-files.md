---
title: Erstellungs Richtlinien für MIDI-Dateien
description: Erstellungs Richtlinien für MIDI-Dateien
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Digital Instrumentation Digital Interface (MIDI), Richtlinien zum Erstellen von Dateien
- MIDI (Digital Instrumentation Digital Interface), Richtlinien für die Dateierstellung
- Erstellen von MIDI-Dateien, Richtlinien zum Erstellen von Dateien
- standardmäßige MIDI-patchzuweisungen
- Standard-MIDI-schlüsselzuweisungen
- Digital Instrumentation Digital Interface (MIDI), Standard-patchzuweisungen
- MIDI (Digital Instrumentation Digital Interface), Standard-patchzuweisungen
- Digital Instrumentation Digital Interface (MIDI), Standardschlüssel Zuweisungen
- MIDI (Digital Interface Digital Interface), Standardschlüssel Zuweisungen
- Erstellen von MIDI-Dateien, Standard-patchzuweisungen
- Erstellen von MIDI-Dateien, Standardschlüssel Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037519"
---
# <a name="authoring-guidelines-for-midi-files"></a>Erstellungs Richtlinien für MIDI-Dateien

Befolgen Sie diese Richtlinien, um geräteunabhängige MIDI-Dateien für Windows zu erstellen:

-   Verwenden Sie die [standardmäßigen MIDI-patchzuweisungen](standard-midi-patch-assignments.md) und die [Standard-MIDI-schlüsselzuweisungen](standard-midi-key-assignments.md).
-   Senden Sie immer eine Programm Änderungs Meldung an einen Kanal, um einen Patch auszuwählen, bevor andere Nachrichten an diesen Kanal gesendet werden. Wählen Sie für die beiden Percussion-Kanäle (10 und 16) Programmnummer 0 aus.
-   Befolgen Sie immer eine Nachricht vom Typ "MIDI-Programm ändern" mit einer Nachricht vom Typ "MIDI Main-Volume Controller" (Controller Nummer 7), um das relative Volume des Patches festzulegen.
-   Verwenden Sie für den Haupt volumecontroller den Wert 80 (0x50) für die normalen Empfangs Ebenen. Bei ruhigeren oder lauter Ebenen können Sie niedrigere oder höhere Werte verwenden.
-   Verwenden Sie nur die folgenden MIDI-Meldungen: Note-on mit Velocity, Note-Off, Programmänderung, Pitch-Kurve, Haupt Volume (Controller 7) und Dämpferpedal (Controller 64). Interne Synthesizer sind erforderlich, um auf diese Nachrichten zu reagieren, und die meisten von den meisten der von Ihnen darauf antworten.

 

 




