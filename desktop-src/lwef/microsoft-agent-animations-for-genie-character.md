---
title: Microsoft Agent-Animationen für Figurzeichen
description: Microsoft Agent-Animationen für Figurzeichen
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204da244b74e96e239d540662dabf73af82001748b395da8e660f53fe4cf85e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976100"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Microsoft Agent-Animationen für Figurzeichen

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Das [Microsoft Agent -Zeichen ist](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) ein urheberrechtlich geschütztes Microsoft Corporation.

Dabei werden die animationen unterstützt, die in der folgenden Tabelle aufgeführt sind. Informationen zum Aufrufen der Animationen des Zeichens finden Sie unter Programmieren der [Microsoft Agent-Serverschnittstelle](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) und Programmieren des Microsoft Agent-Steuerelements. [](programming-the-microsoft-agent-control.md)

Wenn Sie mithilfe des HTTP-Protokolls und der [**Prepare-Methode**](get-method.md) des -Steuerelements oder des Servers auf diese Zeichenanimationen zugreifen, überlegen Sie, wie Sie sie herunterladen. [](/windows/desktop/lwef/iagentcharacter--prepare) Anstatt alle Animationen gleichzeitig herunterzuladen, sollten Sie  zuerst die Animationen zum Anzeigen und **sprechenden** Zustand abrufen. Dadurch können Sie das Zeichen schnell anzeigen und sprechen lassen, während andere Animationen asynchron heruntergefahren werden. Verwenden Sie außerdem das [**RequestComplete-Ereignis,**](requestcomplete-event.md) um sicherzustellen, dass Zeichen- und Animationsdaten erfolgreich geladen werden. Wenn bei einer Ladeanforderung ein Fehler auftritt, können Sie versuchen, die Daten zu laden oder eine entsprechende Meldung anzuzeigen.

Wenn die **Rückgabeanimationen** einer Animation mit Exitbranches definiert werden, müssen Sie sie nicht explizit aufrufen. Der Agent gibt die **Return-Animation automatisch** vor der nächsten Animation wieder. Wenn jedoch eine **Return-Animation** aufgeführt wird, müssen Sie die Animation mit der [**Play-Methode**](play-method.md) vor einer anderen Animation aufrufen, um einen reibungslosen Übergang zu ermöglichen. Wenn  keine Rückgabeanimation aufgeführt wird, endet die Animation in der Regel, ohne dass eine Übergangsanimation erforderlich ist.

Die Zeichendatei enthält Soundeffekte für einige Animationen, wie in der folgenden Tabelle angegeben. Soundeffekte werden nur dann wieder verwendet, wenn diese Option im Microsoft Agent-Eigenschaftenblatt aktiviert ist. Sie können auch Soundeffekte in Ihrer Anwendung deaktivieren.



| Animation                 | Rückgabeanimation         | Unterstützt Sprech | Soundeffekte | Zustand zugewiesen                            | BESCHREIBUNG                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Bestätigen**           | Keine                     | Nein                | **Nein**        | Keine                                         | Nods head                                                      |
| **Warnung**                 | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **Hören**                                | Begradigt und löst Augenbrowsen aus                                |
| **Verkünden**              | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Löst Hand aus                                                    |
| **Blink**                 | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blinkende Augen                                                    |
| **Verwirrt**              | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Scratches head                                                 |
| **Gratulieren**          | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Begrüßt                                                       |
| **\_2. Januar 2016**       | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Gibt die Geste "Daumen nach oben"                                        |
| **Ablehnen**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hebt die Hände und schüttelt den Kopf                                   |
| **DoMagic1**              | Keine                     | Ja               | **Nein**        | Keine                                         | Kehrt zur Seite und hebt die Hände                                 |
| **DoMagic2**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Senken der Hände, Clouds werden angezeigt                                    |
| **DontRecognize**         | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hand-zu-Hand-an-Hand-Hand                                              |
| **Explain**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Erweitert Die Arme auf die Seite                                           |
| **GestureDown**           | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingDown**                            | Gesten nach unten                                                  |
| **GestureLeft**           | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingLeft**                            | Gesten nach links                                                  |
| **GestureRight**          | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingRight**                           | Gesten nach rechts                                                 |
| **GestureUp**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingUp**                              | Gesten nach oben                                                    |
| **GetAttention**          | **GetAttentionReturn**   | Ja               | **Nein**        | Keine                                         | Wellenarme                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Ja               | **Nein**        | Keine                                         | Wellenwappen erneut                                               |
| **GetAttentionReturn**    | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück                                    |
| **Greet**                 | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Bögen                                                           |
| **Hörvermögen \_ 1**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Verlängerungserweiterung ( \* Schleifenanimation)                              |
| **Hörvermögen \_ 2**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Neigungen nach links ( \* Schleifenanimation)                          |
| **Hörvermögen \_ 3**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Drehen des Kopfes nach links \* (Schleifenanimation)                          |
| **Hörvermögen \_ 4**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Kehrt den Kopf nach rechts ( \* Schleifenanimation)                         |
| **Ausblenden**                  | Keine                     | Nein                | **Ja**       | **Versteckt**                                   | Verschwindet in Qualm                                          |
| **Idle1 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** IdlingLevel2                | Nimmt einen 100-Prozent                                                   |
| **Idle1 \_ 2**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach rechts und blinkt                                       |
| **Idle1 \_ 3**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach links und Blinken                                        |
| **Idle1 \_ 4**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blick nach rechts und blinkt                             |
| **Idle1 \_ 5**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blick nach unten und Blinken                                        |
| **Idle1 \_ 6**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach oben und Blinken                                          |
| **Idle2 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | Wisp-Gänge                                                    |
| **Idle2 \_ 2**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel2**                             | Zeigt Bildlauf und Lesefunktionen an                                       |
| **Idle2 \_ 3**              | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **IdlingLevel2**                             | Zeigt Bildlauf und Schreibvorgänge an                                      |
| **Idle3 \_ 1**              | Keine                     | Nein                | **Ja**       | **IdlingLevel3**                             | Yawns                                                          |
| **Idle3 \_ 2**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **IdlingLevel3**                             | Falls a sleep \* (Schleifenanimation)                             |
| **LookDown**              | **LookDownReturn**       | Nein                | **Nein**        | Keine                                         | Nach unten                                                     |
| **LookDownBlink**         | **LookDownReturn**       | Nein                | **Nein**        | Keine                                         | Blinkt nach unten                                            |
| **LookDownReturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück                                    |
| **LookLeft**              | **LookLeftReturn**       | Nein                | **Nein**        | Keine                                         | Sieht nach links aus.                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | Nein                | **Nein**        | Keine                                         | Blinkt nach links                                            |
| **LookLeftReturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück                                    |
| **LookRight**             | **LookRightReturn**      | Nein                | **Nein**        | Keine                                         | Sieht richtig aus                                                    |
| **LookRightBlink**        | **LookRightReturn**      | Nein                | **Nein**        | Keine                                         | Blinkt nach rechts                                           |
| **LookRightReturn**       | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück                                    |
| **Lookup**                | **LookUpReturn**         | Nein                | **Nein**        | Keine                                         | Sucht nach                                                       |
| **LookUpBlink**           | **LookUpReturn**         | Nein                | **Nein**        | Keine                                         | Blinks looking up (Blinken nach oben)                                              |
| **LookUpReturn**          | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                                    |
| **Movedown**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingDown**                               | Abknaben                                                     |
| **MoveLeft**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingLeft**                               | Links von Links                                                     |
| **MoveRight**             | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingRight**                              | Rechts vom 5.00                                                    |
| **MoveUp**                | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingUp**                                 | Nach oben                                                       |
| **Zufrieden**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Lächeln und Halten der Hände                                |
| **Process**               | Nein                       | Nein                | **Nein**        | Keine                                         | Spins in einer Cloud                                             |
| **Verarbeitung**            | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | Keine                                         | Drehungen in einer Cloud ( \* Schleifenanimation)                       |
| **Lesen**                  | **ReadReturn**           | Ja               | **Ja**       | Keine                                         | Zeigt bildlauf, liest und sucht nach.                             |
| **ReadContinued**         | **ReadReturn**           | Ja               | **Nein**        | Keine                                         | Liest und sucht                                             |
| **ReadReturn**            | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                                    |
| **Aktuell gelesen**               | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Reveal scroll and reads ( looping animation) (Reveal scroll and reads ( \* Loopinganimation)                  |
| **RestPose**              | Keine                     | Ja               | **Nein**        | **Sprechen**                                 | Neutrale Position                                               |
| **Traurig**                   | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Leiderer Ausdruck                                                 |
| **Suche**                | Nein                       | Nein                | **Nein**        | Keine                                         | Zeigt Binoken und Turns an                                   |
| **Suche**             | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | Keine                                         | Zeigt Binokulare und Turns an \* (Schleifenanimation)             |
| **Anzeigen**                  | Keine                     | Nein                | **Ja**       | **Anzeige**                                  | Wird aus dem Feuer heraus angezeigt                                           |
| **StartListening**        | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Legt Die Hand an das Hörhörnchen                                               |
| **StopListening**         | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Legt Hand über Kopf                                           |
| **Vorschlagen**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Zeigt eine Glühbirne an                                             |
| **Überrascht**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Sieht überraschend aus                                                |
| **Denke**                 | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Sucht mit der Hand auf dem Kinn                                     |
| **Berechnung**              | Nein                       | Nein                | **Nein**        | Keine                                         | Sucht mit der Hand auf dem Kinn ( \* Schleifenanimation)               |
| **Unsicher**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Verschiebt eine Hand an das Kinn, eine andere an die Hip und löst die rechte Augenbrow aus. |
| **Welle**                  | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Wellen                                                          |
| **Schreiben**                 | **WriteReturn**          | Ja               | **Ja**       | Keine                                         | Zeigt Scrollen, Schreibt und sucht nach                            |
| **WriteContinued**        | **WriteReturn**          | Ja               | **Ja**       | Keine                                         | Schreibt und sucht                                            |
| **WriteReturn**           | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück                                    |
| **Schreiben**               | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Zeigt Bildlauf und Schreibvorgänge an ( \* Schleifenanimation)                   |



 

\* Wenn Sie eine Schleifenanimation wiedergeben, müssen Sie [**beenden**](stop-method.md) verwenden, um sie zu löschen, bevor andere Animationen in der Warteschlange des Zeichens wiedergegeben werden.

 

