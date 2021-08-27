---
description: Winlogon sendet Nachrichten an die GINA, während Dialogfelder angezeigt werden. Diese Nachrichten werden alle wie folgt in der WLX \_ WM \_ SAS-Nachricht gekapselt.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Senden von Nachrichten an die GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb52da6a2a66d901207485ed97592a97286902ba51c54ec4924240ab9403a885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918319"
---
# <a name="sending-messages-to-the-gina"></a>Senden von Nachrichten an die GINA

[*Winlogon*](../secgloss/w-gly.md) sendet Nachrichten an die [*GINA,*](../secgloss/g-gly.md) während Dialogfelder angezeigt werden. Diese Nachrichten werden alle wie folgt in der WLX \_ WM \_ SAS-Nachricht gekapselt.



| Sicherer Aufmerksamkeitssequenztyp im wParam-Parameter | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| WLX \_ SAS \_ TYPE \_ STRG ALT \_ \_ DEL                     | Gibt an, dass eine TASTENfolge mit STRG+ALT+ENTF empfangen wurde.                                                                                      |
| WLX \_ SAS \_ TYPE \_ SC \_ INSERT                         | Gibt an, dass eine [*Smartcard*](../secgloss/s-gly.md) in ein kompatibles Gerät eingefügt wurde. |
| WLX \_ SAS \_ TYPE \_ SC \_ REMOVE                         | Gibt an, dass eine Smartcard von einem kompatiblen Gerät entfernt wurde.                                                                        |
| WLX \_ SAS \_ TYPE \_ USER \_ LOGOFF                       | Gibt an, dass ein Benutzer die Abmeldung angefordert hat.                                                                                                       |
| WLX \_ SAS \_ TYPE \_ SCRNSVR \_ TIMEOUT                   | Gibt an, dass der Bildschirmschoner aufgrund fehlender Benutzereingaben ausgeführt werden soll.                                                                      |
| TIMEOUT FÜR \_ WLX-SAS-TYP \_ \_                            | Gibt an, dass innerhalb des angegebenen Time out-Zeitraums keine Benutzereingabe empfangen wurde.                                                               |



 

Bei Time outs und Logoffs schließt Winlogon das Dialogfeld, nachdem die Nachricht gesendet wurde. Diese Meldung wird gesendet, damit der Dialogfeldvorgang auf nützliche Weise reagieren kann (z. B. indem er sich selbst schließt, wenn eine Abmeldung aufgetreten ist).

Bei Eingabetimeouts wird das Dialogfeld mit dem Code WLX \_ DLG \_ INPUT \_ TIMEOUT geschlossen.

Für Bildschirmschonertimeouts wird das Dialogfeld mit dem Code WLX \_ DLG \_ SCREEN \_ SAVER \_ TIMEOUT geschlossen.

Bei Abmeldungen wird der Dialogfeldvorgang mit dem Code WLX \_ DLG \_ USER \_ LOGOFF geschlossen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Initialisieren von Winlogon](initializing-winlogon.md)
</dt> <dt>

[Winlogon-Zustände](winlogon-states.md)
</dt> <dt>

[Unterstützte Time out-Vorgänge des Dialogfelddiensts](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Winlogon-Unterstützungsfunktionen](authentication-functions.md)
</dt> </dl>

 

 
