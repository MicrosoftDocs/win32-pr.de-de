---
description: Wenn Winlogon initialisiert, registriert es die STRG + ALT + ENTF-SAS (Secure Attention Sequence) im System und erstellt dann drei Desktops innerhalb der WinSta0-Fenster Station.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Winlogon wird initialisiert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768983d308228e73316c797fb67b035d491a1582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217769"
---
# <a name="initializing-winlogon"></a>Winlogon wird initialisiert.

Wenn [Winlogon](winlogon.md) initialisiert, registriert es die STRG + ALT + ENTF-SAS ( [*Secure Attention Sequence*](../secgloss/s-gly.md) ) im System und erstellt dann drei Desktops innerhalb der WinSta0-Fenster Station.

Durch das Registrieren von STRG + ALT + ENTF wird diese Initialisierung zum ersten Prozess, wodurch sichergestellt wird, dass keine andere Anwendung diese Schlüssel Sequenz verknüpft hat.

WinSta0 ist der Name des Fensters der Fenster Station, das den physischen Bildschirm, die Tastatur und die Maus darstellt. Winlogon erstellt die folgenden Desktops im WinSta0-Objekt.



| Desktop              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Winlogon-Desktop     | Dies ist der Desktop, den Winlogon und [*Gina*](../secgloss/g-gly.md) für die interaktive Identifizierung und Authentifizierung verwenden, sowie andere sichere Dialogfelder. Winlogon wechselt automatisch zu diesem Desktop, wenn eine SAS-Ereignis Benachrichtigung empfangen wird.                                                                                                                                                                                                                                                                                                                                                                          |
| Anwendungs Desktop  | Jedes Mal, wenn sich ein Benutzer erfolgreich anmeldet, wird ein Anwendungs Desktop für diese [*Anmelde Sitzung*](../secgloss/l-gly.md)erstellt. Der Anwendungs Desktop wird auch als Standard-oder Benutzer Desktop bezeichnet. Auf diesem Desktop findet die gesamte Benutzeraktivität statt. Der Anwendungs Desktop ist geschützt. nur das System und die interaktive Anmelde Sitzung haben Zugriff darauf. Beachten Sie, dass nur eine bestimmte Instanz des angemeldeten Benutzers auf den Desktop zugreifen können. Wenn der interaktive Benutzer einen Prozess mithilfe des Dienst Controllers aktiviert, hat diese Dienst Anwendung keinen Zugriff auf den Anwendungs Desktop. |
| Bildschirmschoner Desktop | Dies ist der aktuelle Desktop, wenn ein Bildschirmschoner ausgeführt wird. Wenn ein Benutzer angemeldet ist, haben sowohl das System als auch die interaktive Anmelde Sitzung Zugriff auf den Desktop. Andernfalls hat nur das System Zugriff auf den Desktop.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Als Besitzer dieser Desktops kann Winlogon den aktuellen oder sichtbaren Desktop auf einen der drei Desktops umstellen und den Gina Zugriff auf diese Funktionalität gewähren. Im Allgemeinen wird der aktuelle Desktop von Gina-Entwicklern nicht geändert, da Winlogon den Desktop vor der Kommunikation mit der Gina entsprechend festlegt. Die Beschreibung jeder Gina-Funktion gibt an, welcher Desktop für diesen Befehl aktuell ist.



| Informationen über                                    | Finden Sie unter                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Die verschiedenen Zustände, in denen Winlogon ausgeführt werden kann           | [Winlogon-Zustände](winlogon-states.md)                                                                   |
| Timeout Vorgänge                                      | [Unterstützte Dialog Feld Dienstnutzungsdauer-out-Vorgänge](supported-dialog-box-service-time-out-operations.md) |
| Senden von Nachrichten an Gina, während ein Dialogfeld angezeigt wird | [Senden von Nachrichten an die Gina](sending-messages-to-the-gina.md)                                         |
| Unterstützungsfunktionen                                        | [Winlogon-Unterstützungsfunktionen](authentication-functions.md)                    |



 

 

 
