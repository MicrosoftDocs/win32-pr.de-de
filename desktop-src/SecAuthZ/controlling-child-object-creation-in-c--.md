---
description: Sie können die DACL eines Container Objekts verwenden, um zu steuern, wer die Möglichkeit hat, untergeordnete Objekte im Container zu erstellen.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Steuern der Erstellung von untergeordneten Objekten in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527638"
---
# <a name="controlling-child-object-creation-in-c"></a>Steuern der Erstellung von untergeordneten Objekten in C++

Sie können die DACL eines Container Objekts verwenden, um zu steuern, wer die Möglichkeit hat, untergeordnete Objekte im Container zu erstellen. Dies kann wichtig sein, da der Ersteller eines Objekts in der Regel als Besitzer des Objekts zugewiesen wird und der Besitzer eines Objekts den Zugriff auf das Objekt steuern kann.

Die verschiedenen Typen von Container Objekten verfügen über bestimmte Zugriffsrechte, die die Fähigkeit zum Erstellen untergeordneter Objekte steuern. Beispielsweise muss ein Thread Key \_ Create \_ Sub Key- \_ Zugriff auf einen Registrierungsschlüssel aufweisen, um unter dem Schlüssel einen Unterschlüssel zu erstellen. Die DACL eines Registrierungsschlüssels kann ACEs enthalten, die dieses Zugriffsrecht zulassen oder verweigern. Ebenso unterstützt NTFS die Datei \_ Add \_ -Datei und die Datei \_ Add \_ subdirectory-Zugriffsrechte, um die Fähigkeit zum Erstellen von Dateien oder Verzeichnissen in einem Verzeichnis zu steuern.

Die ADS \_ right \_ DS \_ Create \_ Child Access Right steuert die Erstellung von untergeordneten Objekten in einem Verzeichnisdienst Objekt (DS). DS-Objekte können jedoch unterschiedliche Objekttypen enthalten, sodass das System eine präzisere Granularität der Steuerelemente unterstützt. Mithilfe [Objekt spezifischer ACEs](object-specific-aces.md) können Sie das Recht zum Erstellen eines angegebenen Typs untergeordneter Objekte zulassen oder verweigern. Sie können es Benutzern ermöglichen, einen Typ von untergeordneten Objekten zu erstellen, während Sie verhindern, dass der Benutzer andere Typen von untergeordneten Objekten erstellt.

Im folgenden Beispiel wird die [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) -Funktion verwendet, um einen Objekt spezifischen ACE zu einer ACL hinzuzufügen. Der ACE erteilt die Berechtigung zum Erstellen eines angegebenen Typs von untergeordnetem Objekt. Der **grfakcesspermissions** -Member der [**expliziten \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Struktur ist auf ADS \_ right \_ DS \_ Create \_ Child festgelegt, um anzugeben, dass der ACE die Erstellung des untergeordneten Objekts steuert. Der **objectspree sent** -Member der [**Objekte \_ und der \_ sid-**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) Struktur ist auf den ACE- \_ \_ Objekttyp vorhanden festgelegt \_ , um anzugeben, dass der **objecttypguid** -Member eine gültige GUID enthält. Der GUID identifiziert einen Typ von untergeordnetem Objekt, dessen Erstellung gesteuert wird.

Im folgenden Beispiel muss polddacl ein gültiger Zeiger auf eine vorhandene [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) -Struktur sein. Informationen dazu, wie Sie eine **ACL** -Struktur für ein Objekt erstellen, finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).


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



 

 



