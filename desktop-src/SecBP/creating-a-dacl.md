---
description: Zeigt, wie eine DACL ordnungsgemäß erstellt wird.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Erstellen einer DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf8213f6fbb4e2a885655b47437ec464337ea13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868219"
---
# <a name="creating-a-dacl"></a>Erstellen einer DACL

Das Erstellen einer ordnungsgemäßen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) ist ein erforderlicher und wichtiger Bestandteil der Anwendungsentwicklung. Da eine **null** -DACL alle Zugriffs Typen für alle Benutzer zulässt, dürfen keine **null** -DACLs verwendet werden.

Im folgenden Beispiel wird gezeigt, wie eine DACL ordnungsgemäß erstellt wird. Das Beispiel enthält die Funktion "kreatemydacl", die die [Sicherheits Deskriptor-Definitions Sprache (Security Deskriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) , SDDL) zum Definieren der gewährten und verweigerten Zugriffs Steuerung in einer DACL verwendet. Um unterschiedliche Zugriffsrechte für die Objekte Ihrer Anwendung bereitzustellen, ändern Sie die Funktion "fiatemydacl" nach Bedarf.

Im Beispiel:

1.  Die Main-Funktion übergibt eine Adresse einer [**Sicherheits \_ Attribut**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) Struktur an die Funktion "anatemydacl".
2.  Die Funktion "| atemydacl" verwendet SDDL-Zeichen folgen für Folgendes:
    -   Verweigern Sie den Zugriff auf Gastbenutzer und anonyme Anmelde Benutzer.
    -   Lese-/Schreibzugriff/Ausführungs Zugriff auf authentifizierte Benutzer zulassen.
    -   Ermöglicht die vollständige Kontrolle für Administratoren.

    Weitere Informationen zu den SDDL-Zeichen folgen Formaten finden Sie unter [Format der Sicherheits Deskriptorzeichenfolge](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  Die Funktion "anatemydacl" Ruft die [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) -Funktion auf, um die SDDL-Zeichen folgen in eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)zu konvertieren. Der Sicherheits Deskriptor verweist auf den **lpsecuritydescriptor** -Member der Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . "Anatemydacl" sendet den Rückgabewert von **convertstringsecuritydescriptortosecuritydescriptor** an die Main-Funktion.
4.  Die Main-Funktion verwendet die aktualisierte Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , um die DACL für einen neuen Ordner anzugeben, der von der Funktion "| [**atedirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) " erstellt wird.
5.  Wenn die Main-Funktion die Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) verwendet, gibt die Main-Funktion den für den **lpsecuritydescriptor** -Member zugeordneten Arbeitsspeicher frei, indem die [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) -Funktion aufgerufen wird.

> [!Note]  
> Um SDDL-Funktionen (z. [**b. convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)) erfolgreich zu kompilieren, müssen Sie die \_ Win32- \_ Winnt-Konstante als 0x0500 sein oder höher definieren.

 


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



 

 
