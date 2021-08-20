---
description: Wenn ein Thread versucht, auf ein sicherungsfähiges Objekt zu zugreifen, gewährt oder verweigert das System den Zugriff.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Funktionsweise von AccessCheck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c593c0c50fa1e78639d18bc5c2f372e9c0edd0690e9b338a5126794da54509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671970"
---
# <a name="how-accesscheck-works"></a>Funktionsweise von AccessCheck

Wenn ein Thread versucht, auf ein sicherungsfähiges Objekt zu zugreifen, gewährt oder verweigert das System den Zugriff. Wenn das Objekt nicht über eine DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) verfügt, gewährt das System Zugriff. Andernfalls sucht das System [Access Control Einträge](access-control-entries.md) (ACEs) in der DACL des Objekts, die für den Thread gelten. Jeder ACE in der DACL des Objekts gibt die Zugriffsrechte an, die für einen Vertrauenshänder zulässig oder verweigert werden. Dabei kann es sich um ein Benutzerkonto, ein Gruppenkonto oder eine Anmeldesitzung um einen Benutzer oder eine [*Anmeldesitzung von .*](/windows/desktop/SecGloss/l-gly) [](trustees.md)

## <a name="dacls"></a>DACLs

Das System vergleicht den Vertrauenshänder in jedem ACE mit den Vertrauenshändern, die im Zugriffstoken des [Threads identifiziert werden.](access-tokens.md) Ein Zugriffstoken enthält [*Sicherheits-IDs*](/windows/desktop/SecGloss/s-gly) (SIDs), die den Benutzer und die Gruppenkonten identifizieren, zu denen der Benutzer gehört. Ein Token enthält auch eine [*Anmelde-SID,*](/windows/desktop/SecGloss/l-gly) die die aktuelle Anmeldesitzung identifiziert. Während einer Zugriffsüberprüfung ignoriert das System Gruppen-SIDs, die nicht aktiviert sind. Weitere Informationen zu aktivierten, deaktivierten und nur verweigernden SIDs finden Sie unter [SID-Attribute in einem Zugriffstoken.](sid-attributes-in-an-access-token.md)

In der Regel verwendet das System das [*primäre Zugriffstoken*](/windows/desktop/SecGloss/p-gly) des Threads, der Zugriff an fordert. Wenn der Thread jedoch die Identität eines anderen Benutzers anwechselt, verwendet das System das [*Identitätswechseltoken des Threads.*](/windows/desktop/SecGloss/i-gly)

Das System überprüft jeden ACE nacheinander, bis eines der folgenden Ereignisse eintritt:

-   Ein ACE, dem der Zugriff verweigert wird, verweigert explizit alle angeforderten Zugriffsrechte einem der Vertrauenshänder, die im Zugriffstoken des Threads aufgeführt sind. [](access-rights-and-access-masks.md)
-   Mindestens ein Zugriffsberechtigungs-ACEs für Vertrauenshänder, die im Zugriffstoken des Threads aufgeführt sind, gewähren explizit alle angeforderten Zugriffsrechte.
-   Alle ACEs wurden überprüft, und es gibt immer noch mindestens ein angefordertes Zugriffsrecht, das nicht explizit zugelassen wurde. In diesem Fall wird der Zugriff implizit verweigert.

Die folgende Abbildung zeigt, wie die DACL eines Objekts den Zugriff auf einen Thread zulassen kann, während der Zugriff auf einen anderen verweigert wird.

![Dacl, die unterschiedliche Zugriffsrechte für verschiedene Threads gewährt](images/accctrl1.png)

Für Thread A liest das System ACE 1 und verweigert sofort den Zugriff, da der ZUGRIFFS VERWEIGERTE ACE für den Benutzer im Zugriffstoken des Threads gilt. In diesem Fall überprüft das System acEs 2 und 3 nicht. Für Thread B gilt ACE 1 nicht, sodass das System zu ACE 2 übergeht, der Schreibzugriff zulässt, und ACE 3, der Lese- und Ausführungszugriff zulässt.

Da das System die Überprüfung von ACEs beendet, wenn der angeforderte Zugriff explizit gewährt oder verweigert wird, ist die Reihenfolge der ACEs in einer DACL wichtig. Beachten Sie, dass das System möglicherweise Zugriff auf Thread A gewährt hat, wenn sich die ACE-Reihenfolge im Beispiel unterscheiden würde. Für Systemobjekte definiert das Betriebssystem eine bevorzugte Reihenfolge [von ACEs in einer DACL.](order-of-aces-in-a-dacl.md)

 

 
