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
# <a name="creating-a-dacl"></a><span data-ttu-id="e195e-103">Erstellen einer DACL</span><span class="sxs-lookup"><span data-stu-id="e195e-103">Creating a DACL</span></span>

<span data-ttu-id="e195e-104">Das Erstellen einer ordnungsgemäßen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) ist ein erforderlicher und wichtiger Bestandteil der Anwendungsentwicklung.</span><span class="sxs-lookup"><span data-stu-id="e195e-104">Creating a proper [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) is a necessary and important part of application development.</span></span> <span data-ttu-id="e195e-105">Da eine **null** -DACL alle Zugriffs Typen für alle Benutzer zulässt, dürfen keine **null** -DACLs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e195e-105">Because a **NULL** DACL permits all types of access to all users, do not use **NULL** DACLs.</span></span>

<span data-ttu-id="e195e-106">Im folgenden Beispiel wird gezeigt, wie eine DACL ordnungsgemäß erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e195e-106">The following example shows how to properly create a DACL.</span></span> <span data-ttu-id="e195e-107">Das Beispiel enthält die Funktion "kreatemydacl", die die [Sicherheits Deskriptor-Definitions Sprache (Security Deskriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) , SDDL) zum Definieren der gewährten und verweigerten Zugriffs Steuerung in einer DACL verwendet.</span><span class="sxs-lookup"><span data-stu-id="e195e-107">The example contains a function, CreateMyDACL, that uses the [security descriptor definition language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) to define the granted and denied access control in a DACL.</span></span> <span data-ttu-id="e195e-108">Um unterschiedliche Zugriffsrechte für die Objekte Ihrer Anwendung bereitzustellen, ändern Sie die Funktion "fiatemydacl" nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="e195e-108">To provide different access for your application's objects, modify the CreateMyDACL function as needed.</span></span>

<span data-ttu-id="e195e-109">Im Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e195e-109">In the example:</span></span>

1.  <span data-ttu-id="e195e-110">Die Main-Funktion übergibt eine Adresse einer [**Sicherheits \_ Attribut**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) Struktur an die Funktion "anatemydacl".</span><span class="sxs-lookup"><span data-stu-id="e195e-110">The main function passes an address of a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to the CreateMyDACL function.</span></span>
2.  <span data-ttu-id="e195e-111">Die Funktion "| atemydacl" verwendet SDDL-Zeichen folgen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e195e-111">The CreateMyDACL function uses SDDL strings to:</span></span>
    -   <span data-ttu-id="e195e-112">Verweigern Sie den Zugriff auf Gastbenutzer und anonyme Anmelde Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e195e-112">Deny access to guest and anonymous logon users.</span></span>
    -   <span data-ttu-id="e195e-113">Lese-/Schreibzugriff/Ausführungs Zugriff auf authentifizierte Benutzer zulassen.</span><span class="sxs-lookup"><span data-stu-id="e195e-113">Allow read/write/execute access to authenticated users.</span></span>
    -   <span data-ttu-id="e195e-114">Ermöglicht die vollständige Kontrolle für Administratoren.</span><span class="sxs-lookup"><span data-stu-id="e195e-114">Allow full control to administrators.</span></span>

    <span data-ttu-id="e195e-115">Weitere Informationen zu den SDDL-Zeichen folgen Formaten finden Sie unter [Format der Sicherheits Deskriptorzeichenfolge](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="e195e-115">For more information about the SDDL string formats, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>
3.  <span data-ttu-id="e195e-116">Die Funktion "anatemydacl" Ruft die [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) -Funktion auf, um die SDDL-Zeichen folgen in eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e195e-116">The CreateMyDACL function calls the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL strings to a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="e195e-117">Der Sicherheits Deskriptor verweist auf den **lpsecuritydescriptor** -Member der Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e195e-117">The security descriptor is pointed to by the **lpSecurityDescriptor** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="e195e-118">"Anatemydacl" sendet den Rückgabewert von **convertstringsecuritydescriptortosecuritydescriptor** an die Main-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e195e-118">CreateMyDACL sends the return value from **ConvertStringSecurityDescriptorToSecurityDescriptor** to the main function.</span></span>
4.  <span data-ttu-id="e195e-119">Die Main-Funktion verwendet die aktualisierte Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , um die DACL für einen neuen Ordner anzugeben, der von der Funktion "| [**atedirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) " erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e195e-119">The main function uses the updated [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to specify the DACL for a new folder that is created by the [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) function.</span></span>
5.  <span data-ttu-id="e195e-120">Wenn die Main-Funktion die Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) verwendet, gibt die Main-Funktion den für den **lpsecuritydescriptor** -Member zugeordneten Arbeitsspeicher frei, indem die [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e195e-120">When the main function is finished using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure, the main function frees the memory allocated for the **lpSecurityDescriptor** member by calling the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="e195e-121">Um SDDL-Funktionen (z. [**b. convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)) erfolgreich zu kompilieren, müssen Sie die \_ Win32- \_ Winnt-Konstante als 0x0500 sein oder höher definieren.</span><span class="sxs-lookup"><span data-stu-id="e195e-121">To successfully compile SDDL functions such as [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), you must define the \_WIN32\_WINNT constant as 0x0500 or greater.</span></span>

 


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



 

 
