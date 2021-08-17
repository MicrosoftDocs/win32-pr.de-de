---
description: In diesem Abschnitt wird beschrieben, wie Sie bestimmen, unter welcher Version der Shell-DLLs Ihre Anwendung ausgeführt wird und wie Sie ihre Anwendung auf eine bestimmte Version ausrichten.
title: 'Shell- und Shlwapi-DLL-Versionen '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6d74371478b30037e75b1c168dc235735ba6bd219fa461245262ff55a508ae5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967835"
---
# <a name="shell-and-shlwapi-dll-versions"></a>Shell- und Shlwapi-DLL-Versionen 

In diesem Abschnitt wird beschrieben, wie Sie bestimmen, unter welcher Version der Shell-DLLs Ihre Anwendung ausgeführt wird und wie Sie ihre Anwendung auf eine bestimmte Version ausrichten.

-   [DLL-Versionsnummern](#dll-version-numbers)
-   [Ermitteln der Versionsnummer mithilfe von DllGetVersion](#using-dllgetversion-to-determine-the-version-number)
    -   [Verwenden von DllGetVersion](#using-dllgetversion)
-   [Project Versionen](#project-versions)

## <a name="dll-version-numbers"></a>DLL-Versionsnummern

Alle Programmierelemente bis auf einige der in der Shell-Dokumentation erläuterten Programmierelemente sind in zwei DLLs enthalten: Shell32.dll und Shlwapi.dll. Aufgrund fortlaufender Verbesserungen implementieren verschiedene Versionen dieser DLLs unterschiedliche Features. In der Gesamten Shell-Referenzdokumentation gibt jedes Programmierelement eine mindestens unterstützte DLL-Versionsnummer an. Diese Versionsnummer gibt an, dass das Programmierelement in dieser Version und nachfolgenden Versionen der DLL implementiert ist, sofern nichts anderes angegeben ist. Wenn keine Versionsnummer angegeben wird, wird das Programmierelement in allen vorhandenen Versionen der DLL implementiert.

Vor Windows XP wurden neue Shell32.dll- und Shlwapi.dll-Versionen manchmal mit neuen Versionen von Windows Internet Explorer bereitgestellt. Ab Windows XP wurden diese DLLs nicht mehr als verteilbare Dateien außerhalb neuer Versionen von Windows selbst bereitgestellt. In der folgenden Tabelle werden die verschiedenen DLL-Versionen und deren Verteilung an Microsoft Internet Explorer 3.0, Windows 95 und Microsoft Windows NT 4.0 beschrieben.

Shell32.dll Version 4.0 befindet sich in den ursprünglichen Versionen von Windows 95 und Microsoft Windows NT 4.0. Die Shell wurde nicht mit dem Release Internet Explorer 3.0 aktualisiert, sodass Shell32.dll nicht über version 4.70 verfügt. Shell32.dll Versionen 4.71 und 4.72 wurden mit den entsprechenden Internet Explorer Releases ausgeliefert, aber nicht notwendigerweise installiert (siehe Hinweis 1). Bei Versionen nach Microsoft Internet Explorer 4.01 und Windows 98 unterscheiden sich die Versionsnummern für Shell32.dll und Shlwapi.dll. Im Allgemeinen sollten Sie davon ausgehen, dass die DLLs unterschiedliche Versionsnummern aufweisen und jede einzeln testen.

#### <a name="shell32dll"></a>Shell32.dll

| Version | Verteilungsplattform                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 und Microsoft Windows NT 4.0                                     |
| 4.71    | Microsoft Internet Explorer 4.0. (siehe Hinweis 1).                                |
| 4.72    | Internet Explorer 4.01 und Windows 98. (siehe Hinweis 1).                          |
| 5.0     | Windows 2000 und Windows Edition (Windows Me). Siehe Hinweis 2.       |
| 6.0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| Version | Verteilungsplattform                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 und Microsoft Windows NT 4.0                                     |
| 4.71    | Internet Explorer 4.0. (siehe Hinweis 1).                                          |
| 4.72    | Internet Explorer 4.01 und Windows 98. (siehe Hinweis 1).                          |
| 4,7     | Internet Explorer 3.x                                                       |
| 5.0     | Microsoft Internet Explorer 5 und Windows 98 SE. Siehe Hinweis 2.                |
| 5.5     | Microsoft Internet Explorer 5.5 und Windows Edition (Windows Me) |
| 6.0     | Windows XP und Windows Vista                                                |



**Hinweis 1:** Alle Systeme mit Internet Explorer 4.0 oder 4.01 verfügten über die zugeordnete Version von Shlwapi.dll (4.71 bzw. 4.72). Für Systeme vor Windows 98 können Internet Explorer 4.0 und 4.01 jedoch mit oder ohne die sogenannte *integrierte Shell* installiert werden. Wenn Internet Explorer mit der integrierten Shell installiert wurde, wurde auch die zugehörige Version von Shell32.dll (4.71 oder 4.72) installiert. Wenn Internet Explorer ohne die integrierte Shell installiert wurde, Shell32.dll weiterhin Version 4.0. Anders ausgedrückt: Das Vorhandensein von Version 4.71 oder 4.72 von Shlwapi.dll auf einem System garantiert nicht, dass Shell32.dll die gleiche Versionsnummer hat. Alle Windows 98-Systeme verfügen über Version 4.72 von Shell32.dll.

**Hinweis 2:** Version 5.0 von Shlwapi.dll wurde mit Internet Explorer 5 verteilt und wurde auf allen Systemen gefunden, auf denen Internet Explorer 5 installiert war, mit Ausnahme von Windows 2000. Version 5.0 von Shell32.dll wurde nativ mit Windows 2000 und Windows Edition (Windows Me) zusammen mit Version 5.0 von Shlwapi.dll verteilt.

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Ermitteln der Versionsnummer mithilfe von DllGetVersion

Ab Version 4.71 haben die Shell-DLLs unter anderem damit begonnen, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc)zu exportieren. Diese Funktion kann von einer Anwendung aufgerufen werden, um zu bestimmen, welche DLL-Version auf dem System vorhanden ist.

> [!Note]  
> DLLs exportieren nicht unbedingt [**DllGetVersion.**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) Testen Sie es immer, bevor Sie versuchen, es zu verwenden.

Für Windows Versionen vor Windows 2000 gibt [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) eine [**DLLVERSIONINFO-Struktur**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) zurück, die die Haupt- und Nebenversionsnummer, die Buildnummer und eine Plattform-ID enthält. Für Windows Systeme ab 2000 gibt **DllGetVersion** möglicherweise stattdessen eine [**DLLVERSIONINFO2-Struktur**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) zurück. Zusätzlich zu den Informationen, die über **DLLVERSIONINFO** bereitgestellt werden, stellt **DLLVERSIONINFO2** auch die Hotfixnummer bereit, mit der das neueste installierte Service Pack identifiziert wird. Dies bietet eine stabilere Möglichkeit zum Vergleichen von Versionsnummern. Da der erste Member von **DLLVERSIONINFO2** eine **DLLVERSIONINFO-Struktur** ist, ist die spätere -Struktur abwärtskompatibel.

### <a name="using-dllgetversion"></a>Verwenden von DllGetVersion

Die folgende Beispielfunktion `GetVersion` lädt eine angegebene DLL und versucht, ihre [**DllGetVersion-Funktion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) aufzurufen. Bei Erfolg wird ein Makro verwendet, um die Haupt- und Nebenversionsnummern aus der [**DLLVERSIONINFO-Struktur**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) in ein **DWORD** zu packen, das an die aufrufende Anwendung zurückgegeben wird. Wenn die DLL **dllGetVersion** nicht exportiert, gibt die Funktion 0 (null) zurück. Mit Windows 2000- und höher-Systemen können Sie die Funktion ändern, um die Möglichkeit zu behandeln, dass **DllGetVersion** eine [**DLLVERSIONINFO2-Struktur**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) zurückgibt. Wenn ja, verwenden Sie die Informationen im **ullVersion-Member** der **DLLVERSIONINFO2-Struktur,** um Versionen, Buildnummern und Service Pack-Releases zu vergleichen. Das [**MAKEDLLVERULL-Makro**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) vereinfacht die Aufgabe, diese Werte mit denen in **ullVersion** zu vergleichen.

> [!Note]  
> Die falsche Verwendung von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Windows finden Sie in der **LoadLibrary-Dokumentation.**


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


Im folgenden Codebeispiel wird veranschaulicht, wie Sie verwenden `GetVersion` können, um zu testen, ob Shell32.dll Version 6.0 oder höher ist.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a>Project Versionen

Um sicherzustellen, dass Ihre Anwendung mit verschiedenen Zielversionen einer .dll-Datei kompatibel ist, sind Versionsmakros in den Headerdateien vorhanden. Diese Makros werden verwendet, um bestimmte Definitionen für verschiedene Versionen der DLL zu definieren, auszuschließen oder neu zu definieren. Eine ausführliche Beschreibung dieser Makros finden Sie unter Verwenden der [Windows Header.](../winprog/using-the-windows-headers.md)

Beispielsweise ist der Makroname **\_ WIN32 \_ IE** häufig in älteren Headern zu finden. Sie sind dafür verantwortlich, das Makro als Hexadezimalzahl zu definieren. Diese Versionsnummer definiert die Zielversion der Anwendung, die die DLL verwendet. Die folgende Tabelle zeigt die verfügbaren Versionsnummern und die Auswirkungen, die jede auf Ihre Anwendung hat.


| Version | Beschreibung                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | Die Anwendung ist mit Shell32.dll Version 4.00 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 4.00 hinzugefügt wurden.                                              |
| 0x0300  | Die Anwendung ist mit Shell32.dll 4.70 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 4.70 hinzugefügt wurden.                                              |
| 0x0400  | Die Anwendung ist mit Shell32.dll 4.71 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 4.71 hinzugefügt wurden.                                              |
| 0x0401  | Die Anwendung ist mit Shell32.dll 4.72 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 4.72 hinzugefügt wurden.                                              |
| 0x0500  | Die Anwendung ist mit Shell32.dll und Shlwapi.dll 5.0 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 5.0 von Shell32.dll und Shlwapi.dll. |
| 0x0501  | Die Anwendung ist mit Shell32.dll und Shlwapi.dll 5.0 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 5.0 von Shell32.dll und Shlwapi.dll. |
| 0x0600  | Die Anwendung ist mit Shell32.dll und Shlwapi.dll 6.0 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 6.0 von Shell32.dll und Shlwapi.dll. |


Wenn Sie das **\_ WIN32 \_ IE-Makro** in Ihrem Projekt nicht definieren, wird es automatisch als 0x0500. Um einen anderen Wert zu definieren, können Sie den Compiler-Direktiven in ihrer Make-Datei Folgendes hinzufügen: Ersetzen Sie die gewünschte Versionsnummer durch 0x0400.

```
/D _WIN32_IE=0x0400
```

Eine andere Methode besteht im Hinzufügen einer Zeile ähnlich der folgenden im Quellcode, bevor Sie die Shellheaderdateien hinzufügen. Ersetzen Sie die gewünschte Versionsnummer durch 0x0400.

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
