---
description: Im folgenden Beispiel wird der DACL (Discretionary Access Control List) eines Objekts ein Zugriffssteuerungseintrag (ACE) hinzugefügt.
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Ändern der ACLs eines Objekts in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42681a22e6b5f4b478d55d21f9b0b71dbe3f9c081ef5d18ba3da7a33f8709d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912460"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a>Ändern der ACLs eines Objekts in C++

Im folgenden Beispiel wird der [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) eines Objekts ein [*Zugriffssteuerungseintrag*](/windows/desktop/SecGloss/a-gly) (ACE) hinzugefügt.

Der *AccessMode-Parameter* bestimmt den Typ des neuen ACE und wie der neue ACE mit vorhandenen ACEs für den angegebenen Vertrauensnehmer kombiniert wird. Verwenden Sie die Flags GRANT \_ ACCESS, SET \_ ACCESS, DENY \_ ACCESS oder REVOKE ACCESS im \_ *AccessMode-Parameter.* Informationen zu diesen Flags finden Sie unter [**ACCESS \_ MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Ähnlicher Code kann verwendet werden, um mit einer [*Systemzugriffssteuerungsliste*](/windows/desktop/SecGloss/s-gly) (SACL) zu arbeiten. Geben Sie SACL \_ SECURITY INFORMATION in den Funktionen \_ [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) und [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) an, um die SACL für das Objekt abzurufen und festzulegen. Verwenden Sie die Flags SET \_ AUDIT \_ SUCCESS, SET AUDIT \_ FAILURE und REVOKE ACCESS im \_ \_ *AccessMode-Parameter.* Informationen zu diesen Flags finden Sie unter [**ACCESS \_ MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Verwenden Sie diesen Code, um der DACL eines Verzeichnisdienstobjekts einen [objektspezifischen ACE](object-specific-aces.md) hinzuzufügen. Um die GUIDs in einem objektspezifischen ACE anzugeben, legen Sie den *Parameter TrusteeForm* auf TRUST \_ IS OBJECTS AND NAME oder TRUST IS OBJECTS AND SID \_ \_ \_ \_ \_ \_ \_ fest, und legen Sie den *PszTrustee-Parameter* als Zeiger auf eine [**OBJECTS AND \_ \_ NAME-**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) oder [**OBJECTS AND \_ \_ SID-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) fest.

In diesem Beispiel wird die [**GetNamedSecurityInfo-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) verwendet, um die vorhandene DACL abzurufen. Anschließend füllt sie eine [**EXPLICIT \_ ACCESS-Struktur**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) mit Informationen zu einem ACE und verwendet die [**SetEntriesInAcl-Funktion,**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) um den neuen ACE mit allen vorhandenen ACEs in der DACL zusammenzuführen. Schließlich ruft das Beispiel die [**SetNamedSecurityInfo-Funktion**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) auf, um die neue DACL an den [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly) des Objekts anzufügen.


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



 

 
