---
description: Sie können die DACL eines Containerobjekts verwenden, um zu steuern, wer untergeordnete Objekte innerhalb des Containers erstellen darf.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Steuern der Erstellung untergeordneter Objekte in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2820f6d1bd9aae335e018e15b3b298b5b907f51a47d78e517b8ad798d0aba442
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782715"
---
# <a name="controlling-child-object-creation-in-c"></a>Steuern der Erstellung untergeordneter Objekte in C++

Sie können die DACL eines Containerobjekts verwenden, um zu steuern, wer untergeordnete Objekte innerhalb des Containers erstellen darf. Dies kann wichtig sein, da der Ersteller eines Objekts in der Regel als Besitzer des Objekts zugewiesen wird und der Besitzer eines Objekts den Zugriff auf das Objekt steuern kann.

Die verschiedenen Typen von Containerobjekten verfügen über bestimmte Zugriffsrechte, die die Fähigkeit zum Erstellen von untergeordneten Objekten steuern. Beispielsweise muss ein Thread über KEY CREATE SUB KEY-Zugriff auf einen Registrierungsschlüssel verfügen, um einen Unterschlüssel unter \_ dem Schlüssel zu \_ \_ erstellen. Die DACL eines Registrierungsschlüssels kann ACEs enthalten, die dieses Zugriffsrecht zulassen oder verweigern. Ebenso unterstützt NTFS die Zugriffsrechte FILE ADD FILE und \_ \_ FILE ADD SUBDIRECTORY, um die Möglichkeit zum Erstellen von Dateien oder \_ \_ Verzeichnissen in einem Verzeichnis zu steuern.

Das ZUGRIFFsrecht ADS RIGHT DS CREATE CHILD steuert die Erstellung untergeordneter Objekte in einem \_ \_ \_ \_ Verzeichnisdienstobjekt (Directory Service, DS). DS-Objekte können jedoch unterschiedliche Objekttypen enthalten, sodass das System eine präzisere Steuerung unterstützt. Sie können [objektspezifische ACEs](object-specific-aces.md) verwenden, um das Recht zum Erstellen eines angegebenen Untergeordneten Objekttyps zu erlauben oder zu verweigern. Sie können es einem Benutzer ermöglichen, einen untergeordneten Objekttyp zu erstellen, während Sie gleichzeitig verhindern, dass der Benutzer andere Typen von untergeordneten Objekten erstellt.

Im folgenden Beispiel wird die [**SetEntriesInAcl-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) verwendet, um einer ACL einen objektspezifischen ACE hinzuzufügen. Der ACE erteilt die Berechtigung zum Erstellen eines angegebenen Untergeordneten Objekttyps. Das **grfAccessPermissions-Member** der [**EXPLICIT \_ ACCESS-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) ist auf ADS RIGHT DS CREATE CHILD festgelegt, um anzugeben, dass der ACE die Erstellung des untergeordneten \_ Objekts \_ \_ \_ steuert. Der **ObjectsPresent-Member** der [**OBJECTS AND \_ \_ SID-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) wird auf ACE OBJECT TYPE PRESENT festgelegt, um anzugeben, dass der \_ \_ \_ **ObjectTypeGuid-Member** eine gültige GUID enthält. Die GUID identifiziert einen Typ von untergeordnetem Objekt, dessen Erstellung gesteuert wird.

Im folgenden Beispiel muss pOldDACL ein gültiger Zeiger auf eine vorhandene [**ACL-Struktur**](/windows/desktop/api/Winnt/ns-winnt-acl) sein. Informationen zum Erstellen einer **ACL-Struktur** für ein Objekt finden Sie unter [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)(Erstellen eines Sicherheitsdeskriptors für ein neues Objekt in C++).


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 



