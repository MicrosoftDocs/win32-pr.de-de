---
description: In diesem Abschnitt wird beschrieben, wie Sie bestimmen können, auf welcher Version der Shell-DLLs Ihre Anwendung ausgeführt wird und wie Sie Ihre Anwendung für eine bestimmte Version als Ziel festlegen.
title: 'Shell- und Shlwapi-DLL-Versionen '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215930"
---
# <a name="shell-and-shlwapi-dll-versions"></a>Shell- und Shlwapi-DLL-Versionen 

In diesem Abschnitt wird beschrieben, wie Sie bestimmen können, auf welcher Version der Shell-DLLs Ihre Anwendung ausgeführt wird und wie Sie Ihre Anwendung für eine bestimmte Version als Ziel festlegen.

-   [DLL-Versionsnummern](#dll-version-numbers)
-   [Verwenden von dllgetversion zum Ermitteln der Versionsnummer](#using-dllgetversion-to-determine-the-version-number)
    -   [Verwenden von "dllgetversion"](#using-dllgetversion)
-   [Projekt Versionen](#project-versions)

## <a name="dll-version-numbers"></a>DLL-Versionsnummern

Die in der shelldokumentation erörterten Programmier Elemente sind in zwei DLLs enthalten: Shell32.dll und Shlwapi.dll. Aufgrund von kontinuierlichen Verbesserungen implementieren verschiedene Versionen dieser DLLs verschiedene Funktionen. In der gesamten shellverweisdokumentation gibt jedes Programmier Element eine unterstützte dll-Versionsnummer an. Diese Versionsnummer gibt an, dass das Programmier Element in dieser Version und in nachfolgenden Versionen der dll implementiert ist, sofern nicht anders angegeben. Wenn keine Versionsnummer angegeben ist, wird das Programmier Element in allen vorhandenen Versionen der dll implementiert.

Vor Windows XP wurden neue Shell32.dll und Shlwapi.dll Versionen in einigen Fällen mit neuen Versionen von Windows Internet Explorer bereitgestellt. Ab Windows XP wurden diese DLLs nicht mehr als verteilbare Dateien außerhalb neuer Versionen von Windows selbst bereitgestellt. In der folgenden Tabelle werden die verschiedenen dll-Versionen und deren Verteilung auf den Microsoft Internet Explorer 3,0, Windows 95 und Microsoft Windows NT 4,0 beschrieben.

Shell32.dll Version 4,0 wurde in den ursprünglichen Versionen von Windows 95 und Microsoft Windows NT 4,0 gefunden. Die Shell wurde nicht mit der Version Internet Explorer 3,0 aktualisiert, sodass Shell32.dll nicht über die Version 4,70 verfügt. Shell32.dll Versionen 4,71 und 4,72 waren mit den entsprechenden Internet Explorer-Releases ausgeliefert, aber Sie wurden nicht notwendigerweise installiert (siehe Hinweis 1). Bei Releases nach Microsoft Internet Explorer 4,01 und Windows 98 sind die Versionsnummern für Shell32.dll und Shlwapi.dll voneinander abweicht. Im Allgemeinen sollten Sie davon ausgehen, dass die DLLs über unterschiedliche Versionsnummern verfügen, und jede einzelne einzeln testen.

#### <a name="shell32dll"></a>Shell32.dll

| Version | Verteilungs Plattform                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 und Microsoft Windows NT 4,0                                     |
| 4.71    | Microsoft Internet Explorer 4,0. (siehe Hinweis 1).                                |
| 4.72    | Internet Explorer 4,01 und Windows 98. (siehe Hinweis 1).                          |
| 5.0     | Windows 2000 und Windows Millennium Edition (Windows Me). Siehe Hinweis 2.       |
| 6.0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| Version | Verteilungs Plattform                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 und Microsoft Windows NT 4,0                                     |
| 4.71    | Internet Explorer 4,0. (siehe Hinweis 1).                                          |
| 4.72    | Internet Explorer 4,01 und Windows 98. (siehe Hinweis 1).                          |
| 4,7     | Internet Explorer 3. x                                                       |
| 5.0     | Microsoft Internet Explorer 5 und Windows 98 SE. Siehe Hinweis 2.                |
| 5.5     | Microsoft Internet Explorer 5,5 und Windows Millennium Edition (Windows Me) |
| 6.0     | Windows XP und Windows Vista                                                |



**Hinweis 1:** Alle Systeme mit Internet Explorer 4,0 oder 4,01 verfügten über die zugehörige Version von Shlwapi.dll (4,71 oder 4,72). Allerdings können Internet Explorer 4,0 und 4,01 für Systeme vor Windows 98 mit oder ohne die so genannte *integrierte Shell* installiert werden. Wenn Internet Explorer mit der integrierten Shell installiert wurde, wurde auch die zugehörige Version von Shell32.dll (4,71 oder 4,72) installiert. Wenn Internet Explorer ohne die integrierte Shell installiert wurde, Shell32.dll als Version 4,0 geblieben. Anders ausgedrückt bedeutet das vorhanden sein von Version 4,71 oder 4,72 von Shlwapi.dll auf einem System nicht, dass Shell32.dll die gleiche Versionsnummer hat. Alle Windows 98-Systeme verfügen über die Version 4,72 von Shell32.dll.

**Hinweis 2:** Die Version 5,0 von Shlwapi.dll wurde mit Internet Explorer 5 verteilt und wurde auf allen Systemen gefunden, auf denen Internet Explorer 5 installiert war, mit Ausnahme von Windows 2000. Die Version 5,0 von Shell32.dll wurde nativ mit Windows 2000 und Windows Millennium Edition (Windows Me) zusammen mit Version 5,0 Shlwapi.dll verteilt.

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Verwenden von dllgetversion zum Ermitteln der Versionsnummer

Ab Version 4,71 haben die shelldlls unter anderem begonnen, [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc)zu exportieren. Diese Funktion kann von einer Anwendung aufgerufen werden, um zu bestimmen, welche DLL-Version auf dem System vorhanden ist.

> [!Note]  
> DLLs exportieren nicht notwendigerweise [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Testen Sie Sie immer, bevor Sie versuchen, Sie zu verwenden.

Bei Windows-Versionen vor Windows 2000 gibt [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) eine [**dllversioninfo**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) -Struktur zurück, die die Haupt-und neben Versionsnummern, die Buildnummer und eine Platt Form-ID enthält. Für Windows 2000-Systeme und spätere Systeme gibt **dllgetversion** möglicherweise stattdessen eine [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurück. Zusätzlich zu den Informationen, die über **dllversioninfo** bereitgestellt werden, stellt **DLLVERSIONINFO2** auch die Hotfixnummer bereit, mit der die neuesten installierten Service Pack identifiziert werden, die eine stabilere Möglichkeit zum Vergleichen von Versionsnummern bietet. Da der erste Member von **DLLVERSIONINFO2** eine **dllversioninfo** -Struktur ist, ist die spätere Struktur abwärts kompatibel.

### <a name="using-dllgetversion"></a>Verwenden von "dllgetversion"

Die folgende Beispiel Funktion `GetVersion` lädt eine angegebene DLL und versucht, Ihre [**dllgetversion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) -Funktion aufzurufen. Wenn erfolgreich, wird ein Makro verwendet, um die Haupt-und neben Versionsnummern aus der [**dllversioninfo**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) -Struktur in ein **DWORD** zu packen, das an die aufrufenden Anwendung zurückgegeben wird. Wenn die DLL **dllgetversion** nicht exportiert, gibt die Funktion 0 (null) zurück. Mit Windows 2000 und neueren Systemen können Sie die Funktion ändern, um die Möglichkeit zu verarbeiten, dass **dllgetversion** eine [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurückgibt. Wenn dies der Fall ist, verwenden Sie die Informationen im **ullversion** -Member der **DLLVERSIONINFO2** -Struktur, um Versionen, Buildnummern und Service Pack Releases zu vergleichen. Das [**makedllverull**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) -Makro vereinfacht die Aufgabe, diese Werte mit den Werten in **ullversion** zu vergleichen.

> [!Note]  
> Das nicht ordnungsgemäße Verwenden von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen. Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .


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


Im folgenden Codebeispiel wird veranschaulicht, wie Sie `GetVersion` mit überprüfen können, ob Shell32.dll die Version 6,0 oder höher ist.


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


## <a name="project-versions"></a>Projekt Versionen

Um sicherzustellen, dass Ihre Anwendung mit unterschiedlichen Ziel Versionen einer DLL-Datei kompatibel ist, sind Versions Makros in den Header Dateien vorhanden. Diese Makros werden verwendet, um bestimmte Definitionen für verschiedene Versionen der dll zu definieren, auszuschließen oder neu zu definieren. Eine ausführliche Beschreibung dieser Makros finden [Sie unter Verwenden der Windows-Header](../winprog/using-the-windows-headers.md) .

Beispielsweise befindet sich der Makro Name **\_ Win32 \_ IE** häufig in älteren Headern. Sie sind dafür verantwortlich, das Makro als hexadezimale Zahl zu definieren. Diese Versionsnummer definiert die Zielversion der Anwendung, die die dll verwendet. In der folgenden Tabelle sind die verfügbaren Versionsnummern und die Auswirkungen der einzelnen Anwendungen aufgeführt.


| Version | BESCHREIBUNG                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | Die Anwendung ist kompatibel mit Shell32.dll Version 4,00 und höher. Die Anwendung kann keine Features implementieren, die nach Version 4,00 hinzugefügt wurden.                                              |
| 0x0300  | Die Anwendung ist kompatibel mit Shell32.dll Version 4,70 und höher. Die Anwendung kann keine Features implementieren, die nach Version 4,70 hinzugefügt wurden.                                              |
| 0x0400  | Die Anwendung ist kompatibel mit Shell32.dll Version 4,71 und höher. Die Anwendung kann keine Features implementieren, die nach Version 4,71 hinzugefügt wurden.                                              |
| 0x0401  | Die Anwendung ist kompatibel mit Shell32.dll Version 4,72 und höher. Die Anwendung kann keine Features implementieren, die nach Version 4,72 hinzugefügt wurden.                                              |
| 0x0500 sein  | Die Anwendung ist kompatibel mit Shell32.dll und Shlwapi.dll Version 5,0 und höher. Die Anwendung kann keine Features implementieren, die nach Version 5,0 von Shell32.dll und Shlwapi.dll hinzugefügt wurden. |
| 0x0501  | Die Anwendung ist kompatibel mit Shell32.dll und Shlwapi.dll Version 5,0 und höher. Die Anwendung kann keine Features implementieren, die nach Version 5,0 von Shell32.dll und Shlwapi.dll hinzugefügt wurden. |
| 0x0600 sein  | Die Anwendung ist kompatibel mit Shell32.dll und Shlwapi.dll Version 6,0 und höher. Die Anwendung kann keine Features implementieren, die nach Version 6,0 von Shell32.dll und Shlwapi.dll hinzugefügt wurden. |


Wenn Sie das **\_ Win32- \_ IE** -Makro nicht in Ihrem Projekt definieren, wird es automatisch als 0x0500 definiert. Wenn Sie einen anderen Wert definieren möchten, können Sie den Compilerdirektiven in ihrer Make-Datei Folgendes hinzufügen: Ersetzen Sie die gewünschte Versionsnummer für 0x0400.

```
/D _WIN32_IE=0x0400
```

Eine andere Methode ist das Hinzufügen einer Zeile ähnlich der folgenden in Ihrem Quellcode, bevor Sie die shellheaderdateien einschließen. Ersetzen Sie die gewünschte Versionsnummer für 0x0400.

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
