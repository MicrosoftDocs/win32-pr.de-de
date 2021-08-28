---
description: Die folgenden Funktionen werden bei der Fehlerbehandlung verwendet.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Fehlerbehandlungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fdc25327bed4966336571c20580b0bfdc22b38858d3edad560359eaf0710e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912760"
---
# <a name="error-handling-functions"></a>Fehlerbehandlungsfunktionen

Die folgenden Funktionen werden bei der Fehlerbehandlung verwendet.



| Funktion                                                 | BESCHREIBUNG                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Beep**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Generiert einfache Töne auf dem Lautsprecher.                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Erfasst eine Stapelrückverfolgung, indem der Stapel hochläuft und die Informationen für jeden Frame aufgezeichnet werden.                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Zeigt ein Meldungsfeld an und beendet die Anwendung, wenn das Meldungsfeld geschlossen wird.                                         |
| [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Blinkt das angegebene Fenster einmal.                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Blinkt das angegebene Fenster.                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Formatiert eine Meldungszeichenfolge.                                                                                                     |
| [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Ruft den Fehlermodus für den aktuellen Prozess ab.                                                                             |
| [**Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Ruft den Codewert des letzten Fehlers des aufrufenden Threads ab.                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Ruft den Fehlermodus für den aufrufenden Thread ab.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Gibt einen Wellenformton wieder.                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Durchsucht die aktiven Funktionstabellen nach einem Eintrag, der dem angegebenen PC-Wert entspricht.                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Ruft den Systemfehlercode ab, der dem angegebenen NT-Fehlercode entspricht.                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Ruft die Basisadresse des Images ab, das den angegebenen PC-Wert enthält.                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Initiiert eine Entladung von Prozeduraufrufframes.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Initiiert eine Entladung von Prozeduraufrufframes.                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Initiiert eine Entladung von Prozeduraufrufframes.                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Ruft den Aufrufkontext der Funktion ab, die dem angegebenen Funktionskontext vorausgeht.                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Steuert, ob das System die angegebenen Typen schwerwiegender Fehler behandelt oder ob sie vom Prozess behandelt werden.       |
| [**Setlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Legt den Code für den letzten Fehler für den aufrufenden Thread fest.                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Legt den Code für den letzten Fehler für den aufrufenden Thread fest.                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Steuert, ob das System die angegebenen Typen schwerwiegender Fehler behandelt oder ob sie vom aufrufenden Thread behandelt werden. |



 

 

 
