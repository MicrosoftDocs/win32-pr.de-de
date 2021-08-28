---
title: Verwenden eines Domänenbenutzerkontos als Dienstanmeldungskonto
description: Bei einem Domänenbenutzerkonto können mit dem Dienst die Dienstsicherheitsfunktionen von Windows und Microsoft Active Directory Domain Services in vollem Umfang genutzt werden.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: c8defc6cc3b35ca88038ca3818b56024dfb18699
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881448"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Verwenden eines Domänenbenutzerkontos als Dienstanmeldungskonto

Bei einem Domänenbenutzerkonto können mit dem Dienst die Dienstsicherheitsfunktionen von Windows und Microsoft Active Directory Domain Services in vollem Umfang genutzt werden. Der Dienst verfügt über den lokalen Und Netzwerkzugriff, der dem Konto oder allen Gruppen gewährt wird, deren Mitglied das Konto ist. Der Dienst kann die gegenseitige Kerberos-Authentifizierung unterstützen.

> [!Note]  
> Die folgende Dokumentation richtet sich an Entwickler. Wenn Sie ein Endbenutzer sind und Informationen zu einer Fehlermeldung mit Domänenbenutzerkonten suchen, finden Sie weitere Informationen in den [Microsoft-Communityforen.](https://answers.microsoft.com) Informationen zum Verwalten von Domänenbenutzerkonten finden Sie unter [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

Der Vorteil der Verwendung eines Domänenbenutzerkontos besteht darin, dass die Aktionen des Diensts durch die dem Konto zugeordneten Zugriffsrechte und Berechtigungen eingeschränkt sind. Im Gegensatz zu einem `LocalSystem` Dienst können Fehler in einem Benutzerkontodienst das System nicht beschädigen. Wenn der Dienst durch einen Sicherheitsangriff kompromittiert wird, wird der Schaden für die Vorgänge isoliert, die das System dem Benutzerkonto zulässt. Gleichzeitig können Clients, die auf unterschiedlichen Berechtigungsebenen ausgeführt werden, eine Verbindung mit dem Dienst herstellen, wodurch der Dienst die Identität eines Clients annehmen kann, um vertrauliche Vorgänge auszuführen.

Das Benutzerkonto eines Diensts darf kein Mitglied von Administratorgruppen sein, die lokal, domäne oder unternehmenseigen sind. Wenn Ihr Dienst lokale Administratorrechte benötigt, führen Sie ihn unter dem `LocalSystem` Konto aus. Führen Sie für Vorgänge, für die Domänenverwaltungsberechtigungen erforderlich sind, diese aus, indem Sie die Identität des Sicherheitskontexts einer Clientanwendung annehmen.

Eine Dienstinstanz, die ein Domänenbenutzerkonto verwendet, erfordert regelmäßige administrative Aktionen, um das Kontokennwort zu verwalten. Der Dienststeuerungs-Manager (Service Control Manager, SCM) auf dem Hostcomputer einer Dienstinstanz speichert das Kontokennwort für die Protokollierung des Diensts zwischen. Wenn Sie das Kontokennwort ändern, müssen Sie auch das zwischengespeicherte Kennwort auf dem Hostcomputer aktualisieren, auf dem der Dienst installiert ist. Weitere Informationen und ein Codebeispiel finden Sie unter Ändern des Kennworts für [das Benutzerkonto eines Diensts.](changing-the-password-on-a-serviceampaposs-user-account.md) Sie können die regelmäßige Wartung vermeiden, indem Sie das Kennwort unverändert lassen, aber dies würde die Wahrscheinlichkeit eines Kennwortangriffs auf das Dienstkonto erhöhen. Beachten Sie, dass der SCM das Kennwort zwar in einem sicheren Teil der Registrierung speichert, aber trotzdem einem Angriff ausgesetzt ist.

Ein Domänenbenutzerkonto verfügt über zwei Namensformate: den Distinguished Name des Benutzerobjekts im Verzeichnis und das &lt; Format &gt; \\ &lt; "Domänenbenutzername", &gt; das vom lokalen Dienststeuerungs-Manager verwendet wird. Weitere Informationen und ein Codebeispiel, das von einem Format in das andere konvertiert wird, finden Sie unter [Converting Domain Account Name Formats](converting-domain-account-name-formats.md).

 

 
