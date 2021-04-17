---
title: Wartungs Tasks für Anmeldekonten
description: In diesem Thema werden Probleme beschrieben, die sich auf Anmelde Konto-Wartungsaufgaben beziehen.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- Anmelde Konto-Wartungs Tasks anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0f11f69d9a974fd666871833029eda0e059329
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104390122"
---
# <a name="logon-account-maintenance-tasks"></a>Wartungs Tasks für Anmeldekonten

In diesem Thema werden Probleme beschrieben, die sich auf Anmelde Konto-Wartungsaufgaben beziehen.

Es gibt zwei primäre Probleme, die sich auf Anmelde Konto-Wartungsaufgaben beziehen:

-   Aktualisieren des Konto Kennworts für eine Dienst Instanz, die unter einem Benutzerkonto ausgeführt wird. Weitere Informationen finden Sie unter [Ändern des Kennworts für das Benutzerkonto eines Dienstanbieter](changing-the-password-on-a-serviceampaposs-user-account.md).
-   Behandeln von Änderungen am Anmelde Konto einer Dienst Instanz.

Letzteres ist ein seltener Fall, kann aber eintreten. Das System stellt das Verwaltungs Tool "Computer Verwaltung" bereit, das eine Änderung an einem Dienst Anmelde Konto ermöglicht. Außerdem können andere Anwendungen die [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) -Funktion verwenden, um ein neues Anmelde Konto für einen installierten Dienst anzugeben. Standardmäßig sind lokale Administratorrechte erforderlich, um ein Dienst Konto zu ändern. Wenn dies der Fall ist, kann sich dies auf zwei Arten auf den Dienst auswirken:

-   Wenn Sie Dienst Prinzipal Namen (Service Principal Names, SPNs) registriert haben, werden Sie auf dem falschen Konto registriert.
-   Wenn Sie ACEs festlegen, um Zugriff auf den Dienst zu gewähren, gewähren Sie dem Konto nun Zugriff auf das falsche Konto.

Ein Ansatz besteht darin, dass der Dienst Installationsprogramm die registrierten SPNs für jede Dienst Instanz in der Registrierung auf dem Host Computer speichert. Sie können den gleichen Registrierungsschlüssel unter HKEY \_ local \_ Machine verwenden, den Sie zum Speichern der Bindungs Zeichenfolge für den Dienst-SCP verwendet haben. Beim Starten des Diensts wird die Funktion [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) aufgerufen, um das Anmelde Konto zu ermitteln. Anschließend wird der Active Directory Server abgefragt, um zu bestimmen, ob die SPNs für das Verzeichnis Objekt für dieses Konto registriert sind. Wenn die SPNs nicht registriert sind oder beim falschen Konto registriert sind, lehnt der Dienst ab und zeigt eine Meldung an, die besagt, dass ein Domänen Administrator das Konfigurationsprogramm des Diensts ausführen muss, um die Anmelde Kontoeinstellungen zu aktualisieren. Beachten Sie, dass diese Neukonfiguration von einem Administrator abgeschlossen werden muss, da das Dienst Konto keinen Zugriff zum Aktualisieren seines eigenen SPN haben sollte. Beachten Sie auch, dass SPNs aus dem alten Konto entfernt werden müssen. andernfalls sind die SPNs für die Authentifizierung nutzlos, da Sie in der Gesamtstruktur nicht eindeutig sind.

 

 