---
description: Die OutputDebugString-Funktion sendet eine Zeichenfolge vom debuggten Prozess an den Debugger, indem ein Debug-Ereignis für das Debugger-Ereignis erzeugt wird \_ \_ \_ . Ein Prozess kann erkennen, ob er durch Aufrufen der isdebuggerpresent-Funktion gedebuggt wird.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Kommunikation mit dem Debugger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860582"
---
# <a name="communicating-with-the-debugger"></a><span data-ttu-id="123df-104">Kommunikation mit dem Debugger</span><span class="sxs-lookup"><span data-stu-id="123df-104">Communicating with the Debugger</span></span>

<span data-ttu-id="123df-105">Die [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) -Funktion sendet eine Zeichenfolge vom \_ debuggten Prozess an den Debugger, indem ein Debug-Ereignis für das Debugger-Ereignis erzeugt wird \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="123df-105">The [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) function sends a string from the process being debugged to the debugger by generating an OUTPUT\_DEBUG\_STRING\_EVENT debugging event.</span></span> <span data-ttu-id="123df-106">Ein Prozess kann erkennen, ob er durch Aufrufen der [**isdebuggerpresent-Funktion gedebuggt**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) wird.</span><span class="sxs-lookup"><span data-stu-id="123df-106">A process can detect whether it is being debugged by calling the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>

<span data-ttu-id="123df-107">Die [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) -Funktion verursacht eine breakpointausnahme im aktuellen Prozess.</span><span class="sxs-lookup"><span data-stu-id="123df-107">The [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function causes a breakpoint exception in the current process.</span></span> <span data-ttu-id="123df-108">Ein Haltepunkt ist eine Position in einem Programm, an der die Ausführung angehalten wird, damit der Entwickler den Code, die Variablen und die Registerwerte des Programms untersuchen und ggf. Änderungen vornehmen, die Ausführung fortsetzen oder die Ausführung beenden kann.</span><span class="sxs-lookup"><span data-stu-id="123df-108">A breakpoint is a location in a program where execution is stopped to allow the developer to examine the program's code, variables, and register values and, as necessary, to make changes, continue execution, or terminate execution.</span></span>

<span data-ttu-id="123df-109">Die Funktion [**fatalexit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) beendet den aktuellen Prozess und übergibt die Ausführungs Steuerung an den Debugger, aber im Gegensatz zu [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)wird keine Ausnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="123df-109">The [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) function terminates the current process and gives execution control to the debugger, but unlike [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), it does not generate an exception.</span></span> <span data-ttu-id="123df-110">Diese Funktion sollte nur als letztes Mittel verwendet werden, da Sie nicht immer den Arbeitsspeicher des Prozesses freigibt oder die Dateien schließt.</span><span class="sxs-lookup"><span data-stu-id="123df-110">This function should only be used as a last resort, because it does not always free the process's memory or close its files.</span></span>

 

 
