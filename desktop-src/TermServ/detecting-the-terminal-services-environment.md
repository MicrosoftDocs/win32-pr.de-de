---
title: Erkennen der Remotedesktopdienste Umgebung
description: Um die Leistung zu optimieren, empfiehlt es sich, Anwendungen zu erkennen, ob Sie in einer Remotedesktopdienste Client Sitzung ausgeführt werden.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fde3263925a3b8bf4921dd0dfc95842a5dc5b4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515770"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Erkennen der Remotedesktopdienste Umgebung

Um die Leistung zu optimieren, empfiehlt es sich, Anwendungen zu erkennen, ob Sie in einer Remotedesktopdienste Client Sitzung ausgeführt werden. Wenn eine Anwendung z. b. in einer Remote Sitzung ausgeführt wird, sollten Sie unnötige grafische Effekte vermeiden, wie in [grafische Effekte](graphic-effects.md)beschrieben. Wenn der Benutzer die Anwendung in einer lokalen Umgebung durchführt, ist es für die Anwendung nicht so wichtig, das Verhalten zu optimieren.

Das folgende Beispiel zeigt eine Funktion, die **true** zurückgibt, wenn die Anwendung in einer Remote Sitzung ausgeführt wird, und **false** , wenn die Anwendung in der Konsole ausgeführt wird.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Weitere Informationen finden Sie unter [Lauf Zeit Verknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Sie sollten **GetSystemMetrics (SM \_ remotesession)** nicht verwenden, um zu bestimmen, ob Ihre Anwendung in einer Remote Sitzung unter Windows 8 und höher oder Windows Server 2012 und höher ausgeführt wird, wenn die Remote Sitzung möglicherweise auch die remotefx-vgpu-Verbesserungen für das Microsoft Remote Display Protocol (RDP) verwendet. In diesem Fall identifiziert **GetSystemMetrics (SM \_ remotesession)** die Remote Sitzung als lokale Sitzung.

Die Anwendung kann den folgenden Registrierungsschlüssel überprüfen, um zu bestimmen, ob es sich bei der Sitzung um eine Remote Sitzung handelt, die remotefx vgpu verwendet. Wenn eine lokale Sitzung vorhanden ist, stellt dieser Registrierungsschlüssel die ID der lokalen Sitzung bereit.

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ glasssessionid**

Wenn die ID der aktuellen Sitzung, in der die Anwendung ausgeführt wird, mit der ID im Registrierungsschlüssel identisch ist, wird die Anwendung in einer lokalen Sitzung ausgeführt. Sitzungen, die auf diese Weise als Remote Sitzung identifiziert werden, schließen Remote Sitzungen ein, die remotefx vgpu verwenden. Dies wird im folgenden Beispielcode veranschaulicht.


```C++
#define TERMINAL_SERVER_KEY _T("SYSTEM\\CurrentControlSet\\Control\\Terminal Server\\")
#define GLASS_SESSION_ID    _T("GlassSessionId")

BOOL
IsCurrentSessionRemoteable()
{
    BOOL fIsRemoteable = FALSE;
                                       
    if (GetSystemMetrics(SM_REMOTESESSION)) 
    {
        fIsRemoteable = TRUE;
    }
    else
    {
        HKEY hRegKey = NULL;
        LONG lResult;

        lResult = RegOpenKeyEx(
            HKEY_LOCAL_MACHINE,
            TERMINAL_SERVER_KEY,
            0, // ulOptions
            KEY_READ,
            &hRegKey
            );

        if (lResult == ERROR_SUCCESS)
        {
            DWORD dwGlassSessionId;
            DWORD cbGlassSessionId = sizeof(dwGlassSessionId);
            DWORD dwType;

            lResult = RegQueryValueEx(
                hRegKey,
                GLASS_SESSION_ID,
                NULL, // lpReserved
                &dwType,
                (BYTE*) &dwGlassSessionId,
                &cbGlassSessionId
                );

            if (lResult == ERROR_SUCCESS)
            {
                DWORD dwCurrentSessionId;

                if (ProcessIdToSessionId(GetCurrentProcessId(), &dwCurrentSessionId))
                {
                    fIsRemoteable = (dwCurrentSessionId != dwGlassSessionId);
                }
            }
        }

        if (hRegKey)
        {
            RegCloseKey(hRegKey);
        }
    }

    return fIsRemoteable;
}
```



 

 




