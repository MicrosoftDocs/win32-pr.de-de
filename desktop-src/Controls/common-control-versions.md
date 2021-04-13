---
title: Allgemeine Steuerelement Versionen
description: In diesem Thema werden die verfügbaren Versionen der allgemeinen Steuerelement Bibliothek (ComCtl32.dll) aufgelistet. es wird beschrieben, wie Sie die Version identifizieren, die von der Anwendung verwendet wird, und es wird erläutert, wie Sie Ihre Anwendung für eine bestimmte Version ausrichten.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474703"
---
# <a name="common-control-versions"></a>Allgemeine Steuerelement Versionen

In diesem Thema werden die verfügbaren Versionen der allgemeinen Steuerelement Bibliothek (ComCtl32.dll) aufgelistet. es wird beschrieben, wie Sie die Version identifizieren, die von der Anwendung verwendet wird, und es wird erläutert, wie Sie Ihre Anwendung für eine bestimmte Version ausrichten.

Dieses Thema enthält folgende Abschnitte:

-   [Versions Nummern für allgemeine Steuerelement-dll](#common-control-dll-versions-numbers)
-   [Struktur Größen für verschiedene allgemeine Steuerelement Versionen](#structure-sizes-for-different-common-control-versions)
-   [Verwenden von dllgetversion zum Ermitteln der Versionsnummer](#using-dllgetversion-to-determine-the-version-number)
-   [Projekt Versionen](#project-versions)
-   [Zugehörige Themen](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Versions Nummern für allgemeine Steuerelement-dll

Die Unterstützung für allgemeine Steuerelemente wird von ComCtl32.dll bereitgestellt, die alle 32-Bit-und 64-Bit-Versionen von Windows enthalten. Jede aufeinander folgende Version der DLL unterstützt die Features und API früherer Versionen und fügt neue Funktionen hinzu.

Da verschiedene Versionen von ComCtl32.dll mit Internet Explorer verteilt wurden, unterscheidet sich die aktive Version manchmal von der Version, die mit dem Betriebssystem ausgeliefert wurde. Daher muss Ihre Anwendung direkt ermitteln, welche Version von ComCtl32.dll vorhanden ist.

In der Referenz Dokumentation zu allgemeinen Steuerelementen geben viele Programmier Elemente eine unterstützte dll-Versionsnummer an. Diese Versionsnummer gibt an, dass das Programmier Element in dieser Version und in nachfolgenden Versionen der dll implementiert ist, sofern nicht anders angegeben. Wenn keine Versionsnummer angegeben ist, wird das Programmier Element in allen vorhandenen Versionen der dll implementiert.

In der folgenden Tabelle werden die verschiedenen dll-Versionen und deren Verteilung auf unterstützte Betriebssysteme beschrieben.



ComCtl32.dll

Version

Verteilungs Plattform

5,81

Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 und Microsoft Internet Explorer 6

5,82

Windows Server 2003, Windows Vista, Windows Server 2008 und Windows 7

6.0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 und Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Struktur Größen für verschiedene allgemeine Steuerelement Versionen

Fortlaufende Verbesserungen an allgemeinen Steuerelementen haben dazu geführt, dass viele der Strukturen erweitert werden müssen. Aus diesem Grund hat sich die Größe der Strukturen zwischen den verschiedenen Versionen von "kommctrl. h" geändert. Da die meisten der allgemeinen Steuerelement Strukturen eine Struktur Größe als einen der Parameter annehmen, kann eine Nachricht oder Funktion fehlschlagen, wenn die Größe nicht erkannt wird. Um dieses Problem zu beheben, wurden strukturgrößenkonstanten definiert, um das Ziel einer anderen Version von ComCtl32.dll zu unterstützen. In der folgenden Liste sind die Konstanten für die Struktur Größe definiert.



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| HDITEM \_ v1- \_ Größe              | Die Größe der [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur in Version 4,0.                           |
| Imagelistdrawparameams \_ V3- \_ Größe | Die Größe der [**imagelistdrawparameams**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) -Struktur in Version 5,9. |
| Größe von Pipeline Column \_ v1 \_            | Die Größe der [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur in Version 4,0.                       |
| Größe der \_ \_ Größe der Größe der Größe             | Die Größe der Struktur von " [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) " in Version 6,0.                         |
| Größe von "lvhittestinfo \_ v1" \_       | Die Größe der " [**lvhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) "-Struktur in Version 4,0.             |
| Lvitem \_ v1- \_ Größe              | Die Größe der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur in Version 4,0.                           |
| Lvitem \_ V5- \_ Größe              | Die Größe der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur in Version 6,0.                           |
| Größe von "lvtileinfo \_ V5" \_          | Die Größe der " [**lvtileinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) "-Struktur in Version 6,0.                   |
| MCHITTESTINFO \_ v1- \_ Größe       | Die Größe der [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) -Struktur in Version 4,0.             |
| Nmlvcustomdraw \_ V3- \_ Größe      | Die Größe der [**nmlvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) -Struktur in Version 4,7.           |
| Nmttdispinfo \_ v1- \_ Größe        | Die Größe der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur in Version 4,0.               |
| Nmtvcustomdraw \_ V3- \_ Größe      | Die Größe der [**nmtvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) -Struktur in Version 4,7.           |
| Propsheeteader \_ v1- \_ Größe     | Die Größe der [**propsheeteader**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) -Struktur in Version 4,0.         |
| PROPSHEETPAGE \_ v1- \_ Größe       | Die Größe der [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) -Struktur in Version 4,0.             |
| REBARBANDINFO \_ V3- \_ Größe       | Die Größe der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur in Version 4,7.             |
| REBARBANDINFO \_ V6- \_ Größe       | Die Größe der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur in Version 6,0.             |
| Tttoolinfo \_ v1- \_ Größe          | Die Größe der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur in Version 4,0.                       |
| Tttoolinfo \_ v2- \_ Größe          | Die Größe der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur in Version 4,7.                       |
| Tttoolinfo \_ V3- \_ Größe          | Die Größe der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur in Version 6,0.                       |
| TVINSERTSTRUCT \_ v1- \_ Größe      | Die Größe der [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) -Struktur in Version 4,0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Verwenden von dllgetversion zum Ermitteln der Versionsnummer

Die [**dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) -Funktion kann von einer Anwendung aufgerufen werden, um zu bestimmen, welche DLL-Version auf dem System vorhanden ist.

[**Dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) gibt eine [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurück. Zusätzlich zu den Informationen, die über [**dllversioninfo**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo)bereitgestellt werden, stellt **DLLVERSIONINFO2** auch die Hotfixnummer bereit, mit der die neuesten installierten Service Pack identifiziert werden, die eine stabilere Möglichkeit zum Vergleichen von Versionsnummern bietet. Da der erste Member von **DLLVERSIONINFO2** eine **dllversioninfo** -Struktur ist, ist die spätere Struktur abwärts kompatibel.


Die folgende Beispiel Funktion `GetVersion` lädt eine angegebene DLL und versucht, Ihre [**dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) -Funktion aufzurufen. Wenn erfolgreich, wird ein Makro verwendet, um die Haupt-und neben Versionsnummern aus der [**dllversioninfo**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) -Struktur in ein **DWORD** zu packen, das an die aufrufenden Anwendung zurückgegeben wird. Wenn die DLL **dllgetversion** nicht exportiert, gibt die Funktion 0 (null) zurück. Sie können die-Funktion ändern, um die Möglichkeit zu behandeln, dass **dllgetversion** eine [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) -Struktur zurückgibt. Wenn dies der Fall ist, verwenden Sie die Informationen im **ullversion** -Member der **DLLVERSIONINFO2** -Struktur, um Versionen, Buildnummern und Service Pack Releases zu vergleichen. Das [**makedllverull**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) -Makro vereinfacht die Aufgabe, diese Werte mit den Werten in **ullversion** zu vergleichen.

> [!Note]  
> Das nicht ordnungsgemäße Verwenden von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann Sicherheitsrisiken darstellen. Informationen zum ordnungsgemäßen Laden von DLLs mit unterschiedlichen Versionen von Windows finden Sie in der Dokumentation zu **LoadLibrary** .

 


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



Im folgenden Codebeispiel wird veranschaulicht, wie Sie `GetVersion` mit überprüfen können, ob ComCtl32.dll die Version 6,0 oder höher ist.


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



## <a name="project-versions"></a>Projekt Versionen

Um sicherzustellen, dass Ihre Anwendung mit unterschiedlichen Ziel Versionen einer DLL-Datei kompatibel ist, sind Versions Makros in den Header Dateien vorhanden. Diese Makros werden verwendet, um bestimmte Definitionen für verschiedene Versionen der dll zu definieren, auszuschließen oder neu zu definieren. Eine ausführliche Beschreibung dieser Makros finden [Sie unter Verwenden der Windows-Header](/windows/desktop/WinProg/using-the-windows-headers) .

Beispielsweise befindet sich der Makro Name **\_ Win32 \_ IE** häufig in älteren Headern. Sie sind dafür verantwortlich, das Makro als hexadezimale Zahl zu definieren. Diese Versionsnummer definiert die Zielversion der Anwendung, die die dll verwendet. In der folgenden Tabelle sind die verfügbaren Versionsnummern und die Auswirkungen der einzelnen Anwendungen aufgeführt.



| Version | BESCHREIBUNG                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | Die Anwendung ist kompatibel mit ComCtl32.dll Version 4,70 und höher. Die Anwendung kann keine Features implementieren, die nach Version 4,70 hinzugefügt wurden. |
| 0x0400  | Die Anwendung ist kompatibel mit ComCtl32.dll Version 4,71 und höher. Die Anwendung kann keine Features implementieren, die nach Version 4,71 hinzugefügt wurden. |
| 0x0401  | Die Anwendung ist kompatibel mit ComCtl32.dll Version 4,72 und höher. Die Anwendung kann keine Features implementieren, die nach Version 4,72 hinzugefügt wurden. |
| 0x0500 sein  | Die Anwendung ist kompatibel mit ComCtl32.dll Version 5,80 und höher. Die Anwendung kann keine Features implementieren, die nach Version 5,80 hinzugefügt wurden. |
| 0x0501  | Die Anwendung ist kompatibel mit ComCtl32.dll Version 5,81 und höher. Die Anwendung kann keine Features implementieren, die nach Version 5,81 hinzugefügt wurden. |
| 0x0600 sein  | Die Anwendung ist kompatibel mit ComCtl32.dll Version 6,0 und höher. Die Anwendung kann keine Features implementieren, die nach Version 6,0 hinzugefügt wurden.   |



 

Wenn Sie das **\_ Win32- \_ IE** -Makro nicht in Ihrem Projekt definieren, wird es automatisch als 0x0500 definiert. Wenn Sie einen anderen Wert definieren möchten, können Sie den Compilerdirektiven in ihrer Make-Datei Folgendes hinzufügen: Ersetzen Sie die gewünschte Versionsnummer für 0x0400.


```C++
/D _WIN32_IE=0x0400
```



Eine andere Methode ist das Hinzufügen einer Zeile ähnlich der folgenden in Ihrem Quellcode, bevor Sie die shellheaderdateien einschließen. Ersetzen Sie die gewünschte Versionsnummer für 0x0400.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)
</dt> </dl>

 

 