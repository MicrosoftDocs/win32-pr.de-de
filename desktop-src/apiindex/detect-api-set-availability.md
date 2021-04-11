---
description: Beschreibt, wie Sie erkennen können, ob ein bestimmter API-Satz auf dem aktuellen Gerät verfügbar ist.
title: API-Satz-Verfügbarkeit erkennen
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 7117ae82f142315a3e5f28065583381ef6af67f3
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2020
ms.locfileid: "104102546"
---
# <a name="detect-api-set-availability"></a><span data-ttu-id="f2f54-103">API-Satz-Verfügbarkeit erkennen</span><span class="sxs-lookup"><span data-stu-id="f2f54-103">Detect API set availability</span></span>

<span data-ttu-id="f2f54-104">In einigen Fällen kann es vorkommen, dass ein bestimmter API-Satz Vertrags Name absichtlich einem leeren Modulnamen auf einigen Windows 10-Geräten zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f2f54-104">In some cases, a given API set contract name may be intentionally mapped to an empty module name on some Windows 10 devices.</span></span> <span data-ttu-id="f2f54-105">Die Gründe hierfür variieren, aber ein gängiges Beispiel ist, dass ein kostspieliger Feature in Bezug auf Systemressourcen möglicherweise aus dem Windows-Betriebssystem entfernt wird, wenn es für ein Gerät konfiguriert ist, das mit der Ressource konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="f2f54-105">The reasons for this vary, but a common example is that an expensive feature in terms of system resources may be removed from the Windows OS when configured for a resource-constrained device.</span></span> <span data-ttu-id="f2f54-106">Dies stellt eine Herausforderung dar, damit Anwendungen optionale Features auf API-Ebene ordnungsgemäß verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f2f54-106">This poses a challenge for applications to gracefully handle optional features at the API level.</span></span>

<span data-ttu-id="f2f54-107">Die herkömmliche Methode zum Testen, ob eine Win32-API verfügbar ist, ist die Verwendung von [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="f2f54-107">The traditional approach for testing whether a Win32 API is available is to use [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="f2f54-108">Dies ist jedoch kein zuverlässiges Mittel zum Testen von API-Sätzen aufgrund der [umgekehrten Weiterleitungs](api-set-loader-operation.md#reverse-forwarding) Unterstützung in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f2f54-108">However, these are not a reliable means for testing API sets because of the [reverse forwarding](api-set-loader-operation.md#reverse-forwarding) support in Windows 10.</span></span> <span data-ttu-id="f2f54-109">Wenn die umgekehrte Weiterleitung auf eine bestimmte API angewendet wird, können **LoadLibrary** oder **GetProcAddress** in einen gültigen Funktionszeiger aufgelöst werden, auch wenn die interne Implementierung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2f54-109">When reverse forwarding is applied to a given API, **LoadLibrary** or **GetProcAddress** may resolve to a valid function pointer even in cases where the internal implementation has been removed.</span></span> <span data-ttu-id="f2f54-110">In diesem Fall verweist der Funktionszeiger auf eine stubfunktion, die einfach einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f2f54-110">In this case, the function pointer will be pointing to a stub function that simply returns an error.</span></span>

<span data-ttu-id="f2f54-111">Um diesen Fall zu erkennen, können Sie die [isapisetimplementierte](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) -Funktion verwenden, um die zugrunde liegende Verfügbarkeit einer bestimmten API-Implementierung abzufragen.</span><span class="sxs-lookup"><span data-stu-id="f2f54-111">In order to detect this case, you can use the [IsApiSetImplemented](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) function to query the underlying availability of a given API implementation.</span></span> <span data-ttu-id="f2f54-112">Dieser Test überprüft, ob durch das Aufrufen dieser Funktion eine funktionale Implementierung der API ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2f54-112">This test validates that calling this function will result in executing a functional implementation of the API.</span></span>

<span data-ttu-id="f2f54-113">Im folgenden Codebeispiel wird veranschaulicht, wie mit **isapisetimplementierung** bestimmt wird, ob die [wtsenumschlag](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) -Funktion auf dem aktuellen Gerät verfügbar ist, bevor Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f2f54-113">The following code example demonstrates how to use **IsApiSetImplemented** to determine whether the [WTSEnumerateSessions](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) function is available on the current device before calling it.</span></span> 

```c++
#include <windows.h>
#include <stdio.h>
#include <Wtsapi32.h>

int __cdecl wmain(int /* argc */, PCWSTR /* argv */ [])
{
    PWTS_SESSION_INFO pInfo = {};
    DWORD count = 0;

    if (!IsApiSetImplemented("ext-ms-win-session-wtsapi32-l1-1-0"))
    {
        wprintf(L"IsApiSetImplemented on ext-ms-win-session-wtsapi32-l1-1-0 returns FALSE\n");
    }
    else
    {
        if (WTSEnumerateSessionsW(WTS_CURRENT_SERVER_HANDLE, 0, 1, &pInfo, &count))
        {
            wprintf(L"SessionCount = %d\n", count);

            for (ULONG i = 0; i < count; i++)
            {
                PWTS_SESSION_INFO pCurInfo = &pInfo[i];
                wprintf(L"    %s: ID = %d, state = %d\n", pCurInfo->pWinStationName, 
                    pCurInfo->SessionId, pCurInfo->State);
            }

            WTSFreeMemory(pInfo);
        }
        else
        {
            wprintf(L"WTSEnumerateSessions failure : %x\n", GetLastError());
        }
    }

    return 0;
}
```