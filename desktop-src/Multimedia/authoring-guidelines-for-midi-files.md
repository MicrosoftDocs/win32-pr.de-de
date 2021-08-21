---
title: Richtlinien für die Erstellung von SOLLTEN-Dateien
description: Richtlinien für die Erstellung von SOLLTEN-Dateien
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Instrumentieren der digitalen Schnittstelle (KEYBOARD), Richtlinien für die Dateierstellung
- KEYBOARD (Instrument Digital Interface), Richtlinien für die Dateierstellung
- Erstellen von DATEITYP-Dateien,Richtlinien für die Dateierstellung
- STANDARDMÄßIGE PATCH-Zuweisungen
- Standardmäßige TASTENzuweisungen für DIE STANDARD-Schlüsselzuweisungen
- Instrument Digital Interface (KEYBOARD), Standard-Patchzuweisungen
- KEYBOARD (Keyboard Instrument Digital Interface), Standardpatchzuweisungen
- Instrument Digital Interface (KEYBOARD), Standardschlüsselzuweisungen
- TASTE (Instrument Digital Interface), Standardschlüsselzuweisungen
- Erstellen von FORMAT-Dateien,Standardpatchzuweisungen
- Erstellen von FORMAT-Dateien,Standardschlüsselzuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe148c2fe1bb562aad994608a8c87c35e84bccb7d63ba1bc3ee3e5dd3bbc56a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065640"
---
# <a name="authoring-guidelines-for-midi-files"></a>Richtlinien für die Erstellung von SOLLTEN-Dateien

Befolgen Sie diese Richtlinien, um geräteunabhängige FORMAT-Dateien für Windows:

-   Verwenden Sie [die Standard-FORMAT-Patchzuweisungen](standard-midi-patch-assignments.md) und [Standard-TASTE-Schlüsselzuweisungen.](standard-midi-key-assignments.md)
-   Senden Sie immer eine Programmänderungsnachricht an einen Kanal, um einen Patch auszuwählen, bevor andere Nachrichten an diesen Kanal gesendet werden. Wählen Sie für die beiden Kanäle (10 und 16) die Programmnummer 0 aus.
-   Befolgen Sie immer eine PROGRAMMÄNDERUNGsmeldung mit einer HAUPT-Volumecontroller-Meldung (Controllernummer 7) von ANTIVIRUS, um das relative Volumen des Patches fest zu legen.
-   Verwenden Sie den Wert 80 (0x50) für den Haupt-Volumecontroller für normale Lauschenebenen. Für niedrigere oder lautere Werte können Sie niedrigere oder höhere Werte verwenden.
-   Verwenden Sie nur die folgenden NOTE-Meldungen: Notiz mit Geschwindigkeit, Notiz, Programmänderung, Tonhöhe, Hauptvolumen (Controller 7) und Reglerregler (Controller 64). Interne Synthesizer sind erforderlich, um auf diese Nachrichten zu reagieren, und die meisten SYNTHESIZE-Musikinstrumenten reagieren auch darauf.

 

 




