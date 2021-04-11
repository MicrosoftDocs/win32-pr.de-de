---
description: Im folgenden Beispiel wird ein Zugriffs Steuerungs Eintrag (ACE) zur freigegebenen Zugriffs Steuerungs Liste (DACL) eines-Objekts hinzugefügt.
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Ändern der ACLs eines Objekts in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21195b1164ce949d1305f0c1748d24b0dbb7525b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960536"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a><span data-ttu-id="7562d-103">Ändern der ACLs eines Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="7562d-103">Modifying the ACLs of an Object in C++</span></span>

<span data-ttu-id="7562d-104">Im folgenden Beispiel wird ein [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) zur freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) eines-Objekts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7562d-104">The following example adds an [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) to the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of an object.</span></span>

<span data-ttu-id="7562d-105">Der *AccessMode* -Parameter bestimmt den Typ des neuen ACE und die Kombination des neuen ACE mit allen vorhandenen ACEs für den angegebenen Vertrauens nehmer.</span><span class="sxs-lookup"><span data-stu-id="7562d-105">The *AccessMode* parameter determines the type of new ACE and how the new ACE is combined with any existing ACEs for the specified trustee.</span></span> <span data-ttu-id="7562d-106">Verwenden Sie \_ \_ im AccessMode-Parameter die Flags Zugriff gewähren, Zugriff festlegen, Zugriff verweigern \_ oder Zugriff widerrufen \_ . </span><span class="sxs-lookup"><span data-stu-id="7562d-106">Use the GRANT\_ACCESS, SET\_ACCESS, DENY\_ACCESS, or REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="7562d-107">Weitere Informationen zu diesen Flags finden Sie unter [**Zugriffs \_ Modus**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="7562d-107">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="7562d-108">Ein ähnlicher Code kann verwendet werden, um mit einer [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7562d-108">Similar code can be used to work with a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="7562d-109">Geben Sie SACL \_ \_ -Sicherheitsinformationen in den Funktionen " [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) " und " [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) " an, um die SACL für das Objekt zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7562d-109">Specify SACL\_SECURITY\_INFORMATION in the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) and [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions to get and set the SACL for the object.</span></span> <span data-ttu-id="7562d-110">Verwenden Sie \_ \_ \_ \_ im AccessMode-Parameter die Flags Audit Success, Set Audit Failure und \_ revoaccess. </span><span class="sxs-lookup"><span data-stu-id="7562d-110">Use the SET\_AUDIT\_SUCCESS, SET\_AUDIT\_FAILURE, and REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="7562d-111">Weitere Informationen zu diesen Flags finden Sie unter [**Zugriffs \_ Modus**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="7562d-111">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="7562d-112">Verwenden Sie diesen Code, um der DACL eines Verzeichnisdienst Objekts einen [Objekt spezifischen ACE](object-specific-aces.md) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7562d-112">Use this code to add an [object-specific ACE](object-specific-aces.md) to the DACL of a directory service object.</span></span> <span data-ttu-id="7562d-113">Um die GUIDs in einem Objekt spezifischen ACE anzugeben, legen Sie den " *Treuhänder* "-Parameter auf "Treuhänder is Objects" und "Name" oder "Treuhänder is Objects" und "sid" fest, \_ \_ \_ \_ \_ \_ \_ \_ und legen Sie für den *psztreuhänder* -Parameter einen Zeiger auf [**Objekte \_ und \_ Namen**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) oder [**Objekte und eine \_ \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="7562d-113">To specify the GUIDs in an object-specific ACE, set the *TrusteeForm* parameter to TRUSTEE\_IS\_OBJECTS\_AND\_NAME or TRUSTEE\_IS\_OBJECTS\_AND\_SID and set the *pszTrustee* parameter to be a pointer to an [**OBJECTS\_AND\_NAME**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) or [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure.</span></span>

<span data-ttu-id="7562d-114">In diesem Beispiel wird die [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) -Funktion verwendet, um die vorhandene DACL zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7562d-114">This example uses the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) function to get the existing DACL.</span></span> <span data-ttu-id="7562d-115">Anschließend füllt er eine [**explizite \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Struktur mit Informationen zu einem ACE und verwendet die [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) -Funktion, um den neuen ACE mit allen vorhandenen ACEs in der DACL zusammenzuführen.</span><span class="sxs-lookup"><span data-stu-id="7562d-115">Then it fills an [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure with information about an ACE and uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to merge the new ACE with any existing ACEs in the DACL.</span></span> <span data-ttu-id="7562d-116">Zum Schluss ruft das Beispiel die [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) -Funktion auf, um die neue DACL an die [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) des-Objekts anzufügen.</span><span class="sxs-lookup"><span data-stu-id="7562d-116">Finally, the example calls the [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) function to attach the new DACL to the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the object.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

DWORD AddAceToObjectsSecurityDescriptor (
    LPTSTR pszObjName,          // name of object
    SE_OBJECT_TYPE ObjectType,  // type of object
    LPTSTR pszTrustee,          // trustee for new ACE
    TRUSTEE_FORM TrusteeForm,   // format of trustee structure
    DWORD dwAccessRights,       // access mask for new ACE
    ACCESS_MODE AccessMode,     // type of ACE
    DWORD dwInheritance         // inheritance flags for new ACE
) 
{
    DWORD dwRes = 0;
    PACL pOldDACL = NULL, pNewDACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea;

    if (NULL == pszObjName) 
        return ERROR_INVALID_PARAMETER;

    // Get a pointer to the existing DACL.

    dwRes = GetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, &pOldDACL, NULL, &pSD);
    if (ERROR_SUCCESS != dwRes) {
        printf( "GetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Initialize an EXPLICIT_ACCESS structure for the new ACE. 

    ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
    ea.grfAccessPermissions = dwAccessRights;
    ea.grfAccessMode = AccessMode;
    ea.grfInheritance= dwInheritance;
    ea.Trustee.TrusteeForm = TrusteeForm;
    ea.Trustee.ptstrName = pszTrustee;

    // Create a new ACL that merges the new ACE
    // into the existing DACL.

    dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetEntriesInAcl Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Attach the new ACL as the object's DACL.

    dwRes = SetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, pNewDACL, NULL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    Cleanup:

        if(pSD != NULL) 
            LocalFree((HLOCAL) pSD); 
        if(pNewDACL != NULL) 
            LocalFree((HLOCAL) pNewDACL); 

        return dwRes;
}

```



 

 
