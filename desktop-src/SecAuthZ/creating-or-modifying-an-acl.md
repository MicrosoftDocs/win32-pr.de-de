---
description: Windows unterstützt eine Reihe von Funktionen, die eine Zugriffssteuerungsliste (Access Control List, ACL) erstellen oder die Zugriffssteuerungseinträge (ACEs) in einer vorhandenen ACL ändern.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Erstellen oder Ändern einer ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120b445d37f8c4b82c2b0b2a775a06d68faa46ab5752cc25e913d43676e9a72e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782165"
---
# <a name="creating-or-modifying-an-acl"></a>Erstellen oder Ändern einer ACL

Windows unterstützt eine Reihe von Funktionen, die eine Zugriffssteuerungsliste (Access [*Control List,*](/windows/desktop/SecGloss/a-gly) ACL) erstellen oder die Zugriffssteuerungseinträge (Access [*Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) in einer vorhandenen ACL ändern.

Die [**SetEntriesInAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) erstellt eine neue ACL. **SetEntriesInAcl** kann einen völlig neuen Satz von ACEs für die ACL angeben oder einen oder mehrere neue ACEs mit den ACEs einer vorhandenen ACL zusammenführen. Die **SetEntriesInAcl-Funktion** verwendet ein Array von [**EXPLICIT \_ ACCESS-Strukturen,**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) um die Informationen für die neuen ACEs anzugeben. Jede **EXPLICIT \_ ACCESS-Struktur** enthält Informationen, die einen einzelnen ACE beschreiben. Diese Informationen umfassen die Zugriffsrechte, den Typ des ACE, die [](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) Flags, die die ACE-Vererbung steuern, und eine VERTRAUENS-Struktur, die den Vertrauenshänder identifiziert.

**So fügen Sie einer vorhandenen ACL einen neuen ACE hinzu**

1.  Verwenden Sie [**die Funktion GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) oder [**GetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) um die vorhandene DACL oder SACL aus dem Sicherheitsdeskriptor eines [*Objekts zu erhalten.*](/windows/desktop/SecGloss/s-gly)
2.  Rufen Sie für jeden neuen ACE die [**Funktion BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) auf, um eine [**EXPLICIT \_ ACCESS-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) mit den Informationen zu füllen, die den ACE beschreiben.
3.  Rufen [**Sie SetEntriesInAcl auf,**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla)und geben Sie dabei die vorhandene ACL und ein Array von [**EXPLICIT \_ ACCESS-Strukturen**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) für die neuen ACEs an. Die **SetEntriesInAcl-Funktion** ordnet die ACL und ihre ACEs zu und initialisiert sie.
4.  Rufen Sie [**die Funktion SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) oder [**SetNamedSecurityInfo auf,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) um die neue ACL an den Sicherheitsdeskriptor des Objekts anfügen.

Wenn der Aufrufer eine vorhandene ACL angibt, führt [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) die neuen ACE-Informationen mit den vorhandenen ACEs in der ACL zusammen. Stellen Sie sich beispielsweise den Fall vor, in dem die vorhandene Zugriffssteuerungsliste einem angegebenen Vertrauenshänder Zugriff gewährt und eine [**EXPLICIT \_ ACCESS-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) den Zugriff für denselben Vertrauenshänder verweigert. In diesem Fall fügt **SetEntriesInAcl** einen neuen ACE mit Zugriffsberechtigung für den Vertrauenshänder hinzu und löscht oder ändert den vorhandenen zugriffsbasierten ACE für den Vertrauenshänder.

Beispielcode, der einen neuen ACE mit einer vorhandenen ACL zusammenführungst, finden Sie unter [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md)(Ändern der ACLs eines Objekts in C++).

 

 
