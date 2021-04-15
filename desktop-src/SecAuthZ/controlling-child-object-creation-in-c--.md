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
# <a name="controlling-child-object-creation-in-c"></a><span data-ttu-id="23ab0-103">Steuern der Erstellung von untergeordneten Objekten in C++</span><span class="sxs-lookup"><span data-stu-id="23ab0-103">Controlling Child Object Creation in C++</span></span>

<span data-ttu-id="23ab0-104">Sie können die DACL eines Container Objekts verwenden, um zu steuern, wer die Möglichkeit hat, untergeordnete Objekte im Container zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23ab0-104">You can use the DACL of a container object to control who is allowed to create child objects within the container.</span></span> <span data-ttu-id="23ab0-105">Dies kann wichtig sein, da der Ersteller eines Objekts in der Regel als Besitzer des Objekts zugewiesen wird und der Besitzer eines Objekts den Zugriff auf das Objekt steuern kann.</span><span class="sxs-lookup"><span data-stu-id="23ab0-105">This can be important because the creator of an object is typically assigned as the object's owner, and an object's owner can control access to the object.</span></span>

<span data-ttu-id="23ab0-106">Die verschiedenen Typen von Container Objekten verfügen über bestimmte Zugriffsrechte, die die Fähigkeit zum Erstellen untergeordneter Objekte steuern.</span><span class="sxs-lookup"><span data-stu-id="23ab0-106">The various types of container objects have specific access rights that control the ability to create child objects.</span></span> <span data-ttu-id="23ab0-107">Beispielsweise muss ein Thread Key \_ Create \_ Sub Key- \_ Zugriff auf einen Registrierungsschlüssel aufweisen, um unter dem Schlüssel einen Unterschlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23ab0-107">For example, a thread must have KEY\_CREATE\_SUB\_KEY access to a registry key to create a subkey under the key.</span></span> <span data-ttu-id="23ab0-108">Die DACL eines Registrierungsschlüssels kann ACEs enthalten, die dieses Zugriffsrecht zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="23ab0-108">The DACL of a registry key can contain ACEs that allow or deny this access right.</span></span> <span data-ttu-id="23ab0-109">Ebenso unterstützt NTFS die Datei \_ Add \_ -Datei und die Datei \_ Add \_ subdirectory-Zugriffsrechte, um die Fähigkeit zum Erstellen von Dateien oder Verzeichnissen in einem Verzeichnis zu steuern.</span><span class="sxs-lookup"><span data-stu-id="23ab0-109">Similarly, NTFS supports the FILE\_ADD\_FILE and FILE\_ADD\_SUBDIRECTORY access rights for controlling the ability to create files or directories in a directory.</span></span>

<span data-ttu-id="23ab0-110">Die ADS \_ right \_ DS \_ Create \_ Child Access Right steuert die Erstellung von untergeordneten Objekten in einem Verzeichnisdienst Objekt (DS).</span><span class="sxs-lookup"><span data-stu-id="23ab0-110">The ADS\_RIGHT\_DS\_CREATE\_CHILD access right controls the creation of child objects in a directory service (DS) object.</span></span> <span data-ttu-id="23ab0-111">DS-Objekte können jedoch unterschiedliche Objekttypen enthalten, sodass das System eine präzisere Granularität der Steuerelemente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23ab0-111">However, DS objects can contain different types of objects, so the system supports a finer granularity of control.</span></span> <span data-ttu-id="23ab0-112">Mithilfe [Objekt spezifischer ACEs](object-specific-aces.md) können Sie das Recht zum Erstellen eines angegebenen Typs untergeordneter Objekte zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="23ab0-112">You can use [object-specific ACEs](object-specific-aces.md) to allow or deny the right to create a specified type of child object.</span></span> <span data-ttu-id="23ab0-113">Sie können es Benutzern ermöglichen, einen Typ von untergeordneten Objekten zu erstellen, während Sie verhindern, dass der Benutzer andere Typen von untergeordneten Objekten erstellt.</span><span class="sxs-lookup"><span data-stu-id="23ab0-113">You can allow a user to create one type of child object while preventing the user from creating other types of child objects.</span></span>

<span data-ttu-id="23ab0-114">Im folgenden Beispiel wird die [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) -Funktion verwendet, um einen Objekt spezifischen ACE zu einer ACL hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="23ab0-114">The following example uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to add an object-specific ACE to an ACL.</span></span> <span data-ttu-id="23ab0-115">Der ACE erteilt die Berechtigung zum Erstellen eines angegebenen Typs von untergeordnetem Objekt.</span><span class="sxs-lookup"><span data-stu-id="23ab0-115">The ACE grants permission to create a specified type of child object.</span></span> <span data-ttu-id="23ab0-116">Der **grfakcesspermissions** -Member der [**expliziten \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Struktur ist auf ADS \_ right \_ DS \_ Create \_ Child festgelegt, um anzugeben, dass der ACE die Erstellung des untergeordneten Objekts steuert.</span><span class="sxs-lookup"><span data-stu-id="23ab0-116">The **grfAccessPermissions** member of the [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure is set to ADS\_RIGHT\_DS\_CREATE\_CHILD to indicate that the ACE controls the child object creation.</span></span> <span data-ttu-id="23ab0-117">Der **objectspree sent** -Member der [**Objekte \_ und der \_ sid-**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) Struktur ist auf den ACE- \_ \_ Objekttyp vorhanden festgelegt \_ , um anzugeben, dass der **objecttypguid** -Member eine gültige GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="23ab0-117">The **ObjectsPresent** member of the [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure is set to ACE\_OBJECT\_TYPE\_PRESENT to indicate that the **ObjectTypeGuid** member contains a valid GUID.</span></span> <span data-ttu-id="23ab0-118">Der GUID identifiziert einen Typ von untergeordnetem Objekt, dessen Erstellung gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="23ab0-118">The GUID identifies a type of child object whose creation is being controlled.</span></span>

<span data-ttu-id="23ab0-119">Im folgenden Beispiel muss polddacl ein gültiger Zeiger auf eine vorhandene [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) -Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="23ab0-119">In the following example, pOldDACL must be a valid pointer to an existing [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) structure.</span></span> <span data-ttu-id="23ab0-120">Informationen dazu, wie Sie eine **ACL** -Struktur für ein Objekt erstellen, finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="23ab0-120">For information about how to create an **ACL** structure for an object, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>


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



 

 



