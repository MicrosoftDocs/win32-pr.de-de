---
description: Die folgenden Funktionen werden beim Debuggen verwendet.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Debugfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bf5f81b08e3a7b324f276fc1a7b5d256d40819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346620"
---
# <a name="debugging-functions"></a>Debugfunktionen

Die folgenden Funktionen werden beim Debuggen verwendet.



| Funktion                                                           | BESCHREIBUNG                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Checkremotedebugerpresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Bestimmt, ob der angegebene Prozess gedebuggt wird.                         |
| [**Continuedebugevent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Ermöglicht einem Debugger das Fortsetzen eines Threads, der zuvor ein Debugereignis gemeldet hat. |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Ermöglicht einem Debugger das Anfügen an einen aktiven Prozess und das Debuggen.                     |
| [**"Debug-activeprocessstoppt"**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Verhindert, dass der Debugger den angegebenen Prozess debuggt.                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Bewirkt, dass im aktuellen Prozess eine breakpointausnahme auftritt.                      |
| [**Debugbreakprozess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Bewirkt, dass im angegebenen Prozess eine breakpointausnahme auftritt.                    |
| [**Debug-processkillonexit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Legt die Aktion fest, die ausgeführt werden soll, wenn der aufrufende Thread beendet wird.                      |
| [**Fatalexit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Überträgt die Ausführungs Steuerung an den Debugger.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Leert den Anweisungs Cache für den angegebenen Prozess.                            |
| [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Ruft den Kontext des angegebenen Threads ab.                                      |
| [**Getthreadselector Entry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Ruft einen deskriptortabelleneintrag für den angegebenen Selektor und den angegebenen Thread ab.           |
| [**IsDebug-vorhanden**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Bestimmt, ob der aufrufende Prozess von einem Benutzermodusdebugger debuggt wird.   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Sendet eine Zeichenfolge zur Anzeige an den Debugger.                                         |
| [**"Read processmemory"**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Liest Daten aus einem Arbeitsspeicher Bereich in einem angegebenen Prozess.                           |
| [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Legt den Kontext für den angegebenen Thread fest.                                          |
| [**Waitfordebugevent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Wartet, bis ein Debugereignis in einem debuggten Prozess auftritt.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Ruft den Kontext des angegebenen WOW64-Threads ab.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Ruft einen deskriptortabelleneintrag für den angegebenen Selektor und WOW64 Thread ab.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Legt den Kontext des angegebenen WOW64-Threads fest.                                     |
| [**"Write processmemory"**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Schreibt Daten in einem angegebenen Prozess in einen Arbeitsspeicher Bereich.                            |



 

 

 
