---
description: In der folgenden Tabelle werden die Unterschiede zwischen dem Herunterfahren unter Windows Vista und Windows XP zusammengefasst.
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Änderungen am Herunterfahren für Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e04bb20099349ce378384cf01c39e53ca03a896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042313"
---
# <a name="shutdown-changes-for-windows-vista"></a>Änderungen am Herunterfahren für Windows Vista

In der folgenden Tabelle werden die Unterschiede zwischen dem Herunterfahren unter Windows Vista und Windows XP zusammengefasst.



| Funktion                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blockieren des herunter Fahrens       | Anwendungen können für 5 Sekunden auf [**WM \_ queryendsession**](wm-queryendsession.md) reagieren, und das System ermöglicht dem Benutzer das Beenden der Anwendung. Anwendungen, die als Reaktion auf **WM \_ queryendsession** den Wert **true** zurückgeben, können auf die [**WM- \_ Endsitzung**](wm-endsession.md) für 5 Sekunden verzögern. das System ermöglicht dem Benutzer dann das Beenden der Anwendung. | Anwendungen können auf die [**WM- \_ queryendsession**](wm-queryendsession.md) für 5 Sekunden reagieren. das System ermöglicht dem Benutzer das fortfahren oder das Abbrechen des herunter Fahrens. Anwendungen, die als Reaktion auf **WM \_ queryendsession** den Wert **true** zurückgeben, können auf die [**WM- \_ Endsitzung**](wm-endsession.md) für 5 Sekunden verzögern. anschließend ermöglicht das System dem Benutzer das fortfahren oder das Abbrechen des herunter Fahrens.                                                                                                      |
| Abbrechen wird abgebrochen      | Wenn eine Anwendung als Antwort auf [**WM \_ queryendsession**](wm-queryendsession.md) **false** zurückgibt, wird das Herunterfahren in den meisten Fällen abgebrochen. Es wird jedoch keine Benutzeroberfläche angezeigt, sodass der Benutzer möglicherweise nicht weiß, dass das Herunterfahren abgebrochen wurde.                                                                                                                                                      | Wenn eine Anwendung als Antwort auf [**WM \_ queryendsession**](wm-queryendsession.md) **false** zurückgibt, wird Sie weiterhin in der Benutzeroberfläche für das Herunterfahren angezeigt. Beachten Sie, dass das System keine Konsolen Anwendungen oder-Anwendungen ohne sichtbare Fenster zulässt, um das Herunterfahren abzubrechen. Diese Anwendungen werden automatisch beendet, wenn Sie nicht innerhalb von 5 Sekunden auf **WM \_ queryendsession** oder [**WM \_ EndSession**](wm-endsession.md) reagieren, oder wenn Sie als Antwort auf **WM \_ queryendsession** **false** zurückgeben. |
| Benutzeroberfläche Herunterfahren | Das System zeigt ein Dialogfeld für jede Anwendung an, die das Herunterfahren blockiert. Wenn der Benutzer auf die Schaltfläche " **jetzt beenden** " klickt, wird die Anwendung beendet. Wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, wird Shutdown abgebrochen, und die Anwendung wird weiterhin ausgeführt.                                                                                                                                    | Das System zeigt eine voll Bild Benutzeroberfläche an, die alle Anwendungen, die das Herunterfahren blockieren, sowie deren Gründe identifiziert (wenn Sie einen Grund mit [**shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)registriert haben).                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>Bewährte Methoden

-   Anwendungen sollten das Herunterfahren nicht blockieren. Antworten Sie so schnell wie möglich auf [**WM \_ queryendsession**](wm-queryendsession.md) , und verschieben Sie Bereinigungs Aktivitäten, bis die [**WM- \_ endsitzungs**](wm-endsession.md) Nachricht verarbeitet wird.
-   Anwendungen, die das Herunterfahren blockieren müssen, sollten die neue Funktion [**shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) verwenden, um eine Zeichenfolge zu registrieren, die den Grund für den Benutzer erläutert. Der Benutzer kann entscheiden, ob er fortfahren oder das Herunterfahren abbrechen soll.
-   Anwendungen können das Herunterfahren nicht blockieren.

 

 



