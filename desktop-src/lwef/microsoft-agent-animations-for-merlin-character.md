---
title: Microsoft Agent-Animationen für Merlin-Zeichen
description: Microsoft Agent-Animationen für Merlin-Zeichen
ms.assetid: 4563a464-2c1a-4928-a471-e3f0fdfe85c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797002897f0e3bdb7efb309de8b73a33df8bdf399279895be8daa2b47d8ec084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247473"
---
# <a name="microsoft-agent-animations-for-merlin-character"></a>Microsoft Agent-Animationen für Merlin-Zeichen

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Das [Microsoft Agent Merlin-Zeichen](https://www.microsoft.com/downloads/details.aspx?FamilyID=fee1dadd-2f23-41d0-8a81-2affd74c0aa5) ist ein urheberrechtlich geschütztes Microsoft Corporation.

Merlin unterstützt die animationen, die in der folgenden Tabelle aufgeführt sind. Informationen zum Aufrufen der Animationen des Zeichens finden Sie unter Programmieren der [Microsoft Agent-Serverschnittstelle](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) und Programmieren des Microsoft Agent-Steuerelements. [](programming-the-microsoft-agent-control.md)

Wenn Sie mithilfe des HTTP-Protokolls und der [**Prepare-Methode**](get-method.md) des Steuerelements oder des Servers auf diese Zeichenanimationen zugreifen, sollten Sie überlegen, wie Sie sie herunterladen. [](/windows/desktop/lwef/iagentcharacter--prepare) Anstatt alle Animationen gleichzeitig herunterzuladen, sollten Sie  zuerst die Animationen Zum Anzeigen und Sprechen **des** Zustands abrufen. Dadurch können Sie das Zeichen schnell anzeigen und sprechen lassen, während andere Animationen asynchron heruntergefahren werden. Verwenden Sie außerdem das [**RequestComplete-Ereignis,**](requestcomplete-event.md) um sicherzustellen, dass Zeichen- und Animationsdaten erfolgreich geladen werden. Wenn bei einer Ladeanforderung ein Fehler auftritt, können Sie versuchen, die Daten erneut zu laden oder eine entsprechende Meldung anzuzeigen.

Wenn die Return-Animation einer **Animation** mit Exitbranches definiert wird, müssen Sie sie nicht explizit aufrufen. Der Agent gibt die **Return-Animation** automatisch vor der nächsten Animation wieder. Wenn jedoch eine **Return-Animation** aufgeführt wird, müssen Sie die Animation mithilfe der [**Play-Methode**](play-method.md) vor einer anderen Animation aufrufen, um einen reibungslosen Übergang zu ermöglichen. Wenn keine **Rückgabeanimation** aufgeführt wird, endet die Animation in der Regel, ohne dass eine Übergangsanimation erforderlich ist.

Die Zeichendatei enthält Soundeffekte für einige Animationen, wie in der folgenden Tabelle angegeben. Soundeffekte werden nur dann wieder verwendet, wenn diese Option im Microsoft Agent-Eigenschaftenblatt aktiviert ist. Sie können auch Soundeffekte in Ihrer Anwendung deaktivieren.



| Animation                 | Rückgabeanimation         | Unterstützt Sprech | Soundeffekte | Zustand zugewiesen                            | BESCHREIBUNG                                      |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------|
| **Bestätigen**           | Keine                     | Nein                | **Nein**        | Keine                                         | Nods head                                        |
| **Warnung**                 | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **Hören**                                | Begradigt und löst Augenbrowsen aus                  |
| **Verkünden**              | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Löst Einspielung und Spiele aus                         |
| **Blink**                 | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blinkende Augen                                      |
| **Verwirrt**              | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Scratches head (Kopf ab scratcht)                                   |
| **Gratulieren**          | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Preisanzeigen                                  |
| **\_2. Januar 2016**       | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Begrüßt                                         |
| **Ablehnen**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hebt die Hände und schüttelt den Kopf                     |
| **DoMagic1**              | Keine                     | Ja               | **Nein**        | Keine                                         | Löst Magic Wall aus                                |
| **DoMagic2**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Versenkte Wand, Clouds werden angezeigt                       |
| **DontRecognize**         | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hand-zu-Hand-an-Hand-Hand                                |
| **Explain**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Erweitert die Arme auf die Seite                             |
| **GestureDown**           | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingDown**                            | Gesten nach unten                                    |
| **GestureLeft**           | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingLeft**                            | Gesten links                                    |
| **GestureRight**          | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingRight**                           | Gesten rechts                                   |
| **GestureUp**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingUp**                              | Gesten nach oben                                      |
| **GetAttention**          | **GetAttentionReturn**   | Ja               | **Ja**       | Keine                                         | Lehnt sich vorwärts und lehnt                         |
| **GetAttentionContinued** | **GetAttentionReturn**   | Ja               | **Ja**       | Keine                                         | Lehnend nach vorn, Schläge wieder                    |
| **GetAttentionReturn**    | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                      |
| **Greet**                 | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Bögen                                             |
| **Hörvermögen \_ 1**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Extend-Schleife \* (Schleifenanimation)                |
| **Hörvermögen \_ 2**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Kippt den Kopf nach links \* (Schleifenanimation)            |
| **Hörvermögen \_ 3**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Kehrt den Kopf nach links \* (Schleifenanimation) um.            |
| **Hörvermögen \_ 4**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Wendet den Kopf nach rechts \* (Schleifenanimation)           |
| **Ausblenden**                  | Keine                     | Nein                | **Ja**       | **Versteckt**                                   | Verschwindet unter der Obergrenze                             |
| **Idle1 \_ 1**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Übernimmt die                                     |
| **Idle1 \_ 2**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach links und Blinken                          |
| **Idle1 \_ 3**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach rechts                                    |
| **Idle1 \_ 4**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach rechts und blinken               |
| **Idle2 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | Sieht die Wand und blinkt                         |
| **Idle2 \_ 2**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | Halten der Hände und Blinken                           |
| **Idle3 \_ 1**              | Keine                     | Nein                | **Ja**       | **IdlingLevel3**                             | Yawns                                            |
| **Idle3 \_ 2**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **IdlingLevel3**                             | In den Unterlauf \* (Schleifenanimation)               |
| **LookDown**              | **LookDownReturn**       | Nein                | **Nein**        | Keine                                         | Nach unten                                       |
| **LookDownBlink**         | **LookDownReturn**       | Nein                | **Nein**        | Keine                                         | Blinken nach unten                              |
| **LookDownReturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                      |
| **LookLeft**              | **LookLeftReturn**       | Nein                | **Nein**        | Keine                                         | Sieht links aus                                       |
| **LookLeftBlink**         | **LookLeftReturn**       | Nein                | **Nein**        | Keine                                         | Blinken nach links                              |
| **LookLeftReturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                      |
| **LookRight**             | **LookRightReturn**      | Nein                | **Nein**        | Keine                                         | Sieht richtig aus                                      |
| **LookRightBlink**        | **LookRightReturn**      | Nein                | **Nein**        | Keine                                         | Blinks looking right (Blinken nach rechts)                             |
| **LookRightReturn**       | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                      |
| **Lookup**                | **LookUpReturn**         | Nein                | **Nein**        | Keine                                         | Sucht nach                                         |
| **LookUpBlink**           | **LookUpReturn**         | Nein                | **Nein**        | Keine                                         | Blinkt nachschlagen                                |
| **LookUpReturn**          | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                      |
| **Movedown**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingDown**                               | Abknaben                                       |
| **MoveLeft**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingLeft**                               | Links von Links                                       |
| **MoveRight**             | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingRight**                              | Rechts vom 5.00                                      |
| **MoveUp**                | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingUp**                                 | Nach oben                                         |
| **Zufrieden**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Lächeln und Halten der Hände                  |
| **Process**               | Nein                       | Nein                | **Ja**       | Keine                                         | Stirs caldron                                    |
| **Verarbeitung**            | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Stirs caldron \* (Loopinganimation)              |
| **Lesen**                  | **ReadReturn**           | Ja               | **Ja**       | Keine                                         | Öffnet das Buch, liest und sucht nach.                   |
| **ReadContinued**         | **ReadReturn**           | Ja               | **Ja**       | Keine                                         | Liest und sucht                               |
| **ReadReturn**            | Keine                     | Nein                | **Ja**       | Keine                                         | Zurück zur neutralen Position                      |
| **Aktuell gelesen**               | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Liest ( \* Schleifenanimation)                      |
| **RestPose**              | Keine                     | Ja               | **Nein**        | **Sprechen**                                 | Neutrale Position                                 |
| **Traurig**                   | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Leiderer Ausdruck                                   |
| **Suche**                | Nein                       | Nein                | **Ja**       | Keine                                         | Sucht in die Ballkugel                          |
| **Suche**             | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Sucht in die Ballkugel ( \* Schleifenanimation)    |
| **Anzeigen**                  | Keine                     | Nein                | **Ja**       | **Anzeige**                                  | Wird nicht mehr in der Obergrenze angezeigt                               |
| **StartListening**        | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hand ans Hand-An-Hand-Tor                                 |
| **StopListening**         | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Legt Hand über Kopf                             |
| **Vorschlagen**               | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Zeigt eine Glühbirne an                               |
| **Überrascht**             | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Sieht überraschend aus                                  |
| **Denke**                 | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Sucht mit der Hand auf dem Kinn                       |
| **Berechnung**              | Nein                       | Nein                | **Nein**        | Keine                                         | Sucht mit der Hand auf dem Kinn ( \* Schleifenanimation) |
| **Unsicher**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Verschwenkt nach vorn und löst augengedrehte Augen aus                 |
| **Welle**                  | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Wellen                                            |
| **Schreiben**                 | **WriteReturn**          | Ja               | **Ja**       | Keine                                         | Öffnet buch, schreibt und sucht nach                  |
| **WriteContinued**        | **WriteReturn**          | Ja               | **Ja**       | Keine                                         | Schreibt und sucht                              |
| **WriteReturn**           | Keine                     | Nein                | **Ja**       | Keine                                         | Kehrt zur neutralen Position zurück                      |
| **Schreiben**               | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Schreibvorgänge ( \* Schleifenanimation)                     |



 

\* Wenn Sie eine Schleifenanimation wiedergeben, müssen Sie [**beenden**](stop-method.md) verwenden, um sie zu löschen, bevor andere Animationen in der Warteschlange des Zeichens wiedergegeben werden.

 

