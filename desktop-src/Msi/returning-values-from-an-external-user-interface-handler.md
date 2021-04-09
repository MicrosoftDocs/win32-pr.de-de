---
description: Ein externer Benutzeroberflächen Handler kann eine beliebige Anzahl von Werten zurückgeben Windows Installer, die in Abhängigkeit von dem im Message Type-Parameter angegebenen schaltentyp (User Interface, UI) an den Handler übergeben werden.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Zurückgeben von Werten von einem externen Benutzeroberflächen Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754201"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Zurückgeben von Werten von einem externen Benutzeroberflächen Handler

Ein externer Benutzeroberflächen Handler kann eine beliebige Anzahl von Werten zurückgeben Windows Installer, die in Abhängigkeit von dem im Message Type-Parameter angegebenen schaltentyp (User Interface, UI) an den Handler übergeben werden.

Der externe UI-Handler kann die Werte – 1 und 0 jederzeit zurückgeben, da diese nicht mit den Schaltflächen Typen verknüpft sind. Der Rückgabewert – 1 gibt an, dass im externen UI-Handler ein interner Fehler aufgetreten ist. Der Rückgabewert 0 gibt an, dass der externe UI-Handler die installernachricht nicht verarbeitet hat, und der Installer muss stattdessen die Nachricht verarbeiten.

Bei Nachrichten, die keinen Schalt Flächentyp enthalten, wie z. b. installmessage \_ aktiondata und installmessage \_ Progress, wird die Installation durch die Rückgabe von IDCANCEL abgebrochen. Beim Zurückgeben von IDOK wird das Installationsprogramm benachrichtigt, dass die Nachricht vom externen UI-Handler behandelt wurde.

Die übrigen Rückgabewerte, wie unten beschrieben, sind direkt mit den Schaltflächen Typen verknüpft, die im Nachrichtentyp enthalten sind.



| Rückgabewert der externen Benutzeroberfläche | Bedeutung                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | Der Benutzer hat die Schaltfläche **OK** gedrückt. Die Nachrichten Informationen wurden verstanden.                     |
| IDCANCEL                 | Die Schaltfläche **Abbrechen** wurde gedrückt. Brechen Sie die Installation ab.                                            |
| IDABORT                  | Die Schaltfläche **Abbrechen** wurde gedrückt. Brechen Sie die Installation ab.                                              |
| IDRETRY                  | Die **Wiederholungs** Schaltfläche wurde gedrückt. Wiederholen Sie die Aktion.                                                |
| IDIGNORE                 | Die **ignorieren** -Schaltfläche wurde gedrückt. Ignorieren Sie den Fehler, und fahren Sie fort.                                      |
| IDYES                    | Die **Ja** -Schaltfläche wurde gedrückt. Die positive Antwort ist mit der aktuellen Ereignis Sequenz fortzufahren.   |
| IDNO                     | Die Schaltfläche **Nein** wurde gedrückt. Die negative Antwort wird nicht mit der aktuellen Abfolge von Ereignissen fortgesetzt. |



 

Wenn z. b. der externe UI-Handler eine Meldung mit dem Format "MB \_ AbortRetryIgnore Message Box Styles" sendet, kann der externe UI-Handler einen der folgenden Werte zurückgeben:

-   – 1 (Fehler im externen UI-Handler)
-   0 (keine Aktion im externen UI-Handler ausgeführt, Windows Installer behandeln)
-   Idabort (Schaltfläche **Abbrechen** )
-   Idretry (Schaltfläche "**wiederholen** " gedrückt)
-   IDIGNORE (Schaltfläche "**ignorieren** " gedrückt)

 

 



