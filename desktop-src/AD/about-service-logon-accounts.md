---
title: Informationen zu Dienst Anmeldekonten
description: Wenn ein Win32-basierter Dienst gestartet wird, meldet er sich am lokalen Computer an.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328b33d5dab36ccc5a803eb7c43ca3112e96ecf8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101403"
---
# <a name="about-service-logon-accounts"></a>Informationen zu Dienst Anmeldekonten

Wenn ein Win32-basierter Dienst gestartet wird, meldet er sich am lokalen Computer an. Sie kann sich als anmelden:

-   Ein lokales oder Domänen Benutzerkonto.
-   Das LocalSystem-Konto.

Mit dem Anmelde Konto wird die Sicherheitsidentität des Diensts zur Laufzeit bestimmt, d. h. der primäre Sicherheitskontext des Diensts. Der Sicherheitskontext bestimmt, ob der Dienst auf lokale Ressourcen und Netzwerkressourcen zugreifen kann. Beispielsweise kann ein Dienst, der im Sicherheitskontext eines lokalen Benutzerkontos ausgeführt wird, nicht auf Netzwerkressourcen zugreifen. Umgekehrt hat ein Dienst, der im Sicherheitskontext des Kontos LocalSystem auf einem Windows 2000-Domänen Controller (DC) ausgeführt wird, uneingeschränkten Zugriff auf den DC. Weitere Informationen und eine Erläuterung der Vorteile und Einschränkungen zwischen Benutzerkonten und LocalSystem finden Sie unter [Sicherheits Kontexte und Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).

Letztendlich haben Administratoren auf dem System, auf dem der Dienst installiert ist, die Kontrolle über das Anmelde Konto des Diensts. Aus Sicherheitsgründen können einige Administratoren den Dienst unter dem Konto "LocalSystem" nicht installieren. Ihr Dienst muss unter einem Domänen Benutzerkonto ausgeführt werden können. Als Programmierer können Sie die Kontrolle über das Anmelde Konto Ihres Diensts ausüben. Das Dienst Installationsprogramm gibt das Anmelde Konto des Diensts an, wenn es die Funktion "| [**ateservice**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) " aufruft, um den Dienst auf einem Host Computer zu installieren. Das Installationsprogramm kann ein Standard Anmelde Konto vorschlagen, aber es sollte einem Administrator erlauben, das tatsächliche Konto anzugeben.

Mit dem Installationsprogramm können Sie auch die folgenden Aufgaben im Zusammenhang mit dem Anmelde Konto Ihres Diensts ausführen:

-   Die Installation. Wenn die Installation des Diensts für die unter Verwendung eines Benutzerkontos ausgeführt wird, muss das Konto vorhanden sein, bevor Sie "up [**Service Service" aufrufen können**](/windows/desktop/api/winsvc/nf-winsvc-createservicea). Sie können ein vorhandenes Konto verwenden oder eines als Teil von Host-Computer installrt erstellen. Weitere Informationen finden Sie unter [Einrichten eines Dienst-Benutzerkontos](setting-up-a-serviceampaposs-user-account.md).
-   Authentifizierung Wenn Sie möchten, dass Clients die gegenseitige Kerberos-Authentifizierung verwenden, registrieren Sie die SPNs für das Anmelde Konto des Diensts. Wenn der Dienst unter dem Konto "LocalSystem" ausgeführt wird, ist das Anmelde Konto des Diensts das Computer Konto des Host Computers. Weitere Informationen finden Sie unter [Dienstprinzipalnamen](service-principal-names.md).
-   Gewähren von Zugriff. Stellen Sie sicher, dass der Dienst zur Laufzeit über die Zugriffsrechte und-Berechtigungen verfügt, die er zum Ausführen seiner Aufgaben benötigt. Dies kann das Festlegen von Zugriffs Steuerungs Einträgen (ACEs) in den Sicherheits Beschreibungen verschiedener Ressourcen, d. h. Verzeichnisobjekte, Dateifreigaben usw., erfordern, um die erforderlichen Zugriffsrechte für das Benutzer-oder Computer Konto zuzulassen. Weitere Informationen finden Sie unter [Erteilen von Zugriffsrechten für das Anmelde Konto des Diensts](granting-access-rights-to-the-service-logon-account.md).
-   Legen Sie Berechtigungen fest. Weisen Sie dem angegebenen Anmelde Konto Berechtigungen zu, z. b. das Recht, sich als Dienst beim Host Computer anzumelden. Weitere Informationen finden Sie unter [erteilen der Berechtigung "Anmelden als Dienst" auf dem Host Computer](granting-logon-as-service-right-on-the-host-computer.md).

Nachdem ein Dienst installiert wurde, sind Wartungs Tasks für Ihr Dienst Anmelde Konto verfügbar. Weitere Informationen finden Sie unter [Anmelde Konto-Wartungs Tasks](logon-account-maintenance-tasks.md).

-   Kenn Wort Wartung. Bei einem Dienst, der unter einem Benutzerkonto ausgeführt wird, müssen Sie das Kennwort regelmäßig ändern und das Kennwort mit dem Kennwort synchron halten, das von einem oder mehreren lokalen Dienststeuerungs-Managern zum Starten des Dienstanbieter verwendet wird.
-   SPN-Wartung. Wenn sich ein Dienst Anmelde Konto ändert, entfernen Sie die für das alte Konto registrierten SPNs, und registrieren Sie Sie beim neuen Konto. Beachten Sie, dass ein Domänen Administrator das Konto, unter dem der Dienst ausgeführt wird, ändern kann, wenn ein Dienst installiert ist. Verwenden Sie Win32-Funktionen oder die Benutzeroberfläche des Verwaltungs Tools Computer Verwaltung.
-   ACE-Wartung. Wenn sich das Anmelde Konto eines Diensts ändert, müssen Sie ACEs und Gruppenmitgliedschaften aktualisieren, um sicherzustellen, dass der Dienst weiterhin auf die erforderlichen Ressourcen zugreifen kann.

 

 