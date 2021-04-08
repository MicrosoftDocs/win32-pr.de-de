---
title: Authentifizierungs Probleme bei ADSI mit ASP
description: Abhängig von der Konfiguration Ihres Intranets können Authentifizierungs Probleme auftreten, wenn ADSI-Code auf einer ASP-Seite ausgeführt wird.
ms.assetid: 287e2e19-7da9-497b-bf46-595ff4755261
ms.tgt_platform: multiple
keywords:
- ADSI, ASP-Seiten, Authentifizierungs Probleme
- ADSI, Authentifizierung, ASP-Probleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423d1aa39006f89ca366423da9d135e00af45693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730201"
---
# <a name="authentication-issues-for-adsi-with-asp"></a>Authentifizierungs Probleme bei ADSI mit ASP

Abhängig von der Konfiguration Ihres Intranets können Authentifizierungs Probleme auftreten, wenn ADSI-Code auf einer ASP-Seite ausgeführt wird.

Die Authentifizierung für den Zugriff auf den Domänen Controller kann mithilfe der Delegierung angegeben werden. Durch die Delegierung kann ein Dienst als Benutzer fungieren, sodass er über diese Benutzer Anmelde Informationen auf eine Netzwerkressource zugreifen kann. Wenn das Intranet dieser Konfiguration folgt, müssen Sie IIS für die Verwendung der Delegierung einrichten. Legen Sie den IIS-Authentifizierungsmechanismus als anonym oder NTLM fest. Wenn Sie anonym auswählen, wird der Sicherheitskontext dem IUSR- \_ Computer Konto zugeordnet. Wenn Sie NTLM auswählen, ändert sich der Sicherheitskontext, je nachdem, welcher Benutzer sich bei Ihrer Website anmeldet. Weitere Informationen und Anweisungen zum Einrichten des IIS-Servers für die Delegierung finden Sie unter [Windows 2000 Resource Kit](https://support.microsoft.com/kb/927229).

Wenn Sie einen IIS-Server verwenden, der NT Challenge/Response verwendet, oder einen Browser Client, der Kerberos nicht unterstützt, wird die Doppel-Hop-Authentifizierung nicht unterstützt. Eine Double-Hop-Authentifizierung bedeutet, dass die Benutzer Anmelde Informationen vom Browser Client an den IIS-Server weitergegeben werden. Anschließend übergibt der IIS-Server die Anmelde Informationen an den Back-End-Server. In dieser Situation können Sie eine der folgenden Lösungen verwenden, um den Zugriff auf das Verzeichnis von der ASP-Seite aus zuzulassen:

-   Verwenden Sie [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) oder [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) , um Anmelde Informationen an Active Directory zu übergeben. Die Webseite authentifiziert den verbundenen Benutzer mit dem IIS-Server. Wenn der Benutzer authentifiziert wurde, kann die Webseite opendsobject oder ADsOpenObject verwenden, um einen Benutzernamen und ein Kennwort an den Verzeichnisdienst zu übergeben, um die Authentifizierung für den Back-End-Server zu erhalten. Auf der Webseite kann dann auf Daten aus dem Verzeichnis zugegriffen werden.
-   Fügen Sie Ihren Code einem COM-Objekt hinzu, und platzieren Sie dieses Objekt in einer [com+-Anwendung](../cossdk/com--application-overview.md) (zuvor als MTS-Paket bezeichnet). Die COM+-Anwendung kann dann als [Domänen Benutzerkonto](/windows/desktop/AD/domain-user-accounts)ausgeführt werden.
-   Verwenden Sie mehrere ASP-Seiten, bei denen eine Seite den Client authentifiziert und eine andere Seite Anmelde Informationen mithilfe der anonymen Authentifizierung für ein Domänen Benutzerkonto an das Verzeichnis übergibt.

Diese Methoden umfassen das Authentifizieren des Webclients und das anschließende Ändern der Anmelde Informationen, wenn Sie sich an das Verzeichnis wenden, weil die Double-Hop-Authentifizierung mit denselben Anmelde Informationen nicht möglich ist.

 

 