---
title: Wartungstasks für Anmeldekonten
description: In diesem Thema werden Probleme im Zusammenhang mit Wartungstasks für Anmeldekonten beschrieben.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- Wartungstasks für Anmeldekonten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d026f37ad81d71691ac418ea49b1b0fda5e1d09fb3e4b6e2259083eb80ada9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186632"
---
# <a name="logon-account-maintenance-tasks"></a>Wartungstasks für Anmeldekonten

In diesem Thema werden Probleme im Zusammenhang mit Wartungstasks für Anmeldekonten beschrieben.

Es gibt zwei Hauptprobleme, die Wartungstasks für Anmeldekonten betreffen:

-   Aktualisieren des Kontokennworts für eine Dienstinstanz, die unter einem Benutzerkonto ausgeführt wird. Weitere Informationen finden Sie unter Ändern des Kennworts für [das Benutzerkonto eines Diensts.](changing-the-password-on-a-serviceampaposs-user-account.md)
-   Behandeln von Änderungen am Anmeldekonto einer Dienstinstanz.

Letzteres ist ein seltener Fall, kann aber auftreten. Das System stellt das Verwaltungstool für die Computerverwaltung bereit, das das Ändern eines Dienstanmeldungskontos ermöglicht. Darüber hinaus können andere Anwendungen die [**ChangeServiceConfig-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) verwenden, um ein neues Anmeldekonto für einen installierten Dienst anzugeben. Standardmäßig sind lokale Administratorrechte erforderlich, um ein Dienstkonto zu ändern. In diesem Fall kann sich dies auf zwei Arten auf Ihren Dienst auswirken:

-   Wenn Sie Dienstprinzipalnamen (SPNs) registriert haben, werden diese im falschen Konto registriert.
-   Wenn Sie ACEs festlegen, um Zugriff auf den Dienst zu gewähren, würden diese nun Zugriff auf das falsche Konto gewähren.

Ein Ansatz besteht darin, dass das Dienstinstallationsprogramm die registrierten SPNs für jede Dienstinstanz in der Registrierung auf dem Hostcomputer speichert. Sie können denselben Registrierungsschlüssel unter HKEY LOCAL MACHINE verwenden, den \_ Sie zum Speichern der \_ Bindungszeichenfolge für den Dienst-SCP verwendet haben. Wenn der Dienst gestartet wird, ruft er die [**QueryServiceConfig-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) auf, um sein Anmeldekonto zu bestimmen, und fragt dann den Active Directory-Server ab, um zu bestimmen, ob die SPNs für das Verzeichnisobjekt für dieses Konto registriert sind. Wenn die SPNs nicht registriert sind oder für das falsche Konto registriert sind, verweigert der Dienst den Start und zeigt eine Meldung an, die besagt, dass ein Domänenadministrator das Konfigurationsprogramm des Diensts ausführen muss, um die Einstellungen des Anmeldekontos zu aktualisieren. Beachten Sie, dass diese Neukonfiguration von einem Administrator abgeschlossen werden muss, da das Dienstkonto keinen Zugriff zum Aktualisieren seines eigenen SPN haben sollte. Beachten Sie auch, dass SPNs aus dem alten Konto entfernt werden müssen. Andernfalls sind die SPNs für die Authentifizierung unbrauchbar, da sie in der Gesamtstruktur nicht eindeutig sind.

 

 