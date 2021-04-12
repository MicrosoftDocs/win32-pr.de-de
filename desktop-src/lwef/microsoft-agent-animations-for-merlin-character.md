---
title: Microsoft-Agent-Animationen für Merlin-Zeichen
description: Microsoft-Agent-Animationen für Merlin-Zeichen
ms.assetid: 4563a464-2c1a-4928-a471-e3f0fdfe85c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5138dab8b3a4d411226cfe03b9341a73f301c037
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315039"
---
# <a name="microsoft-agent-animations-for-merlin-character"></a>Microsoft-Agent-Animationen für Merlin-Zeichen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das [Microsoft-Agent-Zeichen (Merlin](https://www.microsoft.com/downloads/details.aspx?FamilyID=fee1dadd-2f23-41d0-8a81-2affd74c0aa5) ) ist ein urheberrechtlich geschütztes Werk der Microsoft Corporation.

Merlin unterstützt die in der folgenden Tabelle aufgeführten Animationen. Informationen dazu, wie Sie die Animationen des Zeichens aufzurufen, finden Sie unter [Programmieren der Microsoft-Agent-Server Schnittstelle](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) und [Programmieren des Microsoft-agentsteuerelements](programming-the-microsoft-agent-control.md) .

Wenn Sie auf diese Zeichen Animationen mithilfe des HTTP-Protokolls und der [**Get**](get-method.md) -oder Server [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode des Steuer Elements zugreifen, sollten Sie überprüfen, wie Sie Sie herunterladen. Anstatt alle Animationen gleichzeitig herunterzuladen, können Sie zuerst die **Anzeige** -und **Sprech** Zustands Animationen abrufen. Dies ermöglicht es Ihnen, das Zeichen schnell anzuzeigen und zu sprechen, während andere Animationen asynchron heruntergeschaltet werden. Verwenden Sie außerdem das [**requestcomplete**](requestcomplete-event.md) -Ereignis, um sicherzustellen, dass die Zeichen-und Animationsdaten erfolgreich geladen werden. Wenn eine Lade Anforderung fehlschlägt, können Sie erneut versuchen, die Daten zu laden oder eine entsprechende Meldung anzuzeigen.

Wenn eine Animations **Rückgabe** Animation mithilfe von Beendigungs Verzweigungen definiert wird, muss Sie nicht explizit aufgerufen werden. Der-Agent **gibt die Rückgabe** Animation automatisch vor der nächsten Animation wieder. Wenn jedoch eine **Rückgabe** Animation aufgeführt ist, müssen Sie die Animation mithilfe der [**Play**](play-method.md) -Methode vor einer anderen Animation abrufen, um einen reibungslosen Übergang bereitzustellen. Wenn keine **Rückgabe** Animation aufgeführt ist, endet die Animation in der Regel ohne eine Übergangs Animation.

Die Zeichen Datei enthält Soundeffekte für einige Animationen, wie in der folgenden Tabelle angegeben. Sound Effekte werden nur wiedergegeben, wenn diese Option auf der Eigenschaften Seite des Microsoft-Agents aktiviert ist. Sie können auch Soundeffekte in der Anwendung deaktivieren.



| Animation                 | Animation zurückgeben         | Unterstützt sprach | Sound Effekte | Zustand zugewiesen                            | BESCHREIBUNG                                      |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------|
| **Bestätigen**           | Keine                     | Nein                | **Nein**        | Keine                                         | Nods-Kopfzeile                                        |
| **Warnung**                 | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Raum**                                | Ausrichten und Auslösen von Augenbrauen                  |
| **Ankündigung**              | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Löst Trompete aus und spielt                         |
| **Blink**                 | Keine                     | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Blinks-Augen                                      |
| **Verwirrt**              | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Kratz Spitze                                   |
| **Gratuliere**          | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Zeigt eine Trophäe an                                  |
| **Gratuliere \_ 2**       | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Applaudiert                                         |
| **Ablehnen**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Löst Hände und shakes Kopf                     |
| **DoMagic1**              | Keine                     | Ja               | **Nein**        | Keine                                         | Löst Magic Wand aus                                |
| **DoMagic2**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Der Wand wird verringert, Clouds werden angezeigt                       |
| **Dontrecognize**         | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Hält Hand an Ohr                                |
| **Explain**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Erweitert die Arme an die Seite.                             |
| **Gesturedown**           | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingdown**                            | Gesten nach unten                                    |
| **Gestureleft**           | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingleft**                            | Gesten Links                                    |
| **Gestureright**          | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingright**                           | Gesten rechts                                   |
| **Gestureup**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | **Gesturingup**                              | Gesten nach oben                                      |
| **Getatgende**          | **Getattentionreturn**   | Ja               | **Ja**       | Keine                                         | Wird vorwärts und-Knöpfe                         |
| **Getattentionfort gesetzt** | **Getattentionreturn**   | Ja               | **Ja**       | Keine                                         | Weiterleiten, wird wiederholt                    |
| **Getattentionreturn**    | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                      |
| **Greet**                 | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Lang                                             |
| **Hören \_ 1**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Ears-Erweiterung ( \* Schleifen Animation)                |
| **Hören \_ 2**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Tilts Head Left ( \* Schleifen Animation)            |
| **Hören \_ 3**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | Schaltet die Kopfzeile ( \* Schleifen Animation).            |
| **Hören \_ 4**            | Keine                     | Nein                | **Nein**        | **Hörvermögen**                                  | "Head right" ( \* Schleifen Animation)           |
| **Ausblenden**                  | Keine                     | Nein                | **Ja**       | **Zieher**                                   | Untergrenze verschwindet                             |
| **Idle1 \_ 1**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | In den Atemtest                                     |
| **Idle1 \_ 2**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Links und blinkt                          |
| **Idle1 \_ 3**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach rechts                                    |
| **Idle1 \_ 4**              | Ja, mithilfe von Exit branches | Nein                | **Nein**        | **IdlingLevel1** **IdlingLevel2**<br/> | Nach rechts und blinkt               |
| **Idle2 \_ 1**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | Prüft "Wand" und "blinkt"                         |
| **Idle2 \_ 2**              | Keine                     | Nein                | **Nein**        | **IdlingLevel2**                             | Enthält Hand und blinkt                           |
| **Idle3 \_ 1**              | Keine                     | Nein                | **Ja**       | **IdlingLevel3**                             | Gähner                                            |
| **Idle3 \_ 2**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **IdlingLevel3**                             | Fällt in den Standbymodus ( \* Schleifen Animation)               |
| **Suche**              | **Lookdownreturn**       | Nein                | **Nein**        | Keine                                         | Nach unten                                       |
| **Lookdownblink**         | **Lookdownreturn**       | Nein                | **Nein**        | Keine                                         | Blinks nach unten                              |
| **Lookdownreturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                      |
| **Lookleft**              | **Lookleftreturn**       | Nein                | **Nein**        | Keine                                         | Nach links                                       |
| **Lookleftblink**         | **Lookleftreturn**       | Nein                | **Nein**        | Keine                                         | Links nach links                              |
| **Lookleftreturn**        | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                      |
| **Lookright**             | **Lookrightreturn**      | Nein                | **Nein**        | Keine                                         | Nach rechts                                      |
| **Lookrightblink**        | **Lookrightreturn**      | Nein                | **Nein**        | Keine                                         | Blinks mit rechts                             |
| **Lookrightreturn**       | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                      |
| **Suche**                | **Lookupreturn**         | Nein                | **Nein**        | Keine                                         | Nach unten                                         |
| **Lookupblink**           | **Lookupreturn**         | Nein                | **Nein**        | Keine                                         | Blinks nach oben                                |
| **Lookupreturn**          | Keine                     | Nein                | **Nein**        | Keine                                         | Kehrt zur neutralen Position zurück.                      |
| **Nach unten**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingdown"**                               | Nach unten                                       |
| **"Muveleft"**              | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingleft"**                               | Nach links                                       |
| **Überprüfen**             | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingright"**                              | Nach rechts                                      |
| **MoveUp**                | Ja, mithilfe von Exit branches | Nein                | **Ja**       | **"Wvingup"**                                 | Wird nach oben                                         |
| **Froh**               | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Ein Lächeln und eine Hand                  |
| **Prozess**               | Nein                       | Nein                | **Ja**       | Keine                                         | Stirs caldron                                    |
| **Verarbeitung**            | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Stirs caldron ( \* Schleifen Animation)              |
| **Lesen**                  | **"Read Return"**           | Ja               | **Ja**       | Keine                                         | Öffnet Bücher, Lese-und Suchvorgänge                   |
| **Fortsetzung**         | **"Read Return"**           | Ja               | **Ja**       | Keine                                         | Lese-und Suchvorgänge                               |
| **"Read Return"**            | Keine                     | Nein                | **Ja**       | Keine                                         | Kehrt zur neutralen Position zurück.                      |
| **Lektüre**               | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Lesevorgänge ( \* Schleifen Animation)                      |
| **Restpose**              | Keine                     | Ja               | **Nein**        | **Isch**                                 | Neutrale Position                                 |
| **Leider**                   | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Trauriger Ausdruck                                   |
| **Suche**                | Nein                       | Nein                | **Ja**       | Keine                                         | Sucht in Crystal Ball                          |
| **Suchen**             | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Sucht in Crystal Ball ( \* Schleifen Animation)    |
| **Anzeigen**                  | Keine                     | Nein                | **Ja**       | **Anzeige**                                  | Erscheint außerhalb der Obergrenze                               |
| **Startüberwachung**        | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Legt Hand in den Ohr                                 |
| **Stoplauschen**         | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Legt die Hände über Ohren                             |
| **Vorschlagen**               | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Zeigt Glühbirnen an                               |
| **Überrascht**             | Ja, mithilfe von Exit branches | Ja               | **Ja**       | Keine                                         | Überrascht überrascht                                  |
| **Meiner**                 | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Sucht mit "Hand an Kinn"                       |
| **Berechnung**              | Nein                       | Nein                | **Nein**        | Keine                                         | Sucht mit "Hand an Chin" ( \* Schleifen Animation) |
| **Missverständ**             | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Wird vorwärts und löst die Augenbrauen                 |
| **Welle**                  | Ja, mithilfe von Exit branches | Ja               | **Nein**        | Keine                                         | Waves                                            |
| **Schreiben**                 | **Beschreibeturn**          | Ja               | **Ja**       | Keine                                         | Öffnet das Buch, schreibt und sucht nach oben                  |
| **Write-Vorgang fortgesetzt**        | **Beschreibeturn**          | Ja               | **Ja**       | Keine                                         | Schreibvorgänge und suchen                              |
| **Beschreibeturn**           | Keine                     | Nein                | **Ja**       | Keine                                         | Kehrt zur neutralen Position zurück.                      |
| **Lassungs**               | Ja, mithilfe von Exit branches | Nein                | **Ja**       | Keine                                         | Schreibvorgänge ( \* Schleifen Animation)                     |



 

\* Wenn Sie eine Schleifen Animation wiedergeben, müssen Sie " [**Beenden**](stop-method.md) " verwenden, um Sie zu löschen, bevor andere Animationen in der Warteschlange des Zeichens abgespielt werden.

 

