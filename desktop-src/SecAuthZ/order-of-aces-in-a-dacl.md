---
description: Wenn ein Prozess versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, durchläuft das System die Zugriffs Steuerungs Einträge (ACEs) in der Zugriffs Steuerungs Liste für Objekte (DACL), bis es ACEs findet, die den angeforderten Zugriff zulassen oder verweigern.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Reihenfolge von ACEs in einer DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359154"
---
# <a name="order-of-aces-in-a-dacl"></a>Reihenfolge von ACEs in einer DACL

Wenn ein [*Prozess*](/windows/desktop/SecGloss/p-gly) versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, durchläuft das System die [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) in der freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des Objekts, bis es ACEs findet, die den angeforderten Zugriff zulassen oder verweigern. Die Zugriffsrechte, die eine DACL einem Benutzer ermöglicht, können abhängig von der Reihenfolge der ACEs in der DACL variieren. Folglich definiert das Betriebssystem Windows XP eine bevorzugte Reihenfolge für ACEs in der DACL eines Sicherungs fähigen Objekts. Die bevorzugte Reihenfolge bietet ein einfaches Framework, mit dem sichergestellt wird, dass der Zugriff verweigert wird. Weitere Informationen zum Algorithmus des Systems zum Überprüfen des Zugriffs finden [Sie Untersteuern des Zugriffs auf ein Objekt durch DACLs](how-dacls-control-access-to-an-object.md).

Für Windows Server 2003 und Windows XP ist die richtige Reihenfolge von ACEs durch die Einführung von Objekt spezifischen ACEs und automatischer Vererbung kompliziert.

In den folgenden Schritten wird die bevorzugte Reihenfolge beschrieben:

1.  Alle expliziten ACEs werden in einer Gruppe vor allen geerbten ACEs platziert.
2.  Innerhalb der Gruppe von expliziten ACEs werden Zugriffs Verweigerungs-ACEs vor Zugriffs zulässigen ACEs platziert.
3.  Geerbte ACEs werden in der Reihenfolge abgelegt, in der Sie geerbt werden. ACEs, die vom übergeordneten Element des untergeordneten Objekts geerbt werden, werden zuerst angezeigt, dann ACEs, die vom übergeordneten Element geerbt wurden, usw., die Struktur von Objekten.
4.  Für jede Ebene der geerbten ACEs werden Zugriffs Verweigerungs-ACEs vor Zugriffs zulässigen ACEs platziert.

Natürlich sind nicht alle ACE-Typen in einer ACL erforderlich.

Funktionen wie [**addaccesszuwedaceex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) und [**addaccesszuwedobjectace**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) fügen am Ende einer ACL einen ACE hinzu. Es liegt in der Verantwortung des Aufrufers, sicherzustellen, dass die ACEs in der richtigen Reihenfolge hinzugefügt werden.

 

 
