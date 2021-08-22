---
title: Erkennen der Remotedesktopdienste Umgebung
description: Um die Leistung zu optimieren, sollten Anwendungen ermitteln, ob sie in einer Remotedesktopdienste ausgeführt werden.
ms.assetid: 9ba03801-8471-43a9-8e24-114a082d5776
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f54634112b4a6ac3cc1e981421e4a3e33af5e32bae8ab63ec8690f2df12c7a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657990"
---
# <a name="detecting-the-remote-desktop-services-environment"></a>Erkennen der Remotedesktopdienste Umgebung

Um die Leistung zu optimieren, sollten Anwendungen ermitteln, ob sie in einer Remotedesktopdienste ausgeführt werden. Wenn eine Anwendung beispielsweise in einer Remotesitzung ausgeführt wird, sollten unnötige grafische Effekte vermieden werden, wie unter [Graphic Effects (Grafikeffekte) beschrieben.](graphic-effects.md) Wenn der Benutzer die Anwendung in einer lokalen Umgebung ausgeführt, ist es für die Anwendung nicht so wichtig, ihr Verhalten zu optimieren.

Das folgende Beispiel zeigt eine Funktion, die **TRUE** zurückgibt, wenn die Anwendung in einer Remotesitzung ausgeführt wird, und **FALSE,** wenn die Anwendung in der Konsole ausgeführt wird.


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



Weitere Informationen finden Sie unter [Laufzeitverknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Sie sollten **getSystemMetrics(SM \_ REMOTESESSION)** nicht verwenden, um zu ermitteln, ob Ihre Anwendung in einer Remotesitzung in Windows 8 und höher oder Windows Server 2012 und höher ausgeführt wird, wenn die Remotesitzung möglicherweise auch die RemoteFX vGPU-Verbesserungen des Microsoft Remote Display Protocol (RDP) verwendet. In diesem Fall identifiziert **GetSystemMetrics (SM \_ REMOTESESSION)** die Remotesitzung als lokale Sitzung.

Ihre Anwendung kann den folgenden Registrierungsschlüssel überprüfen, um zu ermitteln, ob die Sitzung eine Remotesitzung ist, die RemoteFX vGPU verwendet. Wenn eine lokale Sitzung vorhanden ist, gibt dieser Registrierungsschlüssel die ID der lokalen Sitzung an.

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ GlassSessionId**

Wenn die ID der aktuellen Sitzung, in der die Anwendung ausgeführt wird, mit der ID im Registrierungsschlüssel identisch ist, wird die Anwendung in einer lokalen Sitzung ausgeführt. Sitzungen, die auf diese Weise als Remotesitzung identifiziert werden, umfassen Remotesitzungen, die RemoteFX vGPU verwenden. Dies wird im folgenden Beispielcode veranschaulicht.


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



 

 




