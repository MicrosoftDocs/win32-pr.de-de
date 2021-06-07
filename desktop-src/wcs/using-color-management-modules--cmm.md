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
# <a name="using-color-management-modules-cmm"></a>Verwenden von Farbverwaltungsmodulen (CMM)

Color Management Modules (CMMs) sind Module mit WCS-Code, die die Informationen in Geräteprofilen verwenden, um Farbkonvertierung und Farbzuordnung durchzuführen. Anwendungsentwickler sollten keine CMMs implementieren müssen. Microsoft stellt das Standard-CMM zur Verfügung. Wenn Sie jedoch Software schreiben, die die Verwendung spezieller Farbkonvertierungs- und Farbzuordnungsalgorithmen erfordert, können Sie einen erstellen.

> [!Note]  
> CMM-Einstiegspunkte *sind keine* API-Funktionen und sollten nicht von Anwendungen aufgerufen werden.

 

Wenn CMMs installiert sind, registriert das Installationsprogramm sie in der Windows-Registrierung. Anwendungen können die registrierten CMMs auflisten und mithilfe der [**SelectCMM-Funktion eines**](/windows/win32/api/icm/nf-icm-selectcmm) auswählen. Die folgende Beispielanwendung veranschaulicht, wie sie alle registrierten CMMs aufzählt.


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



 

 




