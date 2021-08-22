---
description: Zeigt, wie Sie eine DACL ordnungsgemäß erstellen.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Erstellen einer DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af1c7c43c24c07d3d301642b93db41496f2ff70742ce8e2e95fd3f7364ad765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516050"
---
# <a name="creating-a-dacl"></a>Erstellen einer DACL

Das Erstellen einer [*geeigneten daktiven Zugriffssteuerungsliste (Discretionary Access Control List,*](/windows/desktop/SecGloss/d-gly) DACL) ist ein notwendiger und wichtiger Bestandteil der Anwendungsentwicklung. Da eine **NULL-DACL** allen Arten von Zugriff für alle Benutzer zulässt, verwenden Sie keine **NULL-DACLs.**

Das folgende Beispiel zeigt, wie Sie eine DACL ordnungsgemäß erstellen. Das Beispiel enthält die Funktion CreateMyDACL, die die [Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language,](/windows/desktop/SecAuthZ/security-descriptor-definition-language) SDDL) verwendet, um die gewährte und verweigerte Zugriffssteuerung in einer DACL zu definieren. Um anderen Zugriff auf die Objekte Ihrer Anwendung bereitzustellen, ändern Sie die CreateMyDACL-Funktion nach Bedarf.

Im Beispiel:

1.  Die main-Funktion übergibt eine Adresse einer [**SECURITY \_ ATTRIBUTES-Struktur**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) an die CreateMyDACL-Funktion.
2.  Die CreateMyDACL-Funktion verwendet SDDL-Zeichenfolgen für Folgendes:
    -   Verweigern sie den Zugriff auf Gastbenutzer und anonyme Anmeldebenutzer.
    -   Ermöglicht den Lese-/Schreib-/Ausführungszugriff für authentifizierte Benutzer.
    -   Gestatten Sie Administratoren die vollständige Kontrolle.

    Weitere Informationen zu den SDDL-Zeichenfolgenformaten finden Sie unter [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  Die CreateMyDACL-Funktion ruft die [**ConvertStringSecurityDescriptorToSecurityDescriptor-Funktion**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) auf, um die SDDL-Zeichenfolgen in einen [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly)zu konvertieren. Auf den Sicherheitsdeskriptor verweist der **lpSecurityDescriptor-Member** der [**SECURITY \_ ATTRIBUTES-Struktur.**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) CreateMyDACL sendet den Rückgabewert von **ConvertStringSecurityDescriptorToSecurityDescriptor** an die Main-Funktion.
4.  Die Main-Funktion verwendet die aktualisierte [**SECURITY \_ ATTRIBUTES-Struktur,**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) um die DACL für einen neuen Ordner anzugeben, der von der [**CreateDirectory-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) erstellt wird.
5.  Wenn die Main-Funktion mit der [**SECURITY \_ ATTRIBUTES-Struktur**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) fertig ist, gibt die Main-Funktion den für den **lpSecurityDescriptor-Member** belegten Arbeitsspeicher frei, indem sie die [**LocalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-localfree) aufruft.

> [!Note]  
> Zum erfolgreichen Kompilieren von SDDL-Funktionen wie [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)müssen Sie die \_ WIN32 \_ WINNT-Konstante als 0x0500 oder höher definieren.

 


```C++
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <sddl.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

BOOL CreateMyDACL(SECURITY_ATTRIBUTES *);

void main()
{
     SECURITY_ATTRIBUTES  sa;
      
     sa.nLength = sizeof(SECURITY_ATTRIBUTES);
     sa.bInheritHandle = FALSE;  

     // Call function to set the DACL. The DACL
     // is set in the SECURITY_ATTRIBUTES 
     // lpSecurityDescriptor member.
     if (!CreateMyDACL(&sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateMyDACL\n");
         exit(1);
     }

     // Use the updated SECURITY_ATTRIBUTES to specify
     // security attributes for securable objects.
     // This example uses security attributes during
     // creation of a new directory.
     if (0 == CreateDirectory(TEXT("C:\\MyFolder"), &sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateDirectory\n");
         exit(1);
     }

     // Free the memory allocated for the SECURITY_DESCRIPTOR.
     if (NULL != LocalFree(sa.lpSecurityDescriptor))
     {
         // Error encountered; generate message and exit.
         printf("Failed LocalFree\n");
         exit(1);
     }
}


// CreateMyDACL.
//    Create a security descriptor that contains the DACL 
//    you want.
//    This function uses SDDL to make Deny and Allow ACEs.
//
// Parameter:
//    SECURITY_ATTRIBUTES * pSA
//    Pointer to a SECURITY_ATTRIBUTES structure. It is your
//    responsibility to properly initialize the 
//    structure and to free the structure's 
//    lpSecurityDescriptor member when you have
//    finished using it. To free the structure's 
//    lpSecurityDescriptor member, call the 
//    LocalFree function.
// 
// Return value:
//    FALSE if the address to the structure is NULL. 
//    Otherwise, this function returns the value from the
//    ConvertStringSecurityDescriptorToSecurityDescriptor 
//    function.
BOOL CreateMyDACL(SECURITY_ATTRIBUTES * pSA)
{
     // Define the SDDL for the DACL. This example sets 
     // the following access:
     //     Built-in guests are denied all access.
     //     Anonymous logon is denied all access.
     //     Authenticated users are allowed 
     //     read/write/execute access.
     //     Administrators are allowed full control.
     // Modify these values as needed to generate the proper
     // DACL for your application. 
     TCHAR * szSD = TEXT("D:")       // Discretionary ACL
        TEXT("(D;OICI;GA;;;BG)")     // Deny access to 
                                     // built-in guests
        TEXT("(D;OICI;GA;;;AN)")     // Deny access to 
                                     // anonymous logon
        TEXT("(A;OICI;GRGWGX;;;AU)") // Allow 
                                     // read/write/execute 
                                     // to authenticated 
                                     // users
        TEXT("(A;OICI;GA;;;BA)");    // Allow full control 
                                     // to administrators

    if (NULL == pSA)
        return FALSE;

     return ConvertStringSecurityDescriptorToSecurityDescriptor(
                szSD,
                SDDL_REVISION_1,
                &(pSA->lpSecurityDescriptor),
                NULL);
}
```



 

 
