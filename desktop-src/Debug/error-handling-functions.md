---
description: Die folgenden Funktionen werden bei der Fehlerbehandlung verwendet.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Fehlerbehandlungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4cea391f05638310e17b9ef283e138204bc2cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125726"
---
# <a name="error-handling-functions"></a>Fehlerbehandlungsfunktionen

Die folgenden Funktionen werden bei der Fehlerbehandlung verwendet.



| Funktion                                                 | BESCHREIBUNG                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Signal Tons**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Generiert einfache Töne auf dem Redner.                                                                                        |
| [**Capturestackbacktrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Erfasst eine Stapel Rückverfolgung, indem der Stapel nach oben durchlaufen und die Informationen für die einzelnen Frames aufgezeichnet werden.                             |
| [**Fatalappexit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Zeigt ein Meldungs Feld an und beendet die Anwendung, wenn das Meldungs Feld geschlossen wird.                                         |
| [**Flash Fenster**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Blinkt das angegebene Fenster ein Mal.                                                                                        |
| [**Flash windowex**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Blinkt das angegebene Fenster.                                                                                                 |
| [**Format Message**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Formatiert eine Nachrichten Zeichenfolge.                                                                                                     |
| [**Geterrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Ruft den Fehler Modus für den aktuellen Prozess ab.                                                                             |
| [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Ruft den letzten Fehler Codewert des aufrufenden Threads ab.                                                                         |
| [**Getthreaderrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Ruft den Fehler Modus für den aufrufenden Thread ab.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Gibt einen Wellenform-Sound wieder.                                                                                                       |
| [**Rtllookupfunctionentry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Durchsucht die aktiven Funktionstabellen nach einem Eintrag, der dem angegebenen PC-Wert entspricht.                                  |
| [**Rtlntstatustodoserror**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Ruft den Systemfehler Code ab, der dem angegebenen NT-Fehlercode entspricht.                                              |
| [**Rtlpcto Fileheader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Ruft die Basisadresse des Bilds ab, das den angegebenen PC-Wert enthält.                                                 |
| [**Rtlunwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Initiiert eine Entladung von Prozedur Aufrufframes.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Initiiert eine Entladung von Prozedur Aufrufframes.                                                                                 |
| [**Rtlunwindex**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Initiiert eine Entladung von Prozedur Aufrufframes.                                                                                 |
| [**Rtlvirtualentladen**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Ruft den Aufruf Kontext der Funktion ab, die dem angegebenen Funktions Kontext vorangestellt ist.                                |
| [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Steuert, ob das System die angegebenen Typen von schwerwiegenden Fehlern behandelt oder ob der Prozess Sie behandelt.       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Legt den letzten Fehlercode für den aufrufenden Thread fest.                                                                              |
| [**Setlasterrorex**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Legt den letzten Fehlercode für den aufrufenden Thread fest.                                                                              |
| [**Setthreaderrormode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Steuert, ob das System die angegebenen Typen von schwerwiegenden Fehlern behandelt oder ob der aufrufende Thread diese behandelt. |



 

 

 
