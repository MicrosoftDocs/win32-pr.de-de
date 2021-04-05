---
title: Microsoft-Agent-Animationen für Robby-Zeichen
description: Microsoft-Agent-Animationen für Robby-Zeichen
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347c95fd6a29af72041d3b9e1192167d34602260
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725920"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Microsoft-Agent-Animationen für Robby-Zeichen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das [Microsoft-Agent-Robby-Zeichen](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) ist ein urheberrechtlich geschütztes Werk der Microsoft Corporation.

Robby unterstützt die in der folgenden Tabelle aufgeführten Animationen. Informationen dazu, wie Sie die Animationen des Zeichens aufzurufen, finden Sie unter [Programmieren der Microsoft-Agent-Server Schnittstelle](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) und [Programmieren des Microsoft-agentsteuerelements](programming-the-microsoft-agent-control.md) .

Wenn Sie auf diese Zeichen Animationen mithilfe des HTTP-Protokolls und der [**Get**](get-method.md) -oder Server [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode des Steuer Elements zugreifen, sollten Sie überprüfen, wie Sie Sie herunterladen. Anstatt alle Animationen gleichzeitig herunterzuladen, können Sie zuerst die **Anzeige** -und **Sprech** Zustands Animationen abrufen. Dies ermöglicht es Ihnen, das Zeichen schnell anzuzeigen und zu sprechen, während andere Animationen asynchron heruntergeschaltet werden. Verwenden Sie außerdem das [**requestcomplete**](requestcomplete-event.md) -Ereignis, um sicherzustellen, dass die Zeichen-und Animationsdaten erfolgreich geladen werden. Wenn eine Lade Anforderung fehlschlägt, können Sie erneut versuchen, die Daten zu laden oder eine entsprechende Meldung anzuzeigen.

Wenn eine Animations **Rückgabe** Animation mithilfe von Beendigungs Verzweigungen definiert wird, muss Sie nicht explizit aufgerufen werden. Der-Agent **gibt die Rückgabe** Animation automatisch vor der nächsten Animation wieder. Wenn jedoch eine **Rückgabe** Animation aufgeführt ist, müssen Sie die Animation mithilfe der [**Play**](play-method.md) -Methode vor einer anderen Animation abrufen, um einen reibungslosen Übergang bereitzustellen. Wenn keine **Rückgabe** Animation aufgeführt ist, endet die Animation in der Regel ohne eine Übergangs Animation.

Die Zeichen Datei enthält Soundeffekte für einige Animationen, wie in der folgenden Tabelle angegeben. Sound Effekte werden nur wiedergegeben, wenn diese Option auf der Eigenschaften Seite des Microsoft-Agents aktiviert ist. Sie können auch Soundeffekte in der Anwendung deaktivieren.



| Animation                 | Animation zurückgeben         | Unterstützt sprach | Sound Effekte | Zustand zugewiesen                            | BESCHREIBUNG                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Bestätigen**           | Keine                     | Nein                | **Nein**        | Keine                                         | Nods-Kopfzeile                                                  |
| **Warnung**                 | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Raum**                                | Nachrichten                                                |
| **Ankündigung**              | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Druckt Papier und Berichte                               |
| **Blink**                 | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blinks-Augen                                                |
| **Verwirrt**              | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Kratz Spitze                                             |
| **Gratuliere**          | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Löst dann die Hände aus                             |
| **Ablehnen**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Löst Hand und schüttelt Kopf                                |
| **DoMagic1**              | Keine                     | Ja               | **Nein**        | Keine                                         | Gerät entfernen                                             |
| **DoMagic2**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Drücken der Schaltfläche und des Balkens                            |
| **Dontrecognize**         | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Hält Hand an Ohr                                          |
| **Explain**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Gesten mit Waffen                                         |
| **Gesturedown**           | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingdown**                            | Gesten nach unten                                              |
| **Gestureleft**           | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingleft**                            | Gesten Links                                              |
| **Gestureright**          | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingright**                           | Gesten rechts                                             |
| **Gestureup**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingup**                              | Gesten nach oben                                                |
| **Getatgende**          | **Getattentionreturn**   | Ja               | **Nein**        | Keine                                         | Wellen-Arme                                                 |
| **Getattentionfort gesetzt** | **Getattentionreturn**   | Ja               | **Nein**        | Keine                                         | Wellen, wieder                                           |
| **Getattentionreturn**    | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                |
| **Greet**                 | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Hält an                                              |
| **Hören \_ 1**            | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **Hörvermögen**                                  | Tilts Head Right ( \* Schleifen Animation)                     |
| **Hören \_ 2**            | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **Hörvermögen**                                  | Tilts Head Left ( \* Schleifen Animation)                      |
| **Hören \_ 3**            | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **Hörvermögen**                                  | Hähne Head Left ( \* Schleifen Animation)                      |
| **Hören \_ 4**            | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **Hörvermögen**                                  | Nach unten kippen ( \* Schleifen Animation)                      |
| **Ausblenden**                  | Keine                     | Nein                | **Ja**       | **Zieher**                                   | Durch Tür verschwinden                                    |
| **Idle1 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach rechts                                              |
| **Idle1 \_ 2**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach oben und blinkt                                      |
| **Idle1 \_ 3**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach unten und blinkt                                    |
| **Idle1 \_ 4**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Links und blinkt                                    |
| **Idle2 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | Aufklappen von Waffen                                                 |
| **Idle2 \_ 2**              | Keine                     | Nein                | **Ja**       | **IdlingLevel2**                             | Entfernen von Head und vornehmen der Anpassung                          |
| **Idle3 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel3**                             | Gähner                                                      |
| **Idle3 \_ 2**              | Keine                     | Nein                | **Ja**       | **IdlingLevel3**                             | Heruntergefahren                                                 |
| **Suche**              | **Lookdownreturn**       | Nein                | **Nein**        | Keine                                         | Nach unten                                                 |
| **Lookdownreturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                |
| **Lookleft**              | **Lookleftreturn**       | Nein                | **Nein**        | Keine                                         | Nach links                                                 |
| **Lookleftreturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                |
| **Lookright**             | **Lookrightreturn**      | Nein                | **Nein**        | Keine                                         | Nach rechts                                                |
| **Lookrightreturn**       | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                |
| **Suche**                | **Lookupreturn**         | Nein                | **Nein**        | Keine                                         | Nach unten                                                   |
| **Lookupreturn**          | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                |
| **Nach unten**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingdown"**                               | Nach unten                                                 |
| **"Muveleft"**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingleft"**                               | Nach links                                                 |
| **Überprüfen**             | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingright"**                              | Nach rechts                                                |
| **MoveUp**                | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingup"**                                 | Wird nach oben                                                   |
| **Froh**               | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Lächeln und sofort                                  |
| **Prozess**               | Nein                       | Nein                | **Ja**       | Keine                                         | Drückt Schaltflächen, druckt, Lesevorgänge und schaltet dann Ausdruck ein.       |
| **Verarbeitung**            | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Drückt Schaltflächen, druckt, Lesevorgänge und schaltet dann Ausdruck ein.       |
| **Lesen**                  | **"Read Return"**           | Ja               | **Ja**       | Keine                                         | Druckt, liest und sucht nach oben                                |
| **Fortsetzung**         | **"Read Return"**           | Ja               | **Ja**       | Keine                                         | Lese-und Suchvorgänge                                         |
| **"Read Return"**            | Keine                     | Nein                | **Ja**       | Keine                                         | Kehrt zur neutralen Position zurück.                                |
| **Lektüre**               | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Druckt, liest und sucht ( \* Schleifen Animation)          |
| **Restpose**              | Keine                     | Ja               | **Nein**        | **Isch**                                 | Neutrale Position                                           |
| **Leider**                   | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Trauriger Ausdruck                                             |
| **Suche**                | Nein                       | Nein                | **Ja**       | Keine                                         | Zeigt Toolbox an und entfernt das Tool.                           |
| **Suchen**             | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Zeigt Toolbox und Entfernens von Tools ( \* Schleifen Animation)    |
| **Anzeigen**                  | Keine                     | Nein                | **Ja**       | **Anzeige**                                  | Wird durch den Tor angezeigt                                    |
| **Startüberwachung**        | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Legt Hand in den Ohr                                           |
| **Stoplauschen**         | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Legt die Hände über Ohren                                       |
| **Vorschlagen**               | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Zeigt Glühbirnen an                                         |
| **Überrascht**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Überrascht überrascht                                            |
| **Meiner**                 | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Kratz Spitze                                             |
| **Berechnung**              | Nein                       | Nein                | **Ja**       | Keine                                         | Kratz Spitze ( \* Schleifen Animation)                       |
| **Missverständ**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Shrugs                                                     |
| **Welle**                  | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Waves                                                      |
| **Schreiben**                 | **Beschreibeturn**          | Ja               | **Ja**       | Keine                                         | Zeigt den Stift und die Zwischenablage an, schreibt und sucht nach oben          |
| **Write-Vorgang fortgesetzt**        | **Beschreibeturn**          | Ja               | **Ja**       | Keine                                         | Schreibvorgänge und suchen                                        |
| **Beschreibeturn**           | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                |
| **Lassungs**               | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Zeigt den Stift und die Zwischenablage an, Schreibvorgänge ( \* Schleifen Animation) |



 

\* Wenn Sie eine Schleifen Animation wiedergeben, müssen Sie " [**Beenden**](stop-method.md) " verwenden, um Sie zu löschen, bevor andere Animationen in der Warteschlange des Zeichens abgespielt werden.

 

