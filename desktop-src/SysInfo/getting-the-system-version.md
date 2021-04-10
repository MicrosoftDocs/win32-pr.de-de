---
description: Im folgenden Beispiel wird die Versions-API-Hilfsfunktion verwendet, um die Version des aktuellen Betriebssystems zu ermitteln, sofern es sich um einen Server oder eine Client Version handelt, und zeigt diese Informationen dann in der-Konsole an.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: System Version wird erhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fa259378b81f9255846694927ee2b68e6f38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869211"
---
# <a name="getting-the-system-version"></a>System Version wird erhalten

Im folgenden Beispiel wird die Versions- [API-Hilfsfunktion](version-helper-apis.md) verwendet, um die Version des aktuellen Betriebssystems zu ermitteln, sofern es sich um einen Server oder eine Client Version handelt, und zeigt diese Informationen dann in der-Konsole an. Wenn der Kompatibilitätsmodus aktiviert ist, wird im Beispiel das für die [Anwendungs Kompatibilität](/previous-versions/bb757005(v=msdn.10))ausgewählte Betriebssystem angezeigt.

Die Verwendung von Versionsinformationen ist nicht die beste Methode, um eine Funktion zu testen. Lesen Sie stattdessen die Dokumentation für das relevante Feature. Weitere Informationen zu allgemeinen Techniken für die Funktionserkennung finden Sie unter [Betriebs System Version](operating-system-version.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <VersionHelpers.h>

int 
__cdecl
wmain(
    __in int argc, 
    __in_ecount(argc) PCWSTR argv[]
    )
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    if (IsWindowsXPOrGreater())
    {
        printf("XPOrGreater\n");
    }

    if (IsWindowsXPSP1OrGreater())
    {
        printf("XPSP1OrGreater\n");
    }

    if (IsWindowsXPSP2OrGreater())
    {
        printf("XPSP2OrGreater\n");
    }

    if (IsWindowsXPSP3OrGreater())
    {
        printf("XPSP3OrGreater\n");
    }

    if (IsWindowsVistaOrGreater())
    {
        printf("VistaOrGreater\n");
    }

    if (IsWindowsVistaSP1OrGreater())
    {
        printf("VistaSP1OrGreater\n");
    }

    if (IsWindowsVistaSP2OrGreater())
    {
        printf("VistaSP2OrGreater\n");
    }

    if (IsWindows7OrGreater())
    {
        printf("Windows7OrGreater\n");
    }

    if (IsWindows7SP1OrGreater())
    {
        printf("Windows7SP1OrGreater\n");
    }

    if (IsWindows8OrGreater())
    {
        printf("Windows8OrGreater\n");
    }

    if (IsWindows8Point1OrGreater())
    {
        printf("Windows8Point1OrGreater\n");
    }

    if (IsWindows10OrGreater())
    {
        printf("Windows10OrGreater\n");
    }

    if (IsWindowsServer())
    {
        printf("Server\n");
    }
    else
    {
        printf("Client\n");
    }
}
```



 

 
