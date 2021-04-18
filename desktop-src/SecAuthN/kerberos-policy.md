---
description: Die Kerberos-Ticket Richtlinie wird auf Domänen Ebene definiert und durch die Schlüsselverteilungscenter der Domäne (KDC) implementiert.
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Kerberos-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359108"
---
# <a name="kerberos-policy"></a>Kerberos-Richtlinie

Die Kerberos-Ticket Richtlinie wird auf Domänen Ebene definiert und durch die [*Schlüsselverteilungscenter*](../secgloss/k-gly.md) der Domäne (KDC) implementiert. Die Kerberos-Richtlinie wird in der Active Directory als eine Teilmenge der Attribute der Domänen Sicherheitsrichtlinie gespeichert. Standardmäßig können Richtlinien Optionen nur von Mitgliedern der Gruppe "Domänen Administratoren" festgelegt werden. Die Domänen Richtlinie umfasst folgende Optionen:

-   Unterstützung von postveralteten Tickets
-   Unterstützung der eingeschränkten Delegierung (nur Windows Server 2003)
-   Support Tickets, die weitergeleitet werden können
-   Unterstützen von erneuerbaren Tickets
-   Festlegen des maximalen Ticket Alters
-   Festlegen des maximalen Erneuerungs Alters
-   Festlegen des maximalen proxyticket-Alters
-   Abmeldung von Benutzern beim Ablaufen von Tickets erzwingen

Bei der [*eingeschränkten Delegierung*](../secgloss/c-gly.md)kann ein Computer so festgelegt werden, dass die Weiterleitung von Anmelde Informationen nur an eine bestimmte Liste von Diensten zulässig ist. Diese Dienste müssen sich in derselben Domäne befinden wie der Computer, der die Anmelde Informationen weiterleitet. Bei der *eingeschränkten Delegierung* werden Tickets nicht mehr vom Client an den Server gesendet. Der Server Computer erstellt nach Bedarf Dienst Tickets, die zum Authentifizieren des Clients verwendet werden.

Obwohl die Kerberos-Richtlinie für eine Domäne die delegierte Authentifizierung zulässt, indem Tickets weitergeleitet werden können, muss dieser Aspekt der Richtlinie nicht für alle Benutzer oder alle Computer gelten. Ein Attribut eines einzelnen Benutzerkontos kann festgelegt werden, um die Weiterleitung der [*Anmelde*](../secgloss/c-gly.md) Informationen dieses Benutzers durch einen beliebigen Server zu deaktivieren. Ein Attribut des Kontos eines einzelnen Computers kann festgelegt werden, um die Weiterleitung von Anmelde Informationen von einem beliebigen Benutzer zu deaktivieren. In beiden Fällen können Sie die Delegierung deaktivieren, indem Sie eine Gruppenrichtlinie erstellen, die für alle Benutzer oder alle Computer in einer Organisationseinheit der Active Directory gilt.

**Windows XP/2000:** Die eingeschränkte Delegierung wird nicht unterstützt.

 

 
