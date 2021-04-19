---
description: Winlogon sendet Nachrichten an die Gina, während Dialogfelder angezeigt werden. Diese Nachrichten werden wie folgt in der SAS-Nachricht der wlx-WM gekapselt \_ \_ .
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Senden von Nachrichten an die Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353437"
---
# <a name="sending-messages-to-the-gina"></a>Senden von Nachrichten an die Gina

[*Winlogon*](../secgloss/w-gly.md) sendet Nachrichten an die [*Gina*](../secgloss/g-gly.md) , während Dialogfelder angezeigt werden. Diese Nachrichten werden wie folgt in der SAS-Nachricht der wlx-WM gekapselt \_ \_ .



| Typ der sicheren Aufmerksamkeit in den wParam-Parameter | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| wlx \_ SAS \_ Type \_ STRG \_ alt \_ del                     | Gibt an, dass eine Tastenkombination STRG + ALT + ENTF empfangen wurde.                                                                                      |
| wlx \_ SAS \_ Type \_ SC \_ Insert                         | Gibt an, dass eine [*Smartcard*](../secgloss/s-gly.md) in ein kompatibles Gerät eingefügt wurde. |
| wlx \_ SAS \_ Type \_ SC \_ Remove                         | Gibt an, dass eine Smartcard von einem kompatiblen Gerät entfernt wurde.                                                                        |
| Benutzer Abmeldung zum wlx- \_ SAS- \_ Typ \_ \_                       | Gibt an, dass ein Benutzer eine Abmeldung angefordert hat.                                                                                                       |
| \_ \_ \_ scrnsvr-Timeout für wlx-SAS-Typ \_                   | Gibt an, dass der Bildschirmschoner aufgrund fehlender Benutzereingaben ausgeführt werden soll.                                                                      |
| Timeout für wlx- \_ SAS- \_ Typ \_                            | Gibt an, dass innerhalb des angegebenen Timeout Zeitraums keine Benutzereingaben empfangen wurden.                                                               |



 

Bei Timeouts und Abmelde Vorgängen schließt Winlogon das Dialogfeld, nachdem die Nachricht gesendet wurde. Diese Meldung wird gesendet, sodass der Dialogfeld Vorgang auf nützliche Weise reagieren kann (z. b. durch Schließen des Abmelde Vorgangs, wenn eine Abmeldung aufgetreten ist).

Bei Eingabe Timeouts wird das Dialogfeld mit dem Code wlx \_ DLG \_ input \_ Timeout geschlossen.

Für Bildschirmschoner-Timeouts wird das Dialogfeld mit dem Code wlx \_ DLG \_ Screen \_ Saver Timeout geschlossen \_ .

Bei Abmelde Vorgängen wird der Dialogfeld Vorgang mit dem Code wlx DLG-Benutzer Abmeldung geschlossen \_ \_ \_ .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Winlogon wird initialisiert.](initializing-winlogon.md)
</dt> <dt>

[Winlogon-Zustände](winlogon-states.md)
</dt> <dt>

[Unterstützte Dialog Feld Dienstnutzungsdauer-out-Vorgänge](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Winlogon-Unterstützungsfunktionen](authentication-functions.md)
</dt> </dl>

 

 
