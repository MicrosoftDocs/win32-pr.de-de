---
title: Verwenden von Farbverwaltungsmodulen (CMM)
description: Farb Verwaltungs Module (Color Management modules, CMMS) sind Module von WCS-Code, die die Informationen in Geräte Profilen zum Durchführen der Farbkonvertierung und der Farbzuordnung verwenden.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Windows Color System (WCS), Farb Verwaltungsmodul (CMM)
- WCS (Windows Color System), Farb Verwaltungsmodul (CMM)
- Bild Farbverwaltung, Farb Verwaltungsmodul (CMM)
- Farbverwaltung, Farb Verwaltungsmodul (CMM)
- Farben, Farb Verwaltungsmodul (CMM)
- Farb Verwaltungsmodul (CMM)
- CMM (Farb Verwaltungsmodul)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518558305639f0699358f22fb3544698741cfedf
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "106351182"
---
# <a name="using-color-management-modules-cmm"></a><span data-ttu-id="29718-110">Verwenden von Farbverwaltungsmodulen (CMM)</span><span class="sxs-lookup"><span data-stu-id="29718-110">Using Color Management Modules (CMM)</span></span>

<span data-ttu-id="29718-111">Farb Verwaltungs Module (Color Management modules, CMMS) sind Module von WCS-Code, die die Informationen in Geräte Profilen zum Durchführen der Farbkonvertierung und der Farbzuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="29718-111">Color Management Modules (CMMs) are modules of WCS code that use the information in device profiles to perform color conversion and color mapping.</span></span> <span data-ttu-id="29718-112">Anwendungsentwickler sollten CMMS nicht implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="29718-112">Application developers should not have to implement CMMs.</span></span> <span data-ttu-id="29718-113">Microsoft stellt den Standard-CMM bereit.</span><span class="sxs-lookup"><span data-stu-id="29718-113">Microsoft provides the default CMM.</span></span> <span data-ttu-id="29718-114">Wenn Sie jedoch Software schreiben, für die die Verwendung spezieller Algorithmen zur Farbkonvertierung und Farbzuordnung erforderlich ist, können Sie eine erstellen.</span><span class="sxs-lookup"><span data-stu-id="29718-114">However, if you do write software that requires the use of specialized color conversion and color mapping algorithms, you may create one.</span></span>

> [!Note]  
> <span data-ttu-id="29718-115">CMM-Einstiegspunkte sind *keine* API-Funktionen und sollten nicht von Anwendungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="29718-115">CMM entry points are *not* API functions and should not be called by applications.</span></span>

 

<span data-ttu-id="29718-116">Wenn CMMS installiert sind, werden Sie vom Installationsprogramm in der Windows-Registrierung registriert.</span><span class="sxs-lookup"><span data-stu-id="29718-116">When CMMs are installed, the installation program registers them in the Windows registry.</span></span> <span data-ttu-id="29718-117">Anwendungen können die registrierten CMMS auflisten und mithilfe der [**selectcmm**](/windows/win32/api/icm/nf-icm-selectcmm) -Funktion eine auswählen.</span><span class="sxs-lookup"><span data-stu-id="29718-117">Applications can enumerate the registered CMMs and select one using the [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) function.</span></span> <span data-ttu-id="29718-118">Die folgende Beispielanwendung veranschaulicht, wie alle registrierten CMMS aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="29718-118">The following sample application demonstrates how to enumerate all registered CMMs.</span></span>


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
                 gszICMatcher, &amp;hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&amp;hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &amp;dwMaxName, &amp;dwMaxValue,
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
                   &amp;cjCMM,NULL,&amp;dwType,
                   chCMMFile,&amp;cjCMMFile) == ERROR_SUCCESS)
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



 

 




