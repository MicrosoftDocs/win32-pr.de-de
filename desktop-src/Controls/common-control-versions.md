---
title: Allgemeine Steuerelementversionen
description: In diesem Thema werden die verfügbaren Versionen der Common Control-Bibliothek (ComCtl32.dll) aufgeführt. Es wird beschrieben, wie Sie die Version identifizieren, die ihre Anwendung verwendet, und wie Sie ihre Anwendung auf eine bestimmte Version ausdrungen.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423960"
---
# <a name="common-control-versions"></a>Allgemeine Steuerelementversionen

In diesem Thema werden die verfügbaren Versionen der Common Control-Bibliothek (ComCtl32.dll) aufgeführt. Es wird beschrieben, wie Sie die Version identifizieren, die ihre Anwendung verwendet, und wie Sie ihre Anwendung auf eine bestimmte Version ausdrungen.

Dieses Thema enthält folgende Abschnitte:

-   [Allgemeine Versionsnummern der Steuerelement-DLL](#common-control-dll-versions-numbers)
-   [Strukturgrößen für verschiedene allgemeine Steuerelementversionen](#structure-sizes-for-different-common-control-versions)
-   [Verwenden von DllGetVersion zum Bestimmen der Versionsnummer](#using-dllgetversion-to-determine-the-version-number)
-   [Projektversionen](#project-versions)
-   [Verwandte Themen](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Allgemeine Versionsnummern der Steuerelement-DLL

Unterstützung für allgemeine Steuerelemente wird von ComCtl32.dll bereitgestellt, die alle 32-Bit- und 64-Bit-Versionen von Windows enthalten. Jede aufeinander folgende Version der DLL unterstützt die Features und die API früherer Versionen und fügt neue Features hinzu.

Da verschiedene Versionen von ComCtl32.dll mit Internet Explorer verteilt wurden, ist die aktive Version manchmal anders als die im Lieferumfang des Betriebssystems enthaltene Version. Aus diesem Grund muss Ihre Anwendung direkt bestimmen, welche Version ComCtl32.dll vorhanden ist.

In der Referenzdokumentation zu allgemeinen Steuerelementen geben viele Programmierelemente eine unterstützte DLL-Mindestversionsnummer an. Diese Versionsnummer gibt an, dass das Programmierelement in dieser Version und in nachfolgenden Versionen der DLL implementiert ist, sofern nichts anderes angegeben ist. Wenn keine Versionsnummer angegeben wird, wird das Programmierelement in allen vorhandenen Versionen der DLL implementiert.

In der folgenden Tabelle werden die verschiedenen DLL-Versionen und deren Verteilung auf unterstützte Betriebssystemen beschrieben.



ComCtl32.dll

Version

Verteilungsplattform

5.81

Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5 und Microsoft Internet Explorer 6

5.82

Windows Server 2003, Windows Vista, Windows Server 2008 und Windows 7

6.0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 und Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Strukturgrößen für verschiedene allgemeine Steuerelementversionen

Fortlaufende Verbesserungen an allgemeinen Steuerelementen haben dazu geführt, dass viele der Strukturen erweitert werden müssen. Aus diesem Grund hat sich die Größe der Strukturen zwischen verschiedenen Versionen von Commctrl.h geändert. Da die meisten allgemeinen Steuerelementstrukturen eine Strukturgröße als einen der Parameter annehmen, kann eine Nachricht oder Funktion fehlschlagen, wenn die Größe nicht erkannt wird. Um dies zu beheben, wurden Strukturgrößenkonstanten definiert, um die Ausrichtung auf verschiedene Versionen von ComCtl32.dll zu unterstützen. In der folgenden Liste werden die Strukturgrößenkonstanten definiert.



|    Strukturgrößenkonstante                           |     Definition                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| HDITEM \_ \_ V1-GRÖßE              | Die Größe der [**HDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-hditema) in Version 4.0.                           |
| IMAGELISTDRAWPARAMS \_ \_ V3-GRÖßE | Die Größe der [**IMAGELISTDRAWPARAMS-Struktur**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) in Version 5.9. |
| LVCOLUMN \_ \_ V1-GRÖßE            | Die Größe der [**LVCOLUMN-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) in Version 4.0.                       |
| LVGROUP \_ \_ V5-GRÖßE             | Die Größe der [**LVGROUP-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) in Version 6.0.                         |
| LVHITTESTINFO \_ V1 \_ SIZE       | Die Größe der [**LVHITTESTINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) in Version 4.0.             |
| LVITEM \_ \_ V1-GRÖßE              | Die Größe der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) in Version 4.0.                           |
| LVITEM \_ V5 \_ SIZE              | Die Größe der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) in Version 6.0.                           |
| LVTILEINFO \_ V5 \_ SIZE          | Die Größe der [**LVTILEINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) in Version 6.0.                   |
| MCHITTESTINFO \_ \_ V1-GRÖßE       | Die Größe der [**MCHITTESTINFO-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) in Version 4.0.             |
| NMLVCUSTOMDRAW \_ V3 \_ SIZE      | Die Größe der [**NMLVCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) in Version 4.7.           |
| NMTTDISPINFO \_ V1 \_ SIZE        | Die Größe der [**NMTTDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) in Version 4.0.               |
| NMTVCUSTOMDRAW \_ V3 \_ SIZE      | Die Größe der [**NMTVCUSTOMDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) in Version 4.7.           |
| PROPSHEETHEADER \_ V1 \_ SIZE     | Die Größe der [**PROPSHEETHEADER-Struktur**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) in Version 4.0.         |
| PROPSHEETPAGE \_ V1 \_ SIZE       | Die Größe der [**PROPSHEETPAGE-Struktur**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) in Version 4.0.             |
| REBARBANDINFO \_ \_ V3-GRÖßE       | Die Größe der [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) in Version 4.7.             |
| REBARBANDINFO \_ \_ V6-GRÖßE       | Die Größe der [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) in Version 6.0.             |
| TTTOOLINFO \_ V1 \_ SIZE          | Die Größe der [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) in Version 4.0.                       |
| TTTOOLINFO \_ V2 \_ SIZE          | Die Größe der [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) in Version 4.7.                       |
| TTTOOLINFO \_ V3 \_ SIZE          | Die Größe der [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) in Version 6.0.                       |
| TVINSERTSTRUCT \_ V1 \_ SIZE      | Die Größe der [**TVINSERTSTRUCT-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) in Version 4.0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Ermitteln der Versionsnummer mithilfe von DllGetVersion

Die [**DllGetVersion-Funktion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) kann von einer Anwendung aufgerufen werden, um zu bestimmen, welche DLL-Version auf dem System vorhanden ist.

[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) gibt eine [**DLLVERSIONINFO2-Struktur**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) zurück. Zusätzlich zu den Informationen, die über [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo)bereitgestellt werden, stellt **DLLVERSIONINFO2** auch die Hotfixnummer bereit, mit der das neueste installierte Service Pack identifiziert wird. Dies bietet eine stabilere Möglichkeit zum Vergleichen von Versionsnummern. Da der erste Member von **DLLVERSIONINFO2** eine **DLLVERSIONINFO-Struktur** ist, ist die spätere -Struktur abwärtskompatibel.


Die folgende Beispielfunktion `GetVersion` lädt eine angegebene DLL und versucht, ihre [**DllGetVersion-Funktion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) aufzurufen. Bei Erfolg wird ein Makro verwendet, um die Haupt- und Nebenversionsnummern aus der [**DLLVERSIONINFO-Struktur**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) in ein **DWORD** zu packen, das an die aufrufende Anwendung zurückgegeben wird. Wenn die DLL **dllGetVersion** nicht exportiert, gibt die Funktion 0 (null) zurück. Sie können die Funktion ändern, um die Möglichkeit zu behandeln, **dass DllGetVersion** eine [**DLLVERSIONINFO2-Struktur zurückgibt.**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) Falls ja, verwenden Sie die Informationen im **ullVersion-Member** dieser **DLLVERSIONINFO2-Struktur,** um Versionen, Buildnummern und Service Pack-Releases zu vergleichen. Das [**MAKEDLLVERULL-Makro**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) vereinfacht die Aufgabe, diese Werte mit denen in **ullVersion zu vergleichen.**

> [!Note]  
> Die [**falsche Verwendung von LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Windows finden Sie in der **LoadLibrary-Dokumentation.**

 


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

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

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



Das folgende Codebeispiel zeigt, wie Sie mit testen können, ob ComCtl32.dll Version `GetVersion` 6.0 oder höher ist.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a>Projektversionen

Um sicherzustellen, dass Ihre Anwendung mit verschiedenen Zielversionen einer DLL-Datei kompatibel ist, sind Versionsmakros in den Headerdateien vorhanden. Diese Makros werden verwendet, um bestimmte Definitionen für verschiedene Versionen der DLL zu definieren, auszuschließen oder neu zu definieren. Eine [ausführliche Beschreibung dieser Makros](/windows/desktop/WinProg/using-the-windows-headers) finden Sie unter Verwenden der Windows-Header.

Der Makroname **\_ WIN32 \_ IE** befindet sich beispielsweise häufig in älteren Headern. Sie sind dafür verantwortlich, das Makro als Hexadezimalzahl zu definieren. Diese Versionsnummer definiert die Zielversion der Anwendung, die die DLL verwendet. Die folgende Tabelle zeigt die verfügbaren Versionsnummern und die Auswirkungen auf Ihre Anwendung.



| Version | BESCHREIBUNG                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | Die Anwendung ist mit ComCtl32.dll 4.70 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 4.70 hinzugefügt wurden. |
| 0x0400  | Die Anwendung ist mit ComCtl32.dll Version 4.71 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 4.71 hinzugefügt wurden. |
| 0x0401  | Die Anwendung ist mit ComCtl32.dll 4.72 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 4.72 hinzugefügt wurden. |
| 0x0500  | Die Anwendung ist mit ComCtl32.dll Version 5.80 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 5.80 hinzugefügt wurden. |
| 0x0501  | Die Anwendung ist mit ComCtl32.dll Version 5.81 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 5.81 hinzugefügt wurden. |
| 0x0600  | Die Anwendung ist mit ComCtl32.dll Version 6.0 und höher kompatibel. Die Anwendung kann keine Features implementieren, die nach Version 6.0 hinzugefügt wurden.   |



 

Wenn Sie das **\_ \_ WIN32-IE-Makro** in Ihrem Projekt nicht definieren, wird es automatisch als 0x0500 definiert. Um einen anderen Wert zu definieren, können Sie den Compilerdirektiven in Ihrer Make-Datei Folgendes hinzufügen: ersetzen Sie die gewünschte Versionsnummer für 0x0400.


```C++
/D _WIN32_IE=0x0400
```



Eine weitere Methode besteht darin, eine Zeile ähnlich der folgenden in Ihrem Quellcode hinzuzufügen, bevor Sie die Shell-Headerdateien einschließen. Ersetzen Sie 0x0400 durch die gewünschte Versionsnummer.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)
</dt> </dl>

 

 