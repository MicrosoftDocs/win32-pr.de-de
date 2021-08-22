---
description: Ein Handler für externe Benutzeroberflächen (UI) kann abhängig vom Schaltflächentyp, der im Nachrichtentypparameter angegeben ist, eine beliebige Anzahl von Werten an Windows Installer zurückgeben, die vom Installationsprogramm an den Handler übergeben werden.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Zurückgeben von Werten von einem externen Benutzeroberfläche Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b4ba5edcd87b0d4f324762f840c117425b322ea03d1dd15e103c05bcf12352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626080"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Zurückgeben von Werten von einem externen Benutzeroberfläche Handler

Ein Handler für externe Benutzeroberflächen (UI) kann abhängig vom Schaltflächentyp, der im Nachrichtentypparameter angegeben ist, eine beliebige Anzahl von Werten an Windows Installer zurückgeben, die vom Installationsprogramm an den Handler übergeben werden.

Der externe Benutzeroberflächenhandler kann jederzeit die Werte –1 und 0 zurückgeben, da diese nicht mit den Schaltflächentypen verknüpft sind. Der Rückgabewert –1 gibt an, dass im externen Benutzeroberflächenhandler ein interner Fehler aufgetreten ist. Der Rückgabewert 0 gibt an, dass der externe Benutzeroberflächenhandler die Installationsprogrammmeldung nicht verarbeitet hat und das Installationsprogramm stattdessen die Nachricht verarbeiten muss.

Bei Nachrichten, die keinen Schaltflächentyp enthalten, z. B. INSTALLMESSAGE ACTIONDATA und INSTALLMESSAGE PROGRESS, bricht die Rückgabe von \_ \_ IDCANCEL die Installation ab. Die Rückgabe von IDOK benachrichtigt das Installationsprogramm, dass die Meldung vom externen Benutzeroberflächenhandler verarbeitet wurde.

Die verbleibenden Rückgabewerte, wie unten beschrieben, sind direkt mit den Schaltflächentypen verknüpft, die im Nachrichtentyp enthalten sind.



| Rückgabewert der externen Benutzeroberfläche | Bedeutung                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | Der **Benutzer** hat auf die Schaltfläche OK geklickt. Die Nachrichteninformationen wurden verstanden.                     |
| IDCANCEL                 | Die **Schaltfläche ABBRECHEn** wurde gedrückt. Brechen Sie die Installation ab.                                            |
| IDABORT                  | Die **AbORT-Schaltfläche** wurde gedrückt. Bricht die Installation ab.                                              |
| IDRETRY                  | Die **Schaltfläche RETRY** wurde gedrückt. Wiederholen Sie die Aktion.                                                |
| IDIGNORE                 | Die **Schaltfläche IGNORIEREN** wurde gedrückt. Ignorieren Sie den Fehler, und fahren Sie fort.                                      |
| IDYES                    | Die **Schaltfläche JA** wurde gedrückt. Die positive Antwort wird mit der aktuellen Sequenz von Ereignissen fortgesetzt.   |
| IDNO                     | Die **Schaltfläche NEIN** wurde gedrückt. Die negative Antwort wird nicht mit der aktuellen Ereignissequenz fortgesetzt. |



 

Wenn z. B. dem externen UI-Handler eine Nachricht mit dem MB ABORTRETRYIGNORE-Meldungsfeldstilflag gesendet wird, kann der externe UI-Handler einen der folgenden \_ Werte zurückgeben:

-   –1 (Fehler im externen Benutzeroberflächenhandler)
-   0 (keine Aktion im externen Benutzeroberflächenhandler ausgeführt, lassen Windows Installer es behandeln)
-   IDABORT (**Schaltfläche "ABBRECHEN"** gedrückt)
-   IDRETRY **(Schaltfläche "RETRY"** gedrückt)
-   IDIGNORE (**Schaltfläche IGNORIEREN** gedrückt)

 

 



