---
title: Verwenden des LocalSystem-Kontos als Dienstanmeldungskonto
description: Ein Vorteil der Ausführung unter dem LocalSystem-Konto ist, dass der Dienst vollständig uneingeschränkten Zugriff auf lokale Ressourcen hat.
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- localsystem-Konto
- Localsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ac31cb7b3e0ad335f9a2781187aadcb03a1529055eb0771856aa01543add0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024578"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>Verwenden des LocalSystem-Kontos als Dienstanmeldungskonto

Ein Vorteil der Ausführung unter dem LocalSystem-Konto ist, dass der Dienst vollständig uneingeschränkten Zugriff auf lokale Ressourcen hat. Dies ist auch der Nachteil von LocalSystem, da ein LocalSystem-Dienst Dinge durchführen kann, die das gesamte System aus dem System bringen würden. Insbesondere hat ein Dienst, der als LocalSystem auf einem Domänencontroller (DC) ausgeführt wird, uneingeschränkten Zugriff auf Active Directory Domain Services. Dies bedeutet, dass Fehler im Dienst oder Sicherheitsangriffe auf den Dienst das System beschädigen oder, wenn sich der Dienst auf einem Domänencontroller befindet, das gesamte Unternehmensnetzwerk beschädigen können.

Aus diesen Gründen sind Domänenadministratoren bei sensiblen Installationen vorsichtig, wenn sie zulassen, dass Dienste als LocalSystem ausgeführt werden. Tatsächlich verfügen sie möglicherweise über Richtlinien dafür, insbesondere auf DCs. Wenn Ihr Dienst als LocalSystem ausgeführt werden muss, sollte die Dokumentation für Ihren Dienst domänenadministratoren die Gründe dafür rechtfertigen, dem Dienst die Berechtigung zum Ausführen mit erhöhten Rechten zu gewähren. Dienste sollten nie als LocalSystem auf einem Domänencontroller ausgeführt werden. Weitere Informationen und ein Codebeispiel, das zeigt, wie ein Dienst- oder Dienstinstallationsprogramm feststellen kann, ob er auf einem Domänencontroller ausgeführt wird, finden Sie unter [Testen, ob auf einem Domänencontroller ausgeführt wird.](testing-whether-running-on-a-domain-controller.md)

Wenn ein Dienst unter dem LocalSystem-Konto auf einem Computer ausgeführt wird, der Mitglied einer Domäne ist, verfügt der Dienst über den Netzwerkzugriff, der dem Computerkonto oder allen Gruppen gewährt wird, deren Mitglied das Computerkonto ist. Beachten Sie, dass in Windows 2000 ein Domänencomputerkonto ein Dienstprinzipal ist, ähnlich wie ein Benutzerkonto. Dies bedeutet, dass sich ein Computerkonto in einer Sicherheitsgruppe befinden kann und ein ACE in einer Sicherheitsbeschreibung Zugriff auf ein Computerkonto gewähren kann. Beachten Sie, dass das Hinzufügen von Computerkonten zu Gruppen aus zwei Gründen nicht empfohlen wird:

-   Computerkonten können gelöscht und neu erstellt werden, wenn der Computer die Domäne verlässt und dann wieder eingeht.
-   Wenn Sie einer Gruppe ein Computerkonto hinzufügen, werden allen Diensten, die auf diesem Computer als LocalSystem ausgeführt werden, die Zugriffsrechte der Gruppe gewährt. Dies liegt daran, dass alle LocalSystem-Dienste das Computerkonto ihres Hostservers gemeinsam nutzen. Aus diesem Grund ist es besonders wichtig, dass Computerkonten nicht zu Mitgliedern von Domänenadministratorgruppen werden.

Computerkonten verfügen in der Regel nur über wenige Berechtigungen und gehören nicht zu Gruppen. Der Standardmäßige ACL-Schutz in Active Directory Domain Services ermöglicht minimalen Zugriff für Computerkonten. Folglich haben Dienste, die als LocalSystem auf anderen Computern als DCs ausgeführt werden, nur minimalen Zugriff auf Active Directory Domain Services.

Wenn Ihr Dienst unter LocalSystem ausgeführt wird, müssen Sie den Dienst auf einem Mitgliedsserver testen, um sicherzustellen, dass Ihr Dienst über ausreichende Lese-/Schreibberechtigungen für Active Directory-Domäne Controller verfügt. Ein Domänencontroller sollte nicht der einzige Windows Computer sein, auf dem Sie den Dienst testen. Beachten Sie, dass ein Dienst, der unter LocalSystem auf einem Windows Domänencontroller ausgeführt wird, vollständigen Zugriff auf Active Directory Domain Services hat und dass ein Mitgliedsserver im Kontext des Computerkontos ausgeführt wird, das über wesentlich weniger Rechte verfügt.

 

 




