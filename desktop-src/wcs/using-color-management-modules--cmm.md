---
title: Verwenden von Farbverwaltungsmodulen (CMM)
description: Color Management Modules (CMMs) sind Module mit WCS-Code, die die Informationen in Geräteprofilen verwenden, um Farbkonvertierung und Farbzuordnung durchzuführen.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Windows Color System (WCS), Color Management Module (CMM)
- WCS (Windows Color System), Color Management Module (CMM)
- Bildfarbverwaltung, Farbverwaltungsmodul (CMM)
- Farbverwaltung, Farbverwaltungsmodul (CMM)
- Colors,Color Management Module (CMM)
- Color Management Module (CMM)
- CMM (Farbverwaltungsmodul)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b12a087bfc972ffcbd7f9fb083a9d73d669f134
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386899"
---
# <a name="using-color-management-modules-cmm"></a><span data-ttu-id="fd4fe-110">Verwenden von Farbverwaltungsmodulen (CMM)</span><span class="sxs-lookup"><span data-stu-id="fd4fe-110">Using Color Management Modules (CMM)</span></span>

<span data-ttu-id="fd4fe-111">Color Management Modules (CMMs) sind Module mit WCS-Code, die die Informationen in Geräteprofilen verwenden, um Farbkonvertierung und Farbzuordnung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-111">Color Management Modules (CMMs) are modules of WCS code that use the information in device profiles to perform color conversion and color mapping.</span></span> <span data-ttu-id="fd4fe-112">Anwendungsentwickler sollten keine CMMs implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-112">Application developers should not have to implement CMMs.</span></span> <span data-ttu-id="fd4fe-113">Microsoft stellt das Standard-CMM zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-113">Microsoft provides the default CMM.</span></span> <span data-ttu-id="fd4fe-114">Wenn Sie jedoch Software schreiben, die die Verwendung spezieller Farbkonvertierungs- und Farbzuordnungsalgorithmen erfordert, können Sie einen erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-114">However, if you do write software that requires the use of specialized color conversion and color mapping algorithms, you may create one.</span></span>

> [!Note]  
> <span data-ttu-id="fd4fe-115">CMM-Einstiegspunkte *sind keine* API-Funktionen und sollten nicht von Anwendungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-115">CMM entry points are *not* API functions and should not be called by applications.</span></span>

 

<span data-ttu-id="fd4fe-116">Wenn CMMs installiert sind, registriert das Installationsprogramm sie in der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-116">When CMMs are installed, the installation program registers them in the Windows registry.</span></span> <span data-ttu-id="fd4fe-117">Anwendungen können die registrierten CMMs auflisten und mithilfe der [**SelectCMM-Funktion eines**](/windows/win32/api/icm/nf-icm-selectcmm) auswählen.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-117">Applications can enumerate the registered CMMs and select one using the [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) function.</span></span> <span data-ttu-id="fd4fe-118">Die folgende Beispielanwendung veranschaulicht, wie sie alle registrierten CMMs aufzählt.</span><span class="sxs-lookup"><span data-stu-id="fd4fe-118">The following sample application demonstrates how to enumerate all registered CMMs.</span></span>


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &dwMaxName, &dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &cjCMM,NULL,&dwType,
                   chCMMFile,&cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 




