---
title: Verwenden eines Domänen Benutzerkontos als Dienst Anmelde Konto
description: Bei einem Domänenbenutzerkonto können mit dem Dienst die Dienstsicherheitsfunktionen von Windows und Microsoft Active Directory Domain Services in vollem Umfang genutzt werden.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: f482359eb8445cacef12c46716ecde662a95d46d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106364018"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Verwenden eines Domänen Benutzerkontos als Dienst Anmelde Konto

Bei einem Domänenbenutzerkonto können mit dem Dienst die Dienstsicherheitsfunktionen von Windows und Microsoft Active Directory Domain Services in vollem Umfang genutzt werden. Der Dienst verfügt über den lokalen Zugriff und den Netzwerk Zugriff, der dem Konto oder allen Gruppen, denen das Konto angehört, gewährt wird. Der Dienst kann die gegenseitige Kerberos-Authentifizierung unterstützen.

> [!Note]  
> Die folgende Dokumentation ist für Entwickler konzipiert. Wenn Sie ein Endbenutzer sind, der Informationen zu einer Fehlermeldung im Zusammenhang mit Domänen Benutzerkonten sucht, finden Sie weitere Informationen in den [Microsoft Community-Foren](https://answers.microsoft.com). Weitere Informationen zum Verwalten von Domänen Benutzerkonten finden Sie unter [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

Der Vorteil der Verwendung eines Domänen Benutzerkontos besteht darin, dass die Dienst Aktionen durch die Zugriffsrechte und Berechtigungen, die dem Konto zugeordnet sind, eingeschränkt sind. Im Gegensatz zu einem `LocalSystem` Dienst können Fehler in einem Benutzerkonten Dienst das System nicht beschädigen. Wenn der Dienst durch einen Sicherheitsangriff kompromittiert wird, wird der Schaden für die Vorgänge isoliert, die das Benutzerkonto zulässt. Gleichzeitig können Clients, die mit unterschiedlichen Berechtigungsstufen ausgeführt werden, eine Verbindung mit dem Dienst herstellen, sodass der Dienst die Identität eines Clients annehmen kann, um sensible Vorgänge auszuführen.

Das Benutzerkonto eines Dienstanbieter sollte kein Mitglied der Gruppe "Administratoren" sein, die lokal, Domäne oder Unternehmen sind. Wenn Ihr Dienst lokale Administratorrechte benötigt, führen Sie ihn unter dem `LocalSystem` Konto aus. Für Vorgänge, die Domänen Administratorrechte erfordern, führen Sie diese durch die Identität des Sicherheits Kontexts einer Client Anwendung aus.

Eine Dienst Instanz, die ein Domänen Benutzerkonto verwendet, erfordert regelmäßige administrative Aktionen zur Beibehaltung des Konto Kennworts. Der Dienststeuerungs-Manager (SCM) auf dem Host Computer einer Dienst Instanz speichert das Konto Kennwort für die Verwendung bei der Protokollierung des Diensts zwischen. Wenn Sie das Konto Kennwort ändern, müssen Sie auch das zwischengespeicherte Kennwort auf dem Host Computer aktualisieren, auf dem der Dienst installiert ist. Weitere Informationen und ein Codebeispiel finden Sie unter [Ändern des Kennworts für das Benutzerkonto eines Dienstanbieter](changing-the-password-on-a-serviceampaposs-user-account.md). Sie könnten die reguläre Wartung vermeiden, indem Sie das Kennwort unverändert lassen, aber dies würde die Wahrscheinlichkeit eines Kenn Wort Angriffs auf das Dienst Konto erhöhen. Beachten Sie, dass auch wenn der SCM das Kennwort in einem sicheren Teil der Registrierung speichert, aber trotzdem einem Angriff ausgesetzt ist.

Ein Domänen Benutzerkonto verfügt über zwei namens Formate: den Distinguished Name des Benutzer Objekts im Verzeichnis und das Format "", das <domain> \\ <username> vom lokalen Dienststeuerungs-Manager verwendet wird. Weitere Informationen und ein Codebeispiel, das von einem Format in ein anderes konvertiert, finden Sie unter [Konvertieren von Domänen Konto-namens Formaten](converting-domain-account-name-formats.md).

 

 
