---
description: Durch das Aktivieren einer Berechtigung in einem Zugriffs Token kann der Prozess Aktionen auf Systemebene durchführen, die zuvor nicht möglich waren.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Aktivieren und Deaktivieren von Berechtigungen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050279"
---
# <a name="enabling-and-disabling-privileges-in-c"></a><span data-ttu-id="3d9b5-103">Aktivieren und Deaktivieren von Berechtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="3d9b5-103">Enabling and Disabling Privileges in C++</span></span>

<span data-ttu-id="3d9b5-104">Durch das Aktivieren einer Berechtigung in einem Zugriffs Token kann der Prozess Aktionen auf Systemebene durchführen, die zuvor nicht möglich waren.</span><span class="sxs-lookup"><span data-stu-id="3d9b5-104">Enabling a privilege in an access token allows the process to perform system-level actions that it could not previously.</span></span> <span data-ttu-id="3d9b5-105">Die Anwendung sollte gründlich überprüfen, ob die Berechtigung für den Kontotyp geeignet ist, insbesondere für die folgenden leistungsstarken Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="3d9b5-105">Your application should thoroughly verify that the privilege is appropriate to the type of account, especially for the following powerful privileges.</span></span>



| <span data-ttu-id="3d9b5-106">Berechtigungs Konstante</span><span class="sxs-lookup"><span data-stu-id="3d9b5-106">Privilege constant</span></span>           | <span data-ttu-id="3d9b5-107">Zeichenfolgenwert</span><span class="sxs-lookup"><span data-stu-id="3d9b5-107">String value</span></span>                  | <span data-ttu-id="3d9b5-108">`Display name`</span><span class="sxs-lookup"><span data-stu-id="3d9b5-108">Display name</span></span>                        |
|------------------------------|-------------------------------|-------------------------------------|
| <span data-ttu-id="3d9b5-109">Name des zugriffsdiensts "SE" \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d9b5-109">SE\_ASSIGNPRIMARYTOKEN\_NAME</span></span> | <span data-ttu-id="3d9b5-110">SeAssignPrimaryTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="3d9b5-110">SeAssignPrimaryTokenPrivilege</span></span> | <span data-ttu-id="3d9b5-111">Ersetzen eines Tokens auf Prozessebene</span><span class="sxs-lookup"><span data-stu-id="3d9b5-111">Replace a process-level token</span></span>       |
| <span data-ttu-id="3d9b5-112">Name der SE- \_ Sicherung \_</span><span class="sxs-lookup"><span data-stu-id="3d9b5-112">SE\_BACKUP\_NAME</span></span>             | <span data-ttu-id="3d9b5-113">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="3d9b5-113">SeBackupPrivilege</span></span>             | <span data-ttu-id="3d9b5-114">Sichern von Dateien und Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="3d9b5-114">Back up files and directories</span></span>       |
| <span data-ttu-id="3d9b5-115">SE \_ - \_ debugname</span><span class="sxs-lookup"><span data-stu-id="3d9b5-115">SE\_DEBUG\_NAME</span></span>              | <span data-ttu-id="3d9b5-116">SeDebugPrivilege</span><span class="sxs-lookup"><span data-stu-id="3d9b5-116">SeDebugPrivilege</span></span>              | <span data-ttu-id="3d9b5-117">Debuggen von Programmen</span><span class="sxs-lookup"><span data-stu-id="3d9b5-117">Debug programs</span></span>                      |
| <span data-ttu-id="3d9b5-118">\_ansteigende \_ Kontingent \_ Name für SE</span><span class="sxs-lookup"><span data-stu-id="3d9b5-118">SE\_INCREASE\_QUOTA\_NAME</span></span>    | <span data-ttu-id="3d9b5-119">SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="3d9b5-119">SeIncreaseQuotaPrivilege</span></span>      | <span data-ttu-id="3d9b5-120">Anpassen von Speicherkontingenten für einen Prozess</span><span class="sxs-lookup"><span data-stu-id="3d9b5-120">Adjust memory quotas for a process</span></span>  |
| <span data-ttu-id="3d9b5-121">SE \_ TCB- \_ Name</span><span class="sxs-lookup"><span data-stu-id="3d9b5-121">SE\_TCB\_NAME</span></span>                | <span data-ttu-id="3d9b5-122">SeTcbPrivilege</span><span class="sxs-lookup"><span data-stu-id="3d9b5-122">SeTcbPrivilege</span></span>                | <span data-ttu-id="3d9b5-123">Einsetzen als Teil des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="3d9b5-123">Act as part of the operating system</span></span> |



 

<span data-ttu-id="3d9b5-124">Bevor Sie diese potenziell gefährlichen Berechtigungen aktivieren, stellen Sie fest, dass Funktionen oder Vorgänge in Ihrem Code tatsächlich die Berechtigungen erfordern.</span><span class="sxs-lookup"><span data-stu-id="3d9b5-124">Before enabling any of these potentially dangerous privileges, determine that functions or operations in your code actually require the privileges.</span></span> <span data-ttu-id="3d9b5-125">So erfordern beispielsweise nur wenige Funktionen im Betriebssystem " **SeTcbPrivilege**".</span><span class="sxs-lookup"><span data-stu-id="3d9b5-125">For example, very few functions in the operating system actually require the **SeTcbPrivilege**.</span></span> <span data-ttu-id="3d9b5-126">Eine Liste aller verfügbaren Berechtigungen finden Sie unter [Berechtigungs Konstanten](authorization-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d9b5-126">For a list of all the available privileges, see [Privilege Constants](authorization-constants.md).</span></span>

<span data-ttu-id="3d9b5-127">Im folgenden Beispiel wird gezeigt, wie Sie eine Berechtigung in einem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3d9b5-127">The following example shows how to enable or disable a privilege in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="3d9b5-128">Im Beispiel wird die [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) -Funktion aufgerufen, um den [*lokal eindeutigen Bezeichner*](/windows/desktop/SecGloss/l-gly) (LUID) zu erhalten, den das lokale System zur Identifizierung der Berechtigung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d9b5-128">The example calls the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to get the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) that the local system uses to identify the privilege.</span></span> <span data-ttu-id="3d9b5-129">Im Beispiel wird die Funktion "- [**tokenprivilegien**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) " aufgerufen, die entweder die Berechtigung aktiviert oder deaktiviert, die vom Wert des Parameters " *benableprivilege* " abhängt.</span><span class="sxs-lookup"><span data-stu-id="3d9b5-129">Then the example calls the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function, which either enables or disables the privilege that depends on the value of the *bEnablePrivilege* parameter.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

