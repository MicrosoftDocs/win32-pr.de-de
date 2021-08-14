---
title: Verwenden eines Domänenbenutzerkontos als Dienstanmeldungskonto
description: Bei einem Domänenbenutzerkonto können mit dem Dienst die Dienstsicherheitsfunktionen von Windows und Microsoft Active Directory Domain Services in vollem Umfang genutzt werden.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 7c61816fa140a6126d020285d80a71fb59cc1808ae6888f12dc0e4340447060e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192248"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Verwenden eines Domänenbenutzerkontos als Dienstanmeldungskonto

Bei einem Domänenbenutzerkonto können mit dem Dienst die Dienstsicherheitsfunktionen von Windows und Microsoft Active Directory Domain Services in vollem Umfang genutzt werden. Der Dienst verfügt über jeglichen lokalen und Netzwerkzugriff, der dem Konto oder allen Gruppen gewährt wird, deren Mitglied das Konto ist. Der Dienst kann die gegenseitige Kerberos-Authentifizierung unterstützen.

> [!Note]  
> Die folgende Dokumentation ist für Entwickler. Wenn Sie ein Endbenutzer sind, der nach Informationen zu einer Fehlermeldung im Zusammenhang mit Domänenbenutzerkonten sucht, lesen Sie die [Microsoft-Communityforen](https://answers.microsoft.com). Informationen zum Verwalten von Domänenbenutzerkonten finden Sie unter [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

Der Vorteil der Verwendung eines Domänenbenutzerkontos ist, dass die Aktionen des Diensts durch die dem Konto zugeordneten Zugriffsrechte und Berechtigungen eingeschränkt sind. Im Gegensatz `LocalSystem` zu einem Dienst können Fehler in einem Benutzerkontodienst das System nicht beschädigen. Wenn der Dienst durch einen Sicherheitsangriff kompromittiert wird, wird der Schaden auf die Vorgänge isoliert, die das System dem Benutzerkonto zulässt. Gleichzeitig können Clients, die auf unterschiedlichen Berechtigungsebenen ausgeführt werden, eine Verbindung mit dem Dienst herstellen, wodurch der Dienst die Identität eines Clients für sensible Vorgänge imitieren kann.

Das Benutzerkonto eines Diensts sollte kein Mitglied von Administratorgruppen sein, die lokal, in der Domäne oder im Unternehmen sind. Wenn Ihr Dienst lokale Administratorrechte benötigt, führen Sie ihn unter dem Konto `LocalSystem` aus. Führen Sie für Vorgänge, die Domänenadministratorrechte erfordern, diese durch Identitätswechsel des Sicherheitskontexts einer Clientanwendung aus.

Eine Dienstinstanz, die ein Domänenbenutzerkonto verwendet, erfordert regelmäßige administrative Aktionen, um das Kontokennwort zu verwalten. Der Dienststeuerungs-Manager (Service Control Manager, SCM) auf dem Hostcomputer einer Dienstinstanz speichert das Kontokennwort für die Protokollierung beim Dienst zwischen. Wenn Sie das Kontokennwort ändern, müssen Sie auch das zwischengespeicherte Kennwort auf dem Hostcomputer aktualisieren, auf dem der Dienst installiert ist. Weitere Informationen und ein Codebeispiel finden Sie unter Ändern des Kennworts für das [Benutzerkonto eines Diensts.](changing-the-password-on-a-serviceampaposs-user-account.md) Sie können die regelmäßige Wartung vermeiden, indem Sie das Kennwort unverändert lassen. Dies würde jedoch die Wahrscheinlichkeit eines Kennwortangriffs auf das Dienstkonto erhöhen. Beachten Sie, dass das Kennwort zwar vom SCM in einem sicheren Teil der Registrierung gespeichert wird, aber dennoch Angriffen unterliegt.

Ein Domänenbenutzerkonto verfügt über zwei Namensformate: den Distinguished Name des Benutzerobjekts im Verzeichnis und das Format " ", das vom lokalen Dienststeuerungs-Manager <domain> \\ <username> verwendet wird. Weitere Informationen und ein Codebeispiel, das von einem Format in das andere konvertiert wird, finden Sie unter [Konvertieren von Domänenkontonamenformaten.](converting-domain-account-name-formats.md)

 

 
