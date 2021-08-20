---
description: Die folgenden Funktionen werden beim Debuggen verwendet.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Debugfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfafdf5a453d262e75c4ab87356cbe34cfbb8574b520d353de0e66057903087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162671"
---
# <a name="debugging-functions"></a>Debugfunktionen

Die folgenden Funktionen werden beim Debuggen verwendet.



| Funktion                                                           | Beschreibung                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Bestimmt, ob der angegebene Prozess gedebuggt wird.                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Ermöglicht es einem Debugger, einen Thread fortzusetzen, der zuvor ein Debugereignis gemeldet hat. |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Ermöglicht es einem Debugger, an einen aktiven Prozess anzufügen und ihn zu debuggen.                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Beendet das Debuggen des angegebenen Prozesses durch den Debugger.                            |
| [**Debugbreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Bewirkt, dass eine Breakpointausnahme im aktuellen Prozess auftritt.                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Bewirkt, dass eine Breakpointausnahme im angegebenen Prozess auftritt.                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Legt die Aktion fest, die ausgeführt werden soll, wenn der aufrufende Thread beendet wird.                      |
| [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Überträgt die Ausführungssteuerung an den Debugger.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Leert den Anweisungscache für den angegebenen Prozess.                            |
| [**Getthreadcontext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Ruft den Kontext des angegebenen Threads ab.                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Ruft einen Deskriptortabelleneintrag für den angegebenen Selektor und Thread ab.           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Bestimmt, ob der aufrufende Prozess von einem Debugger im Benutzermodus gedebuggt wird.   |
| [**Outputdebugstring**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Sendet eine Zeichenfolge zur Anzeige an den Debugger.                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Liest Daten aus einem Speicherbereich in einem angegebenen Prozess.                           |
| [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Legt den Kontext für den angegebenen Thread fest.                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Wartet, bis ein Debugereignis in einem Prozess auftritt, der gedebuggt wird.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Ruft den Kontext des angegebenen WOW64-Threads ab.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Ruft einen Deskriptortabelleneintrag für den angegebenen Selektor und wow64-Thread ab.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Legt den Kontext des angegebenen WOW64-Threads fest.                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Schreibt Daten in einen Speicherbereich in einem angegebenen Prozess.                            |



 

 

 
