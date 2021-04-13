---
title: Microsoft-Agent-Animationen für Genie-Zeichen
description: Microsoft-Agent-Animationen für Genie-Zeichen
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f583fc6540b5fe13cc157542d69352a8ea5b31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390315"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Microsoft-Agent-Animationen für Genie-Zeichen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das [Microsoft-Agent-Genie-Zeichen](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) ist ein urheberrechtlich geschütztes Werk der Microsoft Corporation.

Genie unterstützt die in der folgenden Tabelle aufgeführten Animationen. Informationen dazu, wie Sie die Animationen des Zeichens aufzurufen, finden Sie unter [Programmieren der Microsoft-Agent-Server Schnittstelle](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) und [Programmieren des Microsoft-agentsteuerelements](programming-the-microsoft-agent-control.md) .

Wenn Sie auf diese Zeichen Animationen mithilfe des HTTP-Protokolls und der [**Get**](get-method.md) -oder Server [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode des Steuer Elements zugreifen, sollten Sie überprüfen, wie Sie Sie herunterladen. Anstatt alle Animationen gleichzeitig herunterzuladen, können Sie zuerst die **Anzeige** -und **Sprech** Zustands Animationen abrufen. Dies ermöglicht es Ihnen, das Zeichen schnell anzuzeigen und zu sprechen, während andere Animationen asynchron heruntergeschaltet werden. Verwenden Sie außerdem das [**requestcomplete**](requestcomplete-event.md) -Ereignis, um sicherzustellen, dass die Zeichen-und Animationsdaten erfolgreich geladen werden. Wenn eine Lade Anforderung fehlschlägt, können Sie erneut versuchen, die Daten zu laden oder eine entsprechende Meldung anzuzeigen.

Wenn die **Rückgabe** Animationen einer Animation mithilfe von Beendigungs Verzweigungen definiert werden, muss Sie nicht explizit aufgerufen werden. Der-Agent **gibt die Rückgabe** Animation automatisch vor der nächsten Animation wieder. Wenn jedoch eine **Rückgabe** Animation aufgeführt ist, müssen Sie die Animation mithilfe der [**Play**](play-method.md) -Methode vor einer anderen Animation abrufen, um einen reibungslosen Übergang bereitzustellen. Wenn keine **Rückgabe** Animation aufgeführt ist, endet die Animation in der Regel ohne eine Übergangs Animation.

Die Zeichen Datei enthält Soundeffekte für eine Animation, wie in der folgenden Tabelle angegeben. Sound Effekte werden nur wiedergegeben, wenn diese Option auf der Eigenschaften Seite des Microsoft-Agents aktiviert ist. Sie können auch Soundeffekte in der Anwendung deaktivieren.



| Animation                 | Animation zurückgeben         | Unterstützt sprach | Sound Effekte | Zustand zugewiesen                            | BESCHREIBUNG                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Bestätigen**           | Keine                     | Nein                | **Nein**        | Keine                                         | Nods-Kopfzeile                                                      |
| **Warnung**                 | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Raum**                                | Ausrichten und Auslösen von Augenbrauen                                |
| **Ankündigung**              | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Löst Hand                                                    |
| **Blink**                 | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blinks-Augen                                                    |
| **Verwirrt**              | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Kratz Spitze                                                 |
| **Gratuliere**          | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Applaudiert                                                       |
| **Gratuliere \_ 2**       | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Gibt die Daumen Bewegung an                                        |
| **Ablehnen**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Löst Hände und shakes Kopf                                   |
| **DoMagic1**              | Keine                     | Ja               | **Nein**        | Keine                                         | Wechselt zur Seite und löst Hände aus                                 |
| **DoMagic2**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Senkt Hände, Clouds werden angezeigt.                                    |
| **Dontrecognize**         | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Hält Hand an Ohr                                              |
| **Explain**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Erweitert die Arme an die Seite.                                           |
| **Gesturedown**           | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingdown**                            | Gesten nach unten                                                  |
| **Gestureleft**           | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingleft**                            | Gesten Links                                                  |
| **Gestureright**          | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingright**                           | Gesten rechts                                                 |
| **Gestureup**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingup**                              | Gesten nach oben                                                    |
| **Getatgende**          | **Getattentionreturn**   | Ja               | **Nein**        | Keine                                         | Wellen-Arme                                                     |
| **Getattentionfort gesetzt** | **Getattentionreturn**   | Ja               | **Nein**        | Keine                                         | Wellen, wieder                                               |
| **Getattentionreturn**    | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                    |
| **Greet**                 | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Lang                                                           |
| **Hören \_ 1**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Ears-Erweiterung ( \* Schleifen Animation)                              |
| **Hören \_ 2**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Tilts Head Left ( \* Schleifen Animation)                          |
| **Hören \_ 3**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Schaltet die Kopfzeile ( \* Schleifen Animation).                          |
| **Hören \_ 4**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | "Head right" ( \* Schleifen Animation)                         |
| **Ausblenden**                  | Keine                     | Nein                | **Ja**       | **Zieher**                                   | In Rauch verschwinden                                          |
| **Idle1 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** IdlingLevel2                | In den Atemtest                                                   |
| **Idle1 \_ 2**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach rechts und blinkt                                       |
| **Idle1 \_ 3**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Links und blinkt                                        |
| **Idle1 \_ 4**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach rechts und blinkt                             |
| **Idle1 \_ 5**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach unten und blinkt                                        |
| **Idle1 \_ 6**              | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach oben und blinkt                                          |
| **Idle2 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | WISP-Schlangen                                                    |
| **Idle2 \_ 2**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel2**                             | Zeigt Scroll und Lesevorgänge an                                       |
| **Idle2 \_ 3**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel2**                             | Zeigt Scroll und Schreibvorgänge an                                      |
| **Idle3 \_ 1**              | Keine                     | Nein                | **Ja**       | **IdlingLevel3**                             | Gähner                                                          |
| **Idle3 \_ 2**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **IdlingLevel3**                             | Fällt in den Standbymodus ( \* Schleifen Animation)                             |
| **Suche**              | **Lookdownreturn**       | Nein                | **Nein**        | Keine                                         | Nach unten                                                     |
| **Lookdownblink**         | **Lookdownreturn**       | Nein                | **Nein**        | Keine                                         | Blinks nach unten                                            |
| **Lookdownreturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                    |
| **Lookleft**              | **Lookleftreturn**       | Nein                | **Nein**        | Keine                                         | Nach links                                                     |
| **Lookleftblink**         | **Lookleftreturn**       | Nein                | **Nein**        | Keine                                         | Links nach links                                            |
| **Lookleftreturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                    |
| **Lookright**             | **Lookrightreturn**      | Nein                | **Nein**        | Keine                                         | Nach rechts                                                    |
| **Lookrightblink**        | **Lookrightreturn**      | Nein                | **Nein**        | Keine                                         | Blinks mit rechts                                           |
| **Lookrightreturn**       | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                    |
| **Suche**                | **Lookupreturn**         | Nein                | **Nein**        | Keine                                         | Nach unten                                                       |
| **Lookupblink**           | **Lookupreturn**         | Nein                | **Nein**        | Keine                                         | Blinks nach oben                                              |
| **Lookupreturn**          | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                    |
| **Nach unten**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingdown"**                               | Nach unten                                                     |
| **"Muveleft"**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingleft"**                               | Nach links                                                     |
| **Überprüfen**             | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingright"**                              | Nach rechts                                                    |
| **MoveUp**                | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingup"**                                 | Wird nach oben                                                       |
| **Froh**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Ein Lächeln und eine Hand                                |
| **Prozess**               | Nein                       | Nein                | **Nein**        | Keine                                         | Spinnt in eine Cloud                                             |
| **Verarbeitung**            | Ja, mithilfe von Exit branches | Nein                | **Nein**        | Keine                                         | Spinnt in eine Cloud ( \* Schleifen Animation)                       |
| **Lesen**                  | **"Read Return"**           | Ja               | **Ja**       | Keine                                         | Zeigt Scroll, Lesevorgänge und Nachschlagen an                             |
| **Fortsetzung**         | **"Read Return"**           | Ja               | **Nein**        | Keine                                         | Lese-und Suchvorgänge                                             |
| **"Read Return"**            | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                    |
| **Lektüre**               | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Anzeigen von Scroll und Lesevorgängen ( \* Schleifen Animation)                  |
| **Restpose**              | Keine                     | Ja               | **Nein**        | **Isch**                                 | Neutrale Position                                               |
| **Leider**                   | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Trauriger Ausdruck                                                 |
| **Suche**                | Nein                       | Nein                | **Nein**        | Keine                                         | Zeigt das Fern-und Ausschalten an                                   |
| **Suchen**             | Ja, mithilfe von Exit branches | Nein                | **Nein**        | Keine                                         | Zeigt das Fern-und Turn-Diagramm an ( \* Schleifen Animation)             |
| **Anzeigen**                  | Keine                     | Nein                | **Ja**       | **Anzeige**                                  | Erscheint nicht in Rauch                                           |
| **Startüberwachung**        | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Legt Hand in den Ohr                                               |
| **Stoplauschen**         | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Legt die Hände über Ohren                                           |
| **Vorschlagen**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Zeigt Glühbirnen an                                             |
| **Überrascht**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Überrascht überrascht                                                |
| **Meiner**                 | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Sucht mit "Hand an Kinn"                                     |
| **Berechnung**              | Nein                       | Nein                | **Nein**        | Keine                                         | Sucht mit "Hand an Chin" ( \* Schleifen Animation)               |
| **Missverständ**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Verschiebt eine Hand zu "Chin", andere in "Hip" und löst "Right Augen w" aus. |
| **Welle**                  | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Waves                                                          |
| **Schreiben**                 | **Beschreibeturn**          | Ja               | **Ja**       | Keine                                         | Zeigt Scroll, Schreibvorgänge und Nachschlagen an                            |
| **Write-Vorgang fortgesetzt**        | **Beschreibeturn**          | Ja               | **Ja**       | Keine                                         | Schreibvorgänge und suchen                                            |
| **Beschreibeturn**           | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                                    |
| **Lassungs**               | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Zeigt Scroll, Schreibvorgänge ( \* Schleifen Animation)                   |



 

\* Wenn Sie eine Schleifen Animation wiedergeben, müssen Sie " [**Beenden**](stop-method.md) " verwenden, um Sie zu löschen, bevor andere Animationen in der Warteschlange des Zeichens abgespielt werden.

 

