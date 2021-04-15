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
# <a name="detecting-the-remote-desktop-services-environment"></a><span data-ttu-id="5427f-103">Erkennen der Remotedesktopdienste Umgebung</span><span class="sxs-lookup"><span data-stu-id="5427f-103">Detecting the Remote Desktop Services environment</span></span>

<span data-ttu-id="5427f-104">Um die Leistung zu optimieren, empfiehlt es sich, Anwendungen zu erkennen, ob Sie in einer Remotedesktopdienste Client Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5427f-104">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span> <span data-ttu-id="5427f-105">Wenn eine Anwendung z. b. in einer Remote Sitzung ausgeführt wird, sollten Sie unnötige grafische Effekte vermeiden, wie in [grafische Effekte](graphic-effects.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5427f-105">For example, when an application is running on a remote session, it should eliminate unnecessary graphic effects, as described in [Graphic Effects](graphic-effects.md).</span></span> <span data-ttu-id="5427f-106">Wenn der Benutzer die Anwendung in einer lokalen Umgebung durchführt, ist es für die Anwendung nicht so wichtig, das Verhalten zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="5427f-106">If the user is running the application in a local environment, it is not as critical for the application to optimize its behavior.</span></span>

<span data-ttu-id="5427f-107">Das folgende Beispiel zeigt eine Funktion, die **true** zurückgibt, wenn die Anwendung in einer Remote Sitzung ausgeführt wird, und **false** , wenn die Anwendung in der Konsole ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5427f-107">The following example shows a function that returns **TRUE** if the application is running in a remote session and **FALSE** if the application is running on the console.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "user32.lib")

BOOL IsRemoteSession(void)
{
   return GetSystemMetrics( SM_REMOTESESSION );
}
```



<span data-ttu-id="5427f-108">Weitere Informationen finden Sie unter [Lauf Zeit Verknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5427f-108">For more information, see [Run-time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="5427f-109">Sie sollten **GetSystemMetrics (SM \_ remotesession)** nicht verwenden, um zu bestimmen, ob Ihre Anwendung in einer Remote Sitzung unter Windows 8 und höher oder Windows Server 2012 und höher ausgeführt wird, wenn die Remote Sitzung möglicherweise auch die remotefx-vgpu-Verbesserungen für das Microsoft Remote Display Protocol (RDP) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5427f-109">You should not use **GetSystemMetrics(SM\_REMOTESESSION)** to determine if your application is running in a remote session in Windows 8 and later or Windows Server 2012 and later if the remote session may also be using the RemoteFX vGPU improvements to the Microsoft Remote Display Protocol (RDP).</span></span> <span data-ttu-id="5427f-110">In diesem Fall identifiziert **GetSystemMetrics (SM \_ remotesession)** die Remote Sitzung als lokale Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5427f-110">In this case, **GetSystemMetrics(SM\_REMOTESESSION)** will identify the remote session as a local session.</span></span>

<span data-ttu-id="5427f-111">Die Anwendung kann den folgenden Registrierungsschlüssel überprüfen, um zu bestimmen, ob es sich bei der Sitzung um eine Remote Sitzung handelt, die remotefx vgpu verwendet.</span><span class="sxs-lookup"><span data-stu-id="5427f-111">Your application can check the following registry key to determine whether the session is a remote session that uses RemoteFX vGPU.</span></span> <span data-ttu-id="5427f-112">Wenn eine lokale Sitzung vorhanden ist, stellt dieser Registrierungsschlüssel die ID der lokalen Sitzung bereit.</span><span class="sxs-lookup"><span data-stu-id="5427f-112">If a local session exists, this registry key provides the ID of the local session.</span></span>

<span data-ttu-id="5427f-113">**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Terminal Server \\ glasssessionid**</span><span class="sxs-lookup"><span data-stu-id="5427f-113">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Terminal Server\\GlassSessionId**</span></span>

<span data-ttu-id="5427f-114">Wenn die ID der aktuellen Sitzung, in der die Anwendung ausgeführt wird, mit der ID im Registrierungsschlüssel identisch ist, wird die Anwendung in einer lokalen Sitzung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5427f-114">If the ID of the current session in which the application is running is the same as in the registry key, the application is running in a local session.</span></span> <span data-ttu-id="5427f-115">Sitzungen, die auf diese Weise als Remote Sitzung identifiziert werden, schließen Remote Sitzungen ein, die remotefx vgpu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5427f-115">Sessions identified as remote session in this way include remote sessions that use RemoteFX vGPU.</span></span> <span data-ttu-id="5427f-116">Dies wird im folgenden Beispielcode veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5427f-116">The following sample code demonstrates this.</span></span>


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



 

 




