---
description: Bei der Initialisierung von Winlogon wird die SAS (Secure Attention Sequence) STRG+ALT+ENTF beim System registriert und anschließend drei Desktops in der WinSta0-Fensterstation erstellt.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Initialisieren der Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff33740b77b23577cd7749b8cc745cd06a55e18675e35b817e405a71679b482
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482392"
---
# <a name="initializing-winlogon"></a>Initialisieren der Winlogon

Bei der Initialisierung von [Winlogon](winlogon.md) wird die SAS [*(Secure Attention Sequence)*](../secgloss/s-gly.md) STRG+ALT+ENTF beim System registriert und anschließend drei Desktops in der WinSta0-Fensterstation erstellt.

Durch das Registrieren von STRG+ALT+ENTF wird diese Initialisierung zum ersten Prozess, wodurch sichergestellt wird, dass keine andere Anwendung diese Tastensequenz ein hooked hat.

WinSta0 ist der Name des Fensterstationsobjekts, das den physischen Bildschirm, die Tastatur und die Maus darstellt. Winlogon erstellt die folgenden Desktops im WinSta0-Objekt.



| Desktop              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Winlogon-Desktop     | Dies ist der Desktop, den Winlogon und [*GINA*](../secgloss/g-gly.md) für die interaktive Identifikation und Authentifizierung sowie andere sichere Dialogfelder verwenden. Winlogon wechselt automatisch zu diesem Desktop, wenn er SAS-Ereignisbenachrichtigungen empfängt.                                                                                                                                                                                                                                                                                                                                                                          |
| Anwendungsdesktop  | Jedes Mal, wenn sich ein Benutzer erfolgreich anmeldet, wird ein Anwendungsdesktop für diese [*Anmeldesitzung erstellt.*](../secgloss/l-gly.md) Der Anwendungsdesktop wird auch als Standarddesktop oder Benutzerdesktop bezeichnet. Auf diesem Desktop werden alle Benutzeraktivitäten ausgeführt. Der Anwendungsdesktop ist geschützt. nur das System und die interaktive Anmeldesitzung haben Zugriff darauf. Beachten Sie, dass nur eine bestimmte Instanz des angemeldeten Benutzers Zugriff auf den Desktop hat. Wenn der interaktive Benutzer einen Prozess mithilfe des Dienstcontrollers aktiviert, hat diese Dienstanwendung keinen Zugriff auf den Anwendungsdesktop. |
| Desktop des Bildschirmschoners | Dies ist der aktuelle Desktop, wenn ein Bildschirmschoner ausgeführt wird. Wenn ein Benutzer angemeldet ist, haben sowohl das System als auch die interaktive Anmeldesitzung Zugriff auf den Desktop. Andernfalls hat nur das System Zugriff auf den Desktop.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Als Besitzer dieser Desktops kann Winlogon den aktuellen oder sichtbaren Desktop auf einen der drei Desktops umschalten und dem GINA-Zugriff auf diese Funktionalität erlauben. Im Allgemeinen ändern GINA-Entwickler den aktuellen Desktop nicht, da Winlogon den Desktop vor der Kommunikation mit GINA entsprechend fest legt. Die Beschreibung jeder GINA-Funktion gibt an, welcher Desktop für diesen Aufruf aktuell ist.



| Informationen über                                    | Finden Sie unter                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Die verschiedenen Zustände, in denen Winlogon ausgeführt werden kann           | [Winlogon-Zustände](winlogon-states.md)                                                                   |
| Time out-Vorgänge                                      | [Unterstützte Time outvorgänge des Dialogfelddiensts](supported-dialog-box-service-time-out-operations.md) |
| Senden von Nachrichten an GINA, während ein Dialogfeld angezeigt wird | [Senden von Nachrichten an GINA](sending-messages-to-the-gina.md)                                         |
| Unterstützungsfunktionen                                        | [Winlogon-Unterstützungsfunktionen](authentication-functions.md)                    |



 

 

 
