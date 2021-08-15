---
title: Richtlinien für die Erstellung von DATEIEN
description: Richtlinien für die Erstellung von DATEIEN
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Music Instrument Digital Interface (DOSSIER), Richtlinien für die Dateierstellung
- INSTRUMENTS (Music Instrument Digital Interface),Richtlinien für die Dateierstellung
- Erstellen von DATEIEN, Richtlinien für die Dateierstellung
- STANDARDMÄßIGE PATCH-Zuweisungen
- STANDARDMÄßIGE ZUWEISUNGEN VON SCHLÜSSELN
- Music Instrument Digital Interface (OPC), Standardpatchzuweisungen
- INSTRUMENTS (Music Instrument Digital Interface), Standardpatchzuweisungen
- Music Instrument Digital Interface (TASTE), Standardschlüsselzuweisungen
- INSTRUMENTS (Music Instrument Digital Interface), Standardschlüsselzuweisungen
- Erstellen von TEXTDATEI-Dateien, Standardpatchzuweisungen
- Erstellen von DATEIEN, Standardschlüsselzuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe148c2fe1bb562aad994608a8c87c35e84bccb7d63ba1bc3ee3e5dd3bbc56a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065640"
---
# <a name="authoring-guidelines-for-midi-files"></a>Richtlinien für die Erstellung von DATEIEN

Befolgen Sie diese Richtlinien, um geräteunabhängige DATEIEN für Windows zu erstellen:

-   Verwenden Sie die [Standard-PATCH-Zuweisungen UND](standard-midi-patch-assignments.md) [STANDARDMÄßIGE SCHLÜSSELZUWEISUNGEN](standard-midi-key-assignments.md).
-   Senden Sie immer eine Programmänderungsnachricht an einen Kanal, um einen Patch auszuwählen, bevor Sie andere Nachrichten an diesen Kanal senden. Wählen Sie für die beiden Kanäle (10 und 16) programmnummer 0 aus.
-   Folgen Sie immer einer MELDUNG zum Ändern des PROGRAMMS mit einer CONTROLLER-Hauptvolume-Controllermeldung (Controllernummer 7), um das relative Volume des Patches festzulegen.
-   Verwenden Sie den Wert 80 (0x50) für den Hauptvolumecontroller für normale Überwachungsebenen. Für stillere oder lautere Ebenen können Sie niedrigere oder höhere Werte verwenden.
-   Verwenden Sie nur die folgenden MELDUNGEN vom Folgenden: Note-On mit Geschwindigkeit, Hinweis, Programmänderung, Tonhöhenhöhe, Hauptvolumen (Controller 7) und Klappenband (Controller 64). Interne Synthesizer sind erforderlich, um auf diese Nachrichten zu reagieren, und die meisten INSTRUMENT-Instrumenten reagieren auch darauf.

 

 




