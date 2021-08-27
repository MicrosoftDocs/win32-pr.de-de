---
description: Die Kerberos-Ticketrichtlinie wird auf Domänenebene definiert und durch den Schlüsselverteilungscenter (KDC) der Domäne implementiert.
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Kerberos-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d1dd394c42028c70f560fcb7f83b42bab506fbd222f877857be362a450041
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127310"
---
# <a name="kerberos-policy"></a>Kerberos-Richtlinie

Die Kerberos-Ticketrichtlinie wird auf Domänenebene definiert und durch den Schlüsselverteilungscenter (KDC) [*der*](../secgloss/k-gly.md) Domäne implementiert. Die Kerberos-Richtlinie wird in Active Directory als Teilmenge der Attribute der Domänensicherheitsrichtlinie gespeichert. Standardmäßig können Richtlinienoptionen nur von Mitgliedern der Gruppe Domänenadministratoren festgelegt werden. Die Domänenrichtlinie enthält Optionen, die Folgendes umfassen:

-   Support für postdierte Tickets
-   Eingeschränkte Delegierung unterstützen (nur Windows Server 2003)
-   Supporttickets, die weitergeleitet werden können
-   Support für Tickets
-   Festlegen des maximalen Ticketalters
-   Festlegen des maximalen Verlängerungsalters
-   Festlegen des maximalen Proxyticketalters
-   Er forcibly log off users when tickets expire (Benutzer abmelden, wenn Tickets ablaufen)

Bei [*eingeschränkter Delegierung*](../secgloss/c-gly.md)kann ein Computer so festgelegt werden, dass die Weiterleitung von Anmeldeinformationen nur an eine bestimmte Liste von Diensten zulässig ist. Diese Dienste müssen sich in derselben Domäne befinden wie der Computer, der die Anmeldeinformationen weiterleiten. Bei *eingeschränkter Delegierung* werden Keine Tickets mehr vom Client an den Server gesendet. Der Servercomputer erstellt Diensttickets, die bei Bedarf aus Informationen weitergeleitet werden, die zum Authentifizieren des Clients verwendet werden.

Obwohl die Kerberos-Richtlinie für eine Domäne möglicherweise eine delegierte Authentifizierung zu ermöglicht, indem Tickets weitergeleitet werden können, muss dieser Aspekt der Richtlinie nicht für alle Benutzer oder alle Computer gelten. Ein Attribut eines einzelnen Benutzerkontos kann festgelegt werden, um die Weiterleitung der Anmeldeinformationen dieses Benutzers durch [*einen*](../secgloss/c-gly.md) beliebigen Server zu deaktivieren. Ein Attribut des Kontos eines einzelnen Computers kann festgelegt werden, um die Weiterleitung von Anmeldeinformationen von einem beliebigen Benutzer zu deaktivieren. In beiden Fällen kann die Delegierung deaktiviert werden, indem eine Gruppenrichtlinie erstellt wird, die für alle Benutzer oder alle Computer in einer Organisationseinheit von Active Directory gilt.

**Windows XP/2000:** Eingeschränkte Delegierung wird nicht unterstützt.

 

 
