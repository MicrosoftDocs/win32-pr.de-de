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
# <a name="detect-api-set-availability"></a>API-Satz-Verfügbarkeit erkennen

In einigen Fällen kann es vorkommen, dass ein bestimmter API-Satz Vertrags Name absichtlich einem leeren Modulnamen auf einigen Windows 10-Geräten zugeordnet wird. Die Gründe hierfür variieren, aber ein gängiges Beispiel ist, dass ein kostspieliger Feature in Bezug auf Systemressourcen möglicherweise aus dem Windows-Betriebssystem entfernt wird, wenn es für ein Gerät konfiguriert ist, das mit der Ressource konfiguriert ist Dies stellt eine Herausforderung dar, damit Anwendungen optionale Features auf API-Ebene ordnungsgemäß verarbeiten können.

Die herkömmliche Methode zum Testen, ob eine Win32-API verfügbar ist, ist die Verwendung von [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Dies ist jedoch kein zuverlässiges Mittel zum Testen von API-Sätzen aufgrund der [umgekehrten Weiterleitungs](api-set-loader-operation.md#reverse-forwarding) Unterstützung in Windows 10. Wenn die umgekehrte Weiterleitung auf eine bestimmte API angewendet wird, können **LoadLibrary** oder **GetProcAddress** in einen gültigen Funktionszeiger aufgelöst werden, auch wenn die interne Implementierung entfernt wurde. In diesem Fall verweist der Funktionszeiger auf eine stubfunktion, die einfach einen Fehler zurückgibt.

Um diesen Fall zu erkennen, können Sie die [isapisetimplementierte](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) -Funktion verwenden, um die zugrunde liegende Verfügbarkeit einer bestimmten API-Implementierung abzufragen. Dieser Test überprüft, ob durch das Aufrufen dieser Funktion eine funktionale Implementierung der API ausgeführt wird.

Im folgenden Codebeispiel wird veranschaulicht, wie mit **isapisetimplementierung** bestimmt wird, ob die [wtsenumschlag](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) -Funktion auf dem aktuellen Gerät verfügbar ist, bevor Sie aufgerufen wird. 

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