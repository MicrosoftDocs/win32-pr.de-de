---
description: Wenn ein Prozess versucht, auf ein sicherungsfähiges Objekt zu zugreifen, durchlädt das System die Zugriffssteuerungseinträge (ACEs) in der DACL (Discretionary Access Control List) von Objekten, bis ACEs gefunden werden, die den angeforderten Zugriff zulassen oder verweigern.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Reihenfolge der ACEs in einer DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b5d017fe6441e90cded6458d8796dee301e3fa0fda01b7d088039abd9834ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907750"
---
# <a name="order-of-aces-in-a-dacl"></a>Reihenfolge der ACEs in einer DACL

Wenn [](/windows/desktop/SecGloss/p-gly) ein Prozess versucht, auf ein sicherungsfähiges Objekt zu zugreifen, durchlädt das System die Zugriffssteuerungseinträge (ACCESS [*Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) in der DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) des Objekts, bis ACEs gefunden werden, die den angeforderten Zugriff zulassen oder verweigern. Die Zugriffsrechte, die eine DACL einem Benutzer zulässt, können je nach Reihenfolge der ACEs in der DACL variieren. Folglich definiert das Windows XP-Betriebssystem eine bevorzugte Reihenfolge für ACEs in der DACL eines sicherungsfähiges Objekts. Die bevorzugte Reihenfolge bietet ein einfaches Framework, das sicherstellt, dass ein ACE, dem der Zugriff verweigert wird, tatsächlich den Zugriff verweigert. Weitere Informationen zum Systemalgorithmus zum Überprüfen des Zugriffs finden Sie unter Steuern des Zugriffs auf [ein Objekt durch DACLs.](how-dacls-control-access-to-an-object.md)

Für Windows Server 2003 und Windows XP wird die richtige Reihenfolge von ACEs durch die Einführung objektspezifischer ACEs und die automatische Vererbung kompliziert.

In den folgenden Schritten wird die bevorzugte Reihenfolge beschrieben:

1.  Alle expliziten ACEs werden in einer Gruppe vor allen geerbten ACEs platziert.
2.  Innerhalb der Gruppe der expliziten ACEs werden Zugriffs verweigerte ACEs vor Zugriffsberechtigungs-ACEs platziert.
3.  Geerbte ACEs werden in der Reihenfolge platziert, in der sie geerbt werden. ACEs, die vom übergeordneten Element des untergeordneten Objekts geerbt wurden, kommen zuerst, dann aces, die vom über- und übergeordneten Objekt geerbt wurden, und so weiter oben in der Struktur der Objekte.
4.  Für jede Ebene von geerbten ACEs werden zugriffsgeementierte ACEs vor zugriffsgee zugelassenen ACEs platziert.

Natürlich sind nicht alle ACE-Typen in einer ACL erforderlich.

Funktionen wie [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) und [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) fügen am Ende einer ACL einen ACE hinzu. Es liegt in der Verantwortung des Aufrufers, sicherzustellen, dass die ACEs in der richtigen Reihenfolge hinzugefügt werden.

 

 
