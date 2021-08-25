---
description: Beschreibt, wie ermittelt wird, ob ein bestimmter API-Satz auf dem aktuellen Gerät verfügbar ist.
title: API-Satz-Verfügbarkeit erkennen
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: cc4e26c6e59cfa0af095b297efb72a52d0be30a89a23d42d169e3bf45e72fd13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896530"
---
# <a name="detect-api-set-availability"></a>API-Satz-Verfügbarkeit erkennen

In einigen Fällen kann ein angegebener API-Satzvertragsname absichtlich einem leeren Modulnamen auf einigen Windows 10 zugeordnet werden. Die Gründe hierfür variieren, aber ein häufiges Beispiel ist, dass ein teures Feature in Bezug auf Systemressourcen aus dem Windows-Betriebssystem entfernt werden kann, wenn es für ein Gerät mit eingeschränkten Ressourcen konfiguriert ist. Dies stellt eine Herausforderung für Anwendungen dar, optionale Features auf API-Ebene ordnungsgemäß zu verarbeiten.

Der herkömmliche Ansatz zum Testen, ob eine Win32-API verfügbar ist, ist die Verwendung von [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Aufgrund der Unterstützung für die umgekehrte Weiterleitung [](api-set-loader-operation.md#reverse-forwarding) in der Api sind diese jedoch kein zuverlässiges Mittel zum Testen von API-Windows 10. Wenn die umgekehrte Weiterleitung auf eine bestimmte API angewendet wird, kann **LoadLibrary** oder **GetProcAddress** auch dann in einen gültigen Funktionszeiger auflösen, wenn die interne Implementierung entfernt wurde. In diesem Fall wird der Funktionszeiger auf eine Stubfunktion verweisen, die einfach einen Fehler zurückgibt.

Um diesen Fall zu erkennen, können Sie die [IsApiSetImplemented-Funktion](/windows/win32/api/apiquery2/nf-apiquery2-isapisetimplemented) verwenden, um die zugrunde liegende Verfügbarkeit einer bestimmten API-Implementierung abfragt. Dieser Test überprüft, ob das Aufrufen dieser Funktion zum Ausführen einer funktionalen Implementierung der API führt.

Im folgenden Codebeispiel wird veranschaulicht, wie **IsApiSetImplemented** verwendet wird, um zu bestimmen, ob die [WTSEnumerateSessions-Funktion](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumeratesessionsa) auf dem aktuellen Gerät verfügbar ist, bevor sie aufruft. 

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