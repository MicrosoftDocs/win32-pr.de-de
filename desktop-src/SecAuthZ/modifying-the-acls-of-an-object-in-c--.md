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
# <a name="modifying-the-acls-of-an-object-in-c"></a>Ändern der ACLs eines Objekts in C++

Im folgenden Beispiel wird ein [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) zur freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) eines-Objekts hinzugefügt.

Der *AccessMode* -Parameter bestimmt den Typ des neuen ACE und die Kombination des neuen ACE mit allen vorhandenen ACEs für den angegebenen Vertrauens nehmer. Verwenden Sie \_ \_ im AccessMode-Parameter die Flags Zugriff gewähren, Zugriff festlegen, Zugriff verweigern \_ oder Zugriff widerrufen \_ .  Weitere Informationen zu diesen Flags finden Sie unter [**Zugriffs \_ Modus**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Ein ähnlicher Code kann verwendet werden, um mit einer [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) zu arbeiten. Geben Sie SACL \_ \_ -Sicherheitsinformationen in den Funktionen " [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) " und " [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) " an, um die SACL für das Objekt zu erhalten und festzulegen. Verwenden Sie \_ \_ \_ \_ im AccessMode-Parameter die Flags Audit Success, Set Audit Failure und \_ revoaccess.  Weitere Informationen zu diesen Flags finden Sie unter [**Zugriffs \_ Modus**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Verwenden Sie diesen Code, um der DACL eines Verzeichnisdienst Objekts einen [Objekt spezifischen ACE](object-specific-aces.md) hinzuzufügen. Um die GUIDs in einem Objekt spezifischen ACE anzugeben, legen Sie den " *Treuhänder* "-Parameter auf "Treuhänder is Objects" und "Name" oder "Treuhänder is Objects" und "sid" fest, \_ \_ \_ \_ \_ \_ \_ \_ und legen Sie für den *psztreuhänder* -Parameter einen Zeiger auf [**Objekte \_ und \_ Namen**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) oder [**Objekte und eine \_ \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) -Struktur fest.

In diesem Beispiel wird die [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) -Funktion verwendet, um die vorhandene DACL zu erhalten. Anschließend füllt er eine [**explizite \_ Zugriffs**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) Struktur mit Informationen zu einem ACE und verwendet die [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) -Funktion, um den neuen ACE mit allen vorhandenen ACEs in der DACL zusammenzuführen. Zum Schluss ruft das Beispiel die [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) -Funktion auf, um die neue DACL an die [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) des-Objekts anzufügen.


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



 

 
