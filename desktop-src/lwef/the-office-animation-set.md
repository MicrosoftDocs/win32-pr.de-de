---
title: Der Office-Animationssatz
description: Der Office-Animationssatz
ms.assetid: ea80d19b-bf4c-4f6e-bab0-424a9f78f457
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cfe8ffbfb9d54ee956c36dd6eb1b3d567f26ad8dc55cd182282db6a685f3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975550"
---
# <a name="the-office-animation-set"></a>Der Office-Animationssatz

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

In der folgenden Tabelle sind die Animationen aufgeführt, die für die Microsoft Office 2000 Zeichen definiert sind. Wenn Sie beabsichtigen, ihr Zeichen in Microsoft Office, sollten Sie alle Animationen in dieser Tabelle unterstützen. Darüber hinaus können Sie alle anderen Animationen hinzufügen, die Sie live verwenden, aber denken Sie daran, Microsoft Office sie nicht aufrufen. Animationen mit Sternchen ( \* ) sollten eine 100%-ige Schleife sein. Andere Animationen sollten kurz sein.



| Animation               | Agentstatus    | Beispiel für die Verwendung                                                                                 | Spezifische Animationsbeispiele                                                                                                               |
|-------------------------|----------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **Warnung**               | Keine           | Wenn das Zeichen den Benutzer warnen möchte                                                           | Das Zeichen sucht nach dem Benutzer.                                                                                                              |
| **CheckingSomething\*** | Keine           | Rechtschreibprüfung, Grammatikprüfung                                                                            | Zeichen sucht etwas in einem Nachschlagebuch                                                                                          |
| **Gratulieren**        | Keine           | Abschließen eines Assistenten                                                                                    | Großes Lächeln, Eindrungs-, Aber glückliches Aussehen                                                                                                 |
| **EmptyTrash**          | Keine           | Der Papierkorb wird in der Outlook                                                                          | Papierkorb für Zeichenlichter in Brand                                                                                                        |
| **Explain**             | Keine           | Wenn das Zeichen dem Benutzer etwas erklären möchte                                            | Sieht den Benutzer kurz, aber freundlicher an und sieht dann weg.                                                                                     |
| **GestureDown**         | GesturingDown  | Zeichen zeigt auf etwas auf dem Bildschirm                                                         | Das Zeichen sieht den Benutzer an und zeigt dann auf den Bildschirm.                                                                           |
| **GestureLeft**         | GesturingLeft  | Ein Zeichen zeigt auf etwas auf dem Bildschirm, z. B. ein Hilfethema oder ein Teil der Benutzeroberfläche.                  | Das Zeichen sieht den Benutzer an und zeigt dann auf den Bildschirm.                                                                           |
| **GestureRight**        | GesturingRight | "Präsentieren" eines Hilfethemas oder Dialogs                                                                  | Das Zeichen sieht den Benutzer an und zeigt dann auf den Bildschirm.                                                                           |
| **GestureUp**           | GesturingUp    | Zeichen zeigt auf etwas auf dem Bildschirm                                                         | Das Zeichen sieht den Benutzer an und zeigt dann auf den Bildschirm.                                                                           |
| **GetArtsy\***          | Keine           | Autoformat                                                                                           | Zeichen setzt auf Beret, enthält Palette und Zeichnet                                                                                        |
| **GetAttention**        | Keine           | Trinkgeld mit hoher Priorität                                                                                    | Gesten stark, um die Aufmerksamkeit des Benutzers zu erhalten; Springt z. B. mit wellenförmigen Armen nach oben und unten                                                 |
| **GetTechy**            | Keine           | Wird in der Programmierumgebung ausgeführt                                                                | Zeichen pullt Rechner oder Lötmaschine                                                                                          |
| **GetWizardy\***        | Keine           | Diagramm-Assistent wird ausgeführt, während Zeichen sichtbar sind (Aktion wird mit jedem neuen Assistentenbereich erneut ausgelöst)        | Zeichen setzt Assistentenm und Wellenwand ein                                                                                               |
| **Auf Wiedersehen**             | Keine           | Ein weiteres Zeichen wird ausgewählt.                                                                          | Dies ist ein aufwändiges Verschwinden, das in **RestPose beginnt** und mit einem leeren Frame endet.                                                      |
| **Greeting (Begrüßung)**            | Keine           | Das Zeichen wird ausgewählt.                                                                                  | Dies ist ein ausführliches Erscheinen, das mit einem leeren Frame beginnt und mit **RestPose endet.**                                                      |
| **Hörvermögen \_ 1\***        | Keine           | Lange Datei geöffnet                                                                                    | Hörnchen bis zum Boden, lauschend auf den Computer                                                                                              |
| **Ausblenden**                | Versteckt         | Zeichenblätter vorübergehend                                                                         | Blättert schnell in einem Qualm                                                                                                         |
| **Idle1 \_ 1**            | Keine Benutzereingabe  | Aktiv lauschend, dann wird gelockt und in den Ruhezustand übergeht. (Möglichkeit, die Persönlichkeit von Zeichen zu zeigen) | Blinken, suchen, wartend                                                                                               |
| **Idle2**               | Keine Benutzereingabe  | Längere Leerlaufzeiten                                                                                  | Zeichen gähnt und sieht im Ruhezustand aus                                                                                                          |
| **Idle3**               | Keine Benutzereingabe  | Tiefer Leerlauf (wenn sich das Zeichen seit langer Zeit im Leerlauf befindet)                                         | Zeichen geht in den Ruhezustand                                                                                                                   |
| **IdleHit**             | Keine           | Dies ist ein nicht zugeordnetes repräsentatives Beispiel für Animationen auf Leerlaufebene 1.                                | Alle Animationen im Leerlauf                                                                                                                |
| **LookDown**            | Keine           | Kurz nach unten                                                                                   | Bemerkt, dass eine Zeile eingefügt wird und einen Blick auf sie wirt.                                                                                               |
| **LookDownLeft**        | Keine           | Kurz nach unten und links                                                                          | Bemerkt, dass eine Zeile eingefügt wird und einen Blick auf sie wirt.                                                                                               |
| **LookDownRight**       | Keine           | Kurz nach unten und rechts                                                                         | Bemerkt, dass eine Spalte eingefügt wird und einen Blick auf sie wirt.                                                                                            |
| **LookLeft**            | Keine           | Sieht kurz nach links aus                                                                                   | Bemerkt, dass eine Tabelle eingefügt wird und einen Blick auf sie wirt.                                                                                             |
| **LookRight**           | Keine           | Sieht kurz nach rechts aus                                                                                  | Bemerkt, dass ein Wort verschoben wird und es sich ansieht                                                                                                 |
| **Lookup**              | Keine           | Sucht kurz nach, als ob bei etwas, das über dem Zeichen auf dem Bildschirm angezeigt wird,                          | Die Symbolleistenschaltfläche "Hinweise" wird angeklickt, und sie wird angezeigt (das Zeichen ist nicht so überraschend wie interessiert).                                   |
| **LookUpLeft**          | Keine           | Sieht kurz nach links und oben aus                                                                            | Die Symbolleistenschaltfläche "Hinweise" wird angeklickt, und sie wird angezeigt (das Zeichen ist nicht so überraschend wie interessiert).                                   |
| **LookUpRight**         | Keine           | Sieht kurz nach rechts und nach oben aus                                                                           | Die Symbolleistenschaltfläche "Hinweise" wird angeklickt, und sie wird angezeigt (das Zeichen ist nicht so überraschend wie interessiert).                                   |
| **Drucken**               | Keine           | Drucken einer Seite eines Druckauftrags                                                                       | Packt ein Papier und sendet es an den Drucker                                                                                 |
| **Verarbeitung\***        | Keine           | Allgemeine Aktion, für die wir keine bestimmte Zeichenaktion haben                                     | Das Zeichen erhält einen Blick auf die Ziehung und zieht einen Ziehziehzieher für die Ziehung. Die Animation sollte einen schnellen Einstieg in eine Schleife und dann einen schnellen Exit haben. |
| **RestPose**            | Keine           | Wird verwendet, wenn das Zeichen keine Animation abspielt                                                   | Abbildung des Assistenten                                                                                                                 |
| **Speichern\***              | Keine           | Wird während eines Dateischonungsvorgang verwendet                                                                    | Zeichen setzt etwas in einen Tresor                                                                                                     |
| **Suche\***         | Keine           | Wird für die Suche, Rechtschreibprüfung und Grammatikprüfung verwendet.                                                        | Der Kopf kehrt um und sieht auf das Dokument zurück. Die Animation sollte einen schnellen Einstieg in eine Schleife und dann einen schnellen Exit haben.                                 |
| **SendMail**            | Keine           | Senden von E-Mails                                                                                         | Pullt einen Buchstaben und legt ihn in einem Postfach ab.                                                                                             |
| **Anzeigen**                | Anzeige        | Zeichen gibt aus kurzer Zeit zurück                                                                   | Schnelles Und-Abspringen auf der Stage                                                                                                         |
| **Berechnung\***          | Keine           | Durchführen einer komplexen Berechnung, z. B. Solver                                                          | Das Zeichen sieht nach oben aus und scratcht den Kopf. Die Animation sollte einen schnellen Einstieg in eine Schleife und dann einen schnellen Exit haben.                             |
| **Welle**                | Keine           | Zugehörige Warnungen                                                                                  | Welle. Ähnlich wie bei Warnungen, aber nicht so lange oder wie "tic"                                                                                     |
| **Schreiben\***           | Keine           | Der Kunde ändert etwas in den Extrasoptionen. Der Kunde gibt die IntelliSearch-Anforderung ein.                   | Pullt das Pad und beginnt mit dem Dribbling. Die Animation sollte einen schnellen Einstieg in eine Schleife und dann einen schnellen Exit haben.                                   |



 

 

 




