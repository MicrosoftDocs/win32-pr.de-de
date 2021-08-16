---
title: Microsoft Agent-Animationen für Zeichen
description: Microsoft Agent-Animationen für Zeichen
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef6cf0fc3d44f9783fe3d22f9f0d2b291e6acc51bd5bb72890af793ffe55156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609100"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Microsoft Agent-Animationen für Zeichen

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Das [Microsoft Agent-Zeichen ist](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) ein urheberrechtlich geschütztes Microsoft Corporation.

Animationsy unterstützt die animationen, die in der folgenden Tabelle aufgeführt sind. Informationen zum Aufrufen der Animationen des Zeichens finden Sie unter Programmieren der [Microsoft Agent-Serverschnittstelle](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) und Programmieren des Microsoft Agent-Steuerelements. [](programming-the-microsoft-agent-control.md)

Wenn Sie mithilfe des HTTP-Protokolls und der [**Prepare-Methode**](get-method.md) des -Steuerelements oder des Servers auf diese Zeichenanimationen zugreifen, überlegen Sie, wie Sie sie herunterladen. [](/windows/desktop/lwef/iagentcharacter--prepare) Anstatt alle Animationen gleichzeitig herunterzuladen, sollten Sie  zuerst die Animationen zum Anzeigen und **sprechenden** Zustand abrufen. Dadurch können Sie das Zeichen schnell anzeigen und sprechen lassen, während andere Animationen asynchron heruntergefahren werden. Verwenden Sie außerdem das [**RequestComplete-Ereignis,**](requestcomplete-event.md) um sicherzustellen, dass Zeichen- und Animationsdaten erfolgreich geladen werden. Wenn bei einer Ladeanforderung ein Fehler auftritt, können Sie versuchen, die Daten zu laden oder eine entsprechende Meldung anzuzeigen.

Wenn die Return-Animation einer **Animation** mit Exitbranches definiert wird, müssen Sie sie nicht explizit aufrufen. Der Agent gibt die **Return-Animation automatisch** vor der nächsten Animation wieder. Wenn jedoch eine **Return-Animation** aufgeführt wird, müssen Sie die Animation mit der [**Play-Methode**](play-method.md) vor einer anderen Animation aufrufen, um einen reibungslosen Übergang zu ermöglichen. Wenn  keine Rückgabeanimation aufgeführt wird, endet die Animation in der Regel, ohne dass eine Übergangsanimation erforderlich ist.

Die Zeichendatei enthält Soundeffekte für einige Animationen, wie in der folgenden Tabelle angegeben. Soundeffekte werden nur dann wieder verwendet, wenn diese Option im Microsoft Agent-Eigenschaftenblatt aktiviert ist. Sie können auch Soundeffekte in Ihrer Anwendung deaktivieren.



| Animation                 | Rückgabeanimation         | Unterstützt Sprech | Soundeffekte | Zustand zugewiesen                            | BESCHREIBUNG                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Bestätigen**           | Keine                     | Nein                | **Nein**        | Keine                                         | Nods head                                                  |
| **Warnung**                 | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **Hören**                                | Begradigt                                                |
| **Verkünden**              | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Druckt Papier und Berichte                               |
| **Blink**                 | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blinkende Augen                                                |
| **Verwirrt**              | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Scratches head                                             |
| **Gratulieren**          | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hebt die Hände und klammert die Hände.                             |
| **Ablehnen**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hebt die Hand und schüttelt den Kopf                                |
| **DoMagic1**              | Keine                     | Ja               | **Nein**        | Keine                                         | Entfernt das Gerät.                                             |
| **DoMagic2**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Schaltfläche und Balken werden gedrückt                            |
| **DontRecognize**         | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hand-zu-Hand-an-Hand-Hand                                          |
| **Explain**               | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Gesten mit Denn                                         |
| **GestureDown**           | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingDown**                            | Gesten nach unten                                              |
| **GestureLeft**           | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingLeft**                            | Gesten nach links                                              |
| **GestureRight**          | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingRight**                           | Gesten nach rechts                                             |
| **GestureUp**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | **GesturingUp**                              | Gesten nach oben                                                |
| **GetAttention**          | **GetAttentionReturn**   | Ja               | **Nein**        | Keine                                         | Wellenarme                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Ja               | **Nein**        | Keine                                         | Wellenwappen erneut                                           |
| **GetAttentionReturn**    | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück                                |
| **Greet**                 | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Hält die Hand hoch                                              |
| **Hörvermögen \_ 1**            | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **Hörvermögen**                                  | Neigungen nach rechts ( \* Schleifenanimation)                     |
| **Hörvermögen \_ 2**            | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **Hörvermögen**                                  | Neigungen nach links ( \* Schleifenanimation)                      |
| **Hörvermögen \_ 3**            | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **Hörvermögen**                                  | Cocks head left \* (Loopinganimation)                      |
| **Hörvermögen \_ 4**            | Ja, Verwenden von Exitbranches | Nein                | **Nein**        | **Hörvermögen**                                  | Neigungen nach unten \* (Schleifenanimation)                      |
| **Ausblenden**                  | Keine                     | Nein                | **Ja**       | **Versteckt**                                   | Verschwindet durch Die Tür                                    |
| **Idle1 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blick nach rechts                                              |
| **Idle1 \_ 2**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach oben und Blinken                                      |
| **Idle1 \_ 3**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blick nach unten und Blinken                                    |
| **Idle1 \_ 4**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blicke nach links und Blinken                                    |
| **Idle2 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | Verschränkt die Arme                                                 |
| **Idle2 \_ 2**              | Keine                     | Nein                | **Ja**       | **IdlingLevel2**                             | Entfernt den Kopf und stellt die Anpassung vor.                          |
| **Idle3 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel3**                             | Yawns                                                      |
| **Idle3 \_ 2**              | Keine                     | Nein                | **Ja**       | **IdlingLevel3**                             | Wird heruntergefahren                                                 |
| **LookDown**              | **LookDownReturn**       | Nein                | **Nein**        | Keine                                         | Nach unten                                                 |
| **LookDownReturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                                |
| **LookLeft**              | **LookLeftReturn**       | Nein                | **Nein**        | Keine                                         | Sieht links aus                                                 |
| **LookLeftReturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                                |
| **LookRight**             | **LookRightReturn**      | Nein                | **Nein**        | Keine                                         | Sieht richtig aus                                                |
| **LookRightReturn**       | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                                |
| **Lookup**                | **LookUpReturn**         | Nein                | **Nein**        | Keine                                         | Sucht nach                                                   |
| **LookUpReturn**          | Keine                     | Nein                | **Nein**        | Keine                                         | Zurück zur neutralen Position                                |
| **Movedown**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingDown**                               | Abknaben                                                 |
| **MoveLeft**              | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingLeft**                               | Links von Links                                                 |
| **MoveRight**             | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingRight**                              | Rechts vom 5.00                                                |
| **MoveUp**                | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | **MovingUp**                                 | Nach oben                                                   |
| **Zufrieden**               | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Lächeln und Begradign                                  |
| **Process**               | Nein                       | Nein                | **Ja**       | Keine                                         | Drückt Schaltflächen, druckt, liest und wirft dann den Druck       |
| **Verarbeitung**            | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Drückt Schaltflächen, druckt, liest und wirft dann den Ausdruck.       |
| **Lesen**                  | **ReadReturn**           | Ja               | **Ja**       | Keine                                         | Druckt, liest und sucht                                |
| **ReadContinued**         | **ReadReturn**           | Ja               | **Ja**       | Keine                                         | Liest und sucht                                         |
| **ReadReturn**            | Keine                     | Nein                | **Ja**       | Keine                                         | Kehrt zur neutralen Position zurück                                |
| **Aktuell gelesen**               | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Druckt, liest und sucht nach ( \* Schleifenanimation)          |
| **RestPose**              | Keine                     | Ja               | **Nein**        | **Sprechen**                                 | Neutrale Position                                           |
| **Traurig**                   | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Leiderer Ausdruck                                             |
| **Suche**                | Nein                       | Nein                | **Ja**       | Keine                                         | Zeigt die Toolbox an und entfernt das Tool.                           |
| **Suche**             | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Zeigt die Toolbox an und entfernt Tools ( \* Schleifenanimation)    |
| **Anzeigen**                  | Keine                     | Nein                | **Ja**       | **Anzeige**                                  | Wird über doorway angezeigt.                                    |
| **StartListening**        | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Legt Die Hand an das Hörhörnchen                                           |
| **StopListening**         | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Legt Hand über Kopf                                       |
| **Vorschlagen**               | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Zeigt eine Glühbirne an                                         |
| **Überrascht**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Sieht überraschend aus                                            |
| **Denke**                 | Ja, Verwenden von Exitbranches | Ja               | **Ja**       | Keine                                         | Scratches Head                                             |
| **Berechnung**              | Nein                       | Nein                | **Ja**       | Keine                                         | Scratches head \* (Loopinganimation)                       |
| **Unsicher**             | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Zuckt                                                     |
| **Welle**                  | Ja, Verwenden von Exitbranches | Ja               | **Nein**        | Keine                                         | Wellen                                                      |
| **Schreiben**                 | **WriteReturn**          | Ja               | **Ja**       | Keine                                         | Zeigt Stift und Zwischenablage an, schreibt und sucht nach          |
| **WriteContinued**        | **WriteReturn**          | Ja               | **Ja**       | Keine                                         | Schreibt und sucht                                        |
| **WriteReturn**           | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück                                |
| **Schreiben**               | Ja, Verwenden von Exitbranches | Nein                | **Ja**       | Keine                                         | Zeigt Stift und Zwischenablage, Schreibvorgänge ( \* Schleifenanimation) an. |



 

\* Wenn Sie eine Schleifenanimation wiedergeben, müssen Sie [**beenden**](stop-method.md) verwenden, um sie zu löschen, bevor andere Animationen in der Warteschlange des Zeichens wiedergegeben werden.

 

