---
title: Verwenden des Kontos "LocalSystem" als Dienst Anmelde Konto
description: Ein Vorteil der Ausführung unter dem LocalSystem-Konto besteht darin, dass der Dienst uneingeschränkten Zugriff auf lokale Ressourcen hat.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- LocalSystem-Konto
- LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bec3826984e28e29d3156b784da229f8e53e34e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947375"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Verwenden des Kontos "LocalSystem" als Dienst Anmelde Konto

Ein Vorteil der Ausführung unter dem LocalSystem-Konto besteht darin, dass der Dienst uneingeschränkten Zugriff auf lokale Ressourcen hat. Dies ist auch der Nachteil von LocalSystem, da ein LocalSystem-Dienst Aktionen ausführen kann, die das gesamte System heruntergefahren würden. Ein Dienst, der als "LocalSystem" auf einem Domänen Controller (DC) ausgeführt wird, verfügt insbesondere über uneingeschränkten Zugriff auf Active Directory Domain Services. Dies bedeutet, dass Fehler im Dienst oder Sicherheitsangriffe auf den Dienst das System beschädigen können. wenn sich der Dienst auf einem DC befindet, wird das gesamte Unternehmensnetzwerk beschädigt.

Aus diesen Gründen sind Domänen Administratoren mit vertraulichen Installationen vorsichtig, wenn Sie zulassen möchten, dass Dienste als "LocalSystem" ausgeführt werden. Tatsächlich können Sie Richtlinien dafür haben, insbesondere bei DCS. Wenn Ihr Dienst als "LocalSystem" ausgeführt werden muss, sollte die Dokumentation für Ihren Dienst für Domänen Administratoren die Gründe dafür begründen, dass der Dienst mit erhöhten Rechten ausgeführt werden muss. Dienste sollten nie als "LocalSystem" auf einem Domänen Controller ausgeführt werden. Weitere Informationen und ein Codebeispiel, das zeigt, wie ein Dienst-oder Dienst Installationsprogramm ermitteln kann, ob es auf einem Domänen Controller ausgeführt wird, finden Sie unter [testen, ob auf einem Domänen Controller ausgeführt](testing-whether-running-on-a-domain-controller.md)wird.

Wenn ein Dienst unter dem Konto "LocalSystem" auf einem Computer ausgeführt wird, der ein Domänen Mitglied ist, verfügt der Dienst über den Netzwerk Zugriff auf das Computer Konto oder auf alle Gruppen, denen das Computer Konto angehört. Beachten Sie, dass ein Domänen Computer Konto in Windows 2000 ein Dienst Prinzipal ist, ähnlich einem Benutzerkonto. Dies bedeutet, dass sich ein Computer Konto in einer Sicherheitsgruppe befinden kann, und ein ACE in einer Sicherheits Beschreibung kann den Zugriff auf ein Computer Konto gewähren. Beachten Sie, dass das Hinzufügen von Computer Konten zu Gruppen aus zwei Gründen nicht empfohlen wird:

-   Computer Konten unterliegen der Löschung und erneuten Erstellung, wenn der Computer die Domäne verlässt und dann erneut einleitet.
-   Wenn Sie ein Computer Konto zu einer Gruppe hinzufügen, sind alle als "LocalSystem" auf diesem Computer ausgeführt als "LocalSystem" fest zufügenden Dienste zulässig. Dies liegt daran, dass alle LocalSystem-Dienste das Computer Konto Ihres Host Servers gemeinsam verwenden. Aus diesem Grund ist es besonders wichtig, dass Computer Konten nicht als Mitglieder einer Gruppe von Domänen Administratoren erstellt werden.

Computer Konten verfügen in der Regel über wenige Berechtigungen und gehören nicht zu Gruppen. Der Standard-ACL-Schutz in Active Directory Domain Services den minimalen Zugriff auf Computer Konten ermöglicht. Folglich haben Dienste, die als "LocalSystem" ausgeführt werden, auf anderen Computern als DCS nur minimalen Zugriff auf Active Directory Domain Services.

Wenn Ihr Dienst unter "LocalSystem" ausgeführt wird, müssen Sie den Dienst auf einem Mitglieds Server testen, um sicherzustellen, dass der Dienst über ausreichende Berechtigungen zum Lesen/Schreiben von Active Directory-Domäne Controllern verfügt. Ein Domänen Controller darf nicht der einzige Windows-Computer sein, auf dem Sie den Dienst testen. Beachten Sie, dass ein Dienst, der unter "LocalSystem" auf einem Windows-Domänen Controller ausgeführt wird, über einen vollen Zugriff auf Active Directory Domain Services verfügt und dass ein Mitglieds Server im Kontext des Computer Kontos ausgeführt wird, das erheblich weniger Rechte hat.

 

 




