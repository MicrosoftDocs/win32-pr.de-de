---
description: Der Debugger verwendet die WaitForDebugEvent-Funktion am Anfang seiner Hauptschleife.
ms.assetid: 5a45854e-2711-49d5-982b-6b85248ec632
title: Schreiben der Hauptschleife des Debuggers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6695488e6391fa83a7d8aea999487beaae30360786872e3c345d52c201494cc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103890"
---
# <a name="writing-the-debuggers-main-loop"></a>Schreiben der Hauptschleife des Debuggers

Der Debugger verwendet die [**WaitForDebugEvent-Funktion**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) am Anfang seiner Hauptschleife. Diese Funktion blockiert den Debugger, bis ein Debugereignis auftritt. Wenn das Debugereignis auftritt, setzt das System alle Threads im Prozess an, der gedebuggt wird, und benachrichtigt den Debugger über das Ereignis.

Der Debugger kann mit dem Benutzer interagieren oder den Zustand des zu debuggenden Prozesses ändern, indem er die Funktionen [**GetThreadContext,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) [**GetThreadSelectorEntry,**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry) [**ReadProcessMemory,**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)und [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) verwendet. **GetThreadSelectorEntry gibt** den Deskriptortabelleneintrag für einen angegebenen Selektor und Thread zurück. Debugger verwenden den Deskriptortabelleneintrag, um eine segment relative Adresse in eine lineare virtuelle Adresse zu konvertieren. Die **Funktionen ReadProcessMemory** **und WriteProcessMemory** erfordern lineare virtuelle Adressen.

Debugger lesen häufig den Arbeitsspeicher des zu debuggenden Prozesses und schreiben den Arbeitsspeicher, der Anweisungen enthält, in den Anweisungscache. Nachdem die Anweisungen geschrieben wurden, ruft der Debugger die [**FlushInstructionCache-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache) auf, um die zwischengespeicherten Anweisungen auszuführen.

Der Debugger verwendet die [**ContinueDebugEvent-Funktion**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) am Ende seiner Hauptschleife. Mit dieser Funktion kann der Prozess, der gedebuggt wird, weiterhin ausgeführt werden.

Im folgenden Beispiel werden die [**Funktionen WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) und [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) verwendet, um zu veranschaulichen, wie ein einfacher Debugger organisiert werden kann.


```C++
#include <windows.h>

DWORD OnCreateThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnCreateProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnLoadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnUnloadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnOutputDebugStringEvent(const LPDEBUG_EVENT);
DWORD OnRipEvent(const LPDEBUG_EVENT);

void EnterDebugLoop(const LPDEBUG_EVENT DebugEv)
{
   DWORD dwContinueStatus = DBG_CONTINUE; // exception continuation 
 
   for(;;) 
   { 
   // Wait for a debugging event to occur. The second parameter indicates
   // that the function does not return until a debugging event occurs. 
 
      WaitForDebugEvent(DebugEv, INFINITE); 

   // Process the debugging event code. 
 
      switch (DebugEv->dwDebugEventCode) 
      { 
         case EXCEPTION_DEBUG_EVENT: 
         // Process the exception code. When handling 
         // exceptions, remember to set the continuation 
         // status parameter (dwContinueStatus). This value 
         // is used by the ContinueDebugEvent function. 
 
            switch(DebugEv->u.Exception.ExceptionRecord.ExceptionCode)
            { 
               case EXCEPTION_ACCESS_VIOLATION: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_BREAKPOINT: 
               // First chance: Display the current 
               // instruction and register values. 
                  break;
 
               case EXCEPTION_DATATYPE_MISALIGNMENT: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_SINGLE_STEP: 
               // First chance: Update the display of the 
               // current instruction and register values. 
                  break;
 
               case DBG_CONTROL_C: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               default:
               // Handle other exceptions. 
                  break;
            } 

            break;
 
         case CREATE_THREAD_DEBUG_EVENT: 
         // As needed, examine or change the thread's registers 
         // with the GetThreadContext and SetThreadContext functions; 
         // and suspend and resume thread execution with the 
         // SuspendThread and ResumeThread functions. 

            dwContinueStatus = OnCreateThreadDebugEvent(DebugEv);
            break;

         case CREATE_PROCESS_DEBUG_EVENT: 
         // As needed, examine or change the registers of the
         // process's initial thread with the GetThreadContext and
         // SetThreadContext functions; read from and write to the
         // process's virtual memory with the ReadProcessMemory and
         // WriteProcessMemory functions; and suspend and resume
         // thread execution with the SuspendThread and ResumeThread
         // functions. Be sure to close the handle to the process image
         // file with CloseHandle.

            dwContinueStatus = OnCreateProcessDebugEvent(DebugEv);
            break;
 
         case EXIT_THREAD_DEBUG_EVENT: 
         // Display the thread's exit code. 

            dwContinueStatus = OnExitThreadDebugEvent(DebugEv);
            break;
 
         case EXIT_PROCESS_DEBUG_EVENT: 
         // Display the process's exit code. 

            dwContinueStatus = OnExitProcessDebugEvent(DebugEv);
            break;
 
         case LOAD_DLL_DEBUG_EVENT: 
         // Read the debugging information included in the newly 
         // loaded DLL. Be sure to close the handle to the loaded DLL 
         // with CloseHandle.

            dwContinueStatus = OnLoadDllDebugEvent(DebugEv);
            break;
 
         case UNLOAD_DLL_DEBUG_EVENT: 
         // Display a message that the DLL has been unloaded. 

            dwContinueStatus = OnUnloadDllDebugEvent(DebugEv);
            break;
 
         case OUTPUT_DEBUG_STRING_EVENT: 
         // Display the output debugging string. 

            dwContinueStatus = OnOutputDebugStringEvent(DebugEv);
            break;

         case RIP_EVENT:
            dwContinueStatus = OnRipEvent(DebugEv);
            break;
      } 
 
   // Resume executing the thread that reported the debugging event. 
 
   ContinueDebugEvent(DebugEv->dwProcessId, 
                      DebugEv->dwThreadId, 
                      dwContinueStatus);
   }
}
```



 

 
