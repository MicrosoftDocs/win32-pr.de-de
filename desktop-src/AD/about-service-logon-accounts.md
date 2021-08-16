---
title: Informationen zu Dienstanmeldungskonten
description: Wenn ein Win32-basierter Dienst gestartet wird, meldet er sich beim lokalen Computer an.
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ba72ffca4362f42c6a5ad6ee494e36e9698d7883c19e3fe2a157e153ce556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841020"
---
# <a name="about-service-logon-accounts"></a>Informationen zu Dienstanmeldungskonten

Wenn ein Win32-basierter Dienst gestartet wird, meldet er sich beim lokalen Computer an. Die Anmeldung ist möglich wie:

-   Ein lokales Benutzerkonto oder ein Domänenbenutzerkonto.
-   Das LocalSystem-Konto.

Das Anmeldekonto bestimmt die Sicherheitsidentität des Diensts zur Laufzeit, d.&a0;B. den primären Sicherheitskontext des Diensts. Der Sicherheitskontext bestimmt die Fähigkeit des Diensts, auf lokale Ressourcen und Netzwerkressourcen zu zugreifen. Beispielsweise kann ein Dienst, der im Sicherheitskontext eines lokalen Benutzerkontos ausgeführt wird, nicht auf Netzwerkressourcen zugreifen. Umgekehrt hätte ein Dienst, der im Sicherheitskontext des LocalSystem-Kontos auf einem Windows 2000-Domänencontroller (DC) ausgeführt wird, uneingeschränkten Zugriff auf den Domänencontroller. Weitere Informationen und eine Erörterung der Vorteile und Einschränkungen zwischen Benutzerkonten und LocalSystem finden Sie unter [Sicherheitskontexte und Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).

Letztendlich haben Administratoren auf dem System, auf dem der Dienst installiert ist, die Kontrolle über das Anmeldekonto des Diensts. Aus Sicherheitsgründen lassen einige Administratoren möglicherweise nicht zu, dass Sie Ihren Dienst unter dem LocalSystem-Konto installieren. Ihr Dienst muss unter einem Domänenbenutzerkonto ausgeführt werden können. Als Programmierer können Sie etwas Kontrolle über das Anmeldekonto Ihres Diensts haben. Ihr Dienstinstallationsprogramm gibt das Anmeldekonto des Diensts an, wenn es die [**CreateService-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) aufruft, um den Dienst auf einem Hostcomputer zu installieren. Ihr Installationsprogramm kann ein Standardanmeldungskonto vorschlagen, aber es sollte einem Administrator ermöglichen, das tatsächliche Konto anzugeben.

Ihr Installationsprogramm kann auch die folgenden Aufgaben im Zusammenhang mit dem Anmeldekonto Ihres Diensts ausführen:

-   Die Installation. Wenn Sie Ihren Dienst für die Ausführung unter einem Benutzerkonto installieren, muss das Konto vorhanden sein, bevor Sie [**CreateService aufrufen.**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) Sie können ein vorhandenes Konto verwenden oder im Rahmen der Host-Computer-Installation ein Konto erstellen. Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos eines Diensts.](setting-up-a-serviceampaposs-user-account.md)
-   Authentifizierung Wenn Clients die gegenseitige Kerberos-Authentifizierung verwenden möchten, registrieren Sie die SPNs im Anmeldekonto des Diensts. Wenn der Dienst unter dem LocalSystem-Konto ausgeführt wird, ist das Anmeldekonto des Diensts das Computerkonto des Hostcomputers. Weitere Informationen finden Sie unter [Dienstprinzipalnamen](service-principal-names.md).
-   Gewähren sie Zugriff. Stellen Sie sicher, dass der Dienst zur Laufzeit über die Zugriffsrechte und Berechtigungen verfügt, die er zum Ausführen seiner Aufgaben benötigt. Dies kann das Festlegen von Zugriffssteuerungseinträgen (Access Control Entries, ACEs) in den Sicherheitsbeschreibungen verschiedener Ressourcen erfordern, d. h. Verzeichnisobjekte, Dateifreigaben und so weiter, um die erforderlichen Zugriffsrechte für das Benutzer- oder Computerkonto zu ermöglichen. Weitere Informationen finden Sie unter [Gewähren von Zugriffsrechten für das Dienstanmeldungskonto.](granting-access-rights-to-the-service-logon-account.md)
-   Legen Sie Berechtigungen fest. Weisen Sie dem angegebenen Anmeldekonto Berechtigungen zu, z. B. das Recht, sich als Dienst auf dem Hostcomputer zu anmelden. Weitere Informationen finden Sie unter [Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md).

Nach der Installation eines Diensts gibt es Wartungsaufgaben, die sich auf Ihr Dienstanmeldungskonto beziehen. Weitere Informationen finden Sie unter [Anmeldekontowartungsaufgaben.](logon-account-maintenance-tasks.md)

-   Kennwortwartung. Für einen Dienst, der unter einem Benutzerkonto ausgeführt wird, müssen Sie das Kennwort in regelmäßigen Abständen ändern und das Kennwort mit dem Kennwort synchronisieren, das von mindestens einem lokalen Dienststeuerungs-Manager zum Starten des Diensts verwendet wird.
-   SPN-Wartung. Wenn sich ein Dienstanmeldungskonto ändert, entfernen Sie die für das alte Konto registrierten SPNs, und registrieren Sie sie für das neue Konto. Beachten Sie, dass ein Domänenadministrator bei der Installation eines Diensts das Konto ändern kann, unter dem Ihr Dienst ausgeführt wird. Verwenden Sie Win32-Funktionen oder die Benutzeroberfläche des Verwaltungstools für die Computerverwaltung.
-   ACE-Wartung. Wenn sich ein Dienstanmeldungskonto ändert, müssen Sie ACEs und Gruppenmitgliedschaften aktualisieren, um sicherzustellen, dass der Dienst weiterhin auf die erforderlichen Ressourcen zugreifen kann.

 

 