---
description: Erläutert integrierte und Konto Domänen auf Windows-basierten Systemen.
ms.assetid: 306c258b-950e-4506-99e2-67a3714285ff
title: Integrierte und Konto Domänen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d2d4bb18e1ac2ea33aaff008475a44515d9231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347509"
---
# <a name="built-in-and-account-domains"></a>Integrierte und Konto Domänen

Domänen in einem Windows-basierten System fallen in die folgenden beiden Kategorien:

-   [Computer, die keine Domänen Controller sind](#computers-that-are-not-domain-controllers)
-   [Computer mit Domänen Controllern](#computers-that-are-domain-controllers)

## <a name="computers-that-are-not-domain-controllers"></a>Computer, die keine Domänen Controller sind

Die SAM-Datenbank (Security Accounts Manager) befindet sich auf jedem Computer und verwaltet die Konten für die integrierte Domäne und die Konto Domäne.



| Domain          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integrierte Domäne | Diese Domäne enthält lokale Standard Gruppen, wie z. b. die Administratoren und Benutzergruppen, die bei der Installation des Betriebssystems eingerichtet werden. Der Name dieser Domäne ist eine lokalisierte Version von Builtin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Kontodomäne  | Die Konto Domäne kann Benutzer-, Gruppen-und lokale Gruppenkonten enthalten. Das Administrator Konto befindet sich in dieser Domäne. Die Konten, die in der Konto Domäne einer Arbeitsstation oder eines Mitglieds Servers definiert sind, sind auf Ressourcen beschränkt, die sich auf dem physischen Computer befinden, auf dem sich das Konto befindet. Auf einem System, das nicht Teil eines Netzwerks ist und daher keine [primäre Domäne](primary-and-trusted-domains.md)hat, wird die Konto Domäne verwendet, um alle Konten zu beherbergen, die Zugriff auf den Computer ermöglichen. Auf einem System, das Teil eines Netzwerks ist, wird die Konto Domäne des Computers verwendet, um Konten zu beherbergen, die nicht auf Netzwerkressourcen zugreifen. Konten, die Zugriff auf das Netzwerk benötigen, müssen in der Konto Domäne eines Domänen Controllers definiert werden.<br/> Der Name dieser Domäne wird zum Zeitpunkt der Systeminstallation zugewiesen und durch den Computernamen bestimmt. Wenn der Computername geändert wird, wird der Konto Domänen Name erst aktualisiert, wenn der Computer neu gestartet wird.<br/> |



 

## <a name="computers-that-are-domain-controllers"></a>Computer mit Domänen Controllern

Domänen Controller verfügen nicht über integrierte oder Konto Domänen. Außerdem verwenden diese Systeme anstelle einer SAM-Datenbank den Microsoft Active Directory Directory-Dienst, um Konto Zugriffs Informationen zu speichern. Weitere Informationen finden Sie unter [Active Directory](/windows/desktop/AD/active-directory-domain-services).

 

