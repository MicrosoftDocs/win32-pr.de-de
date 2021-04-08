---
description: Windows unterstützt eine Reihe von Funktionen, die eine Zugriffs Steuerungs Liste (ACL) erstellen oder die Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in einer vorhandenen ACL ändern.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Erstellen oder Ändern einer ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0deb72bcd1a1c805dd8524027601952dda0eac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863247"
---
# <a name="creating-or-modifying-an-acl"></a>Erstellen oder Ändern einer ACL

Windows unterstützt eine Reihe von Funktionen, die eine [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/a-gly) (ACL) erstellen oder die [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs) in einer vorhandenen ACL ändern.

Die [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) -Funktion erstellt eine neue ACL. **SetEntriesInAcl** kann einen vollständig neuen Satz von ACEs für die ACL angeben, oder er kann einen oder mehrere neue ACEs mit den ACEs einer vorhandenen ACL zusammenführen. Die **SetEntriesInAcl** -Funktion verwendet ein Array von [**expliziten \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Strukturen, um die Informationen für die neuen ACEs anzugeben. Jede **explizite \_ Zugriffs** Struktur enthält Informationen, die einen einzelnen ACE beschreiben. Diese Informationen umfassen die Zugriffsrechte, den Typ des ACE, die Flags, die die ACE-Vererbung steuern, und eine [**Treuhänder**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) Struktur, die den Vertrauens nehmer identifiziert.

**So fügen Sie einer vorhandenen ACL einen neuen ACE hinzu**

1.  Verwenden Sie die Funktion [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) oder [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) , um die vorhandene DACL oder SACL aus der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts zu erhalten.
2.  Für jeden neuen ACE wird die [**buildexplicitaccesswithname**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) -Funktion aufgerufen, um eine [**explizite \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Struktur mit den Informationen auszufüllen, die den ACE beschreiben.
3.  Aufrufen von [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), wobei die vorhandene ACL und ein Array von [**expliziten \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Strukturen für die neuen ACEs angegeben werden. Die **SetEntriesInAcl** -Funktion ordnet die ACL und ihre ACEs zu und initialisiert sie.
4.  Aufrufen der Funktion [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) oder [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , um die neue ACL an die Sicherheits Beschreibung des Objekts anzufügen.

Wenn der Aufrufer eine vorhandene ACL angibt, führt [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) die neuen ACE-Informationen mit den vorhandenen ACEs in der ACL zusammen. Nehmen wir beispielsweise an, dass die vorhandene ACL Zugriff auf einen bestimmten Vertrauens nehmer gewährt und eine [**explizite \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Struktur dem gleichen Vertrauens nehmer den Zugriff verweigert. In diesem Fall fügt **SetEntriesInAcl** einen neuen ACE "Zugriff verweigert" für den Vertrauens nehmer hinzu und löscht oder ändert den vorhandenen Zugriffs zulässigen ACE für den Vertrauens nehmer.

Beispielcode, der einen neuen ACE in einer vorhandenen ACL zusammenfasst, finden Sie unter [Ändern der ACLs eines Objekts in C++](modifying-the-acls-of-an-object-in-c--.md).

 

 
