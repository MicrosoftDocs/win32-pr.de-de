---
description: Der folgende Code zeigt, wie ausführliche Statusinformationen vom Symbol Handler zum Suchen und Laden von Modulen und den entsprechenden Symbol Dateien abgerufen und gemeldet werden.
ms.assetid: 1dd8af0e-280b-4fc4-bf75-45c5c7517365
title: Abrufen von Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebaed2683f329fa267bdc926063d0b763190400
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214288"
---
# <a name="getting-notifications"></a>Abrufen von Benachrichtigungen

Der folgende Code zeigt, wie ausführliche Statusinformationen vom Symbol Handler zum Suchen und Laden von Modulen und den entsprechenden Symbol Dateien abgerufen und gemeldet werden.

Viele, die mit dem WinDbg-Debugger vertraut sind, können sich einen Befehl mit dem Namen "! SYM noisy" merken. Dieser Befehl wird vom Benutzer verwendet, um zu bestimmen, warum WinDbg Symbol Dateien nicht laden kann oder nicht. Es wird eine ausführliche Liste aller Elemente angezeigt, die der Symbol Handler ausprobiert.

Dieselbe Auflistung ist auch für alle Benutzer verfügbar, die einen Client für den dbghelp-Symbol Handler entwickeln.

Nennen Sie zunächst [**SYM-toptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) mit **symopt \_ Debug**. Dies bewirkt, dass dbghelp debugbenachrichtigungen aktiviert.

Verwenden Sie nach dem Aufrufen von [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) , um eine Rückruffunktion zu registrieren, die von dbghelp aufgerufen wird, wenn ein interessantes Ereignis auftritt. In diesem Beispiel wird die Rückruffunktion als [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback)bezeichnet. Symbol Rückruf Funktionen wird eine Reihe von Aktionscodes an Sie übermittelt, die Sie je nach Typ verarbeiten können. In diesem Beispiel wird nur der Code für die **CBA- \_ Ereignis** Aktion behandelt. Diese Funktion übergibt eine Zeichenfolge, die ausführliche Informationen zu einem Ereignis enthält, das beim Laden eines Symbols aufgetreten ist. Dieses Ereignis könnte von einem Versuch sein, die Daten in einem ausführbaren Image an den erfolgreichen Speicherort einer Symbol Datei zu lesen. **SymRegisterCallbackProc64** zeigt diese Zeichenfolge an und gibt **true** zurück.

> [!IMPORTANT]
> Stellen Sie sicher, dass Sie für jeden Aktions Code, den Sie nicht verarbeiten, **false** zurückgeben. andernfalls kann es zu undefiniertem Verhalten kommen. Eine Liste aller Aktionscodes und ihrer Implikationen finden Sie unter [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) .

 

Nachdem der Rückruf registriert wurde, ist es an der Zeit, das in der Befehlszeile angegebene Modul durch Aufrufen von [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)zu laden.

Nennen Sie schließlich " [**symcleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) " vor dem beenden.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#ifdef UNICODE
 #define DBGHELP_TRANSLATE_TCHAR
#endif
#include <dbghelp.h>

// Here is an implementation of a Symbol Callback function.

BOOL 
CALLBACK 
SymRegisterCallbackProc64(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt ULONG64 CallbackData,
    __in_opt ULONG64 UserContext
    )
{
    UNREFERENCED_PARAMETER(hProcess);
    UNREFERENCED_PARAMETER(UserContext);
    
    PIMAGEHLP_CBA_EVENT evt;

    // If SYMOPT_DEBUG is set, then the symbol handler will pass
    // verbose information on its attempt to load symbols.
    // This information be delivered as text strings.
    
    switch (ActionCode)
    {
    case CBA_EVENT:
        evt = (PIMAGEHLP_CBA_EVENT)CallbackData;
        _tprintf(_T("%s"), (PTSTR)evt->desc);
        break;

    // CBA_DEBUG_INFO is the old ActionCode for symbol spew.
    // It still works, but we use CBA_EVENT in this example.
#if 0
    case CBA_DEBUG_INFO:
        _tprintf(_T("%s"), (PTSTR)CallbackData);
        break;
#endif

    default:
        // Return false to any ActionCode we don't handle
        // or we could generate some undesirable behavior.
        return FALSE;
    }

    return TRUE;
}

// Main code.

int __cdecl
#ifdef UNICODE
_tmain(
#else
main(
#endif
    __in int argc,
    __in_ecount(argc) PCTSTR argv[]
    )
{
    BOOL status;
    int rc = -1;
    HANDLE hProcess;
    DWORD64 module;
    
    if (argc < 2)
    {
        _tprintf(_T("You must specify an executable image to load.\n"));
        return rc;
    }

    // If we want to se debug spew, we need to set this option.
        
    SymSetOptions(SYMOPT_DEBUG);
    
    // We are not debugging an actual process, so lets use a placeholder
    // value of 1 for hProcess just to ID these calls from any other
    // series we may want to load.  For this simple case, anything will do.
    
    hProcess = (HANDLE)1;
    
    // Initialize the symbol handler.  No symbol path.  
    // Just let dbghelp use _NT_SYMBOL_PATH
    
    status = SymInitialize(hProcess, NULL, false);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymInitialize.\n"), GetLastError());
        return rc;
    }
     
    // Now register our callback.
    
    status = SymRegisterCallback64(hProcess, SymRegisterCallbackProc64, NULL);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymRegisterCallback64.\n"), GetLastError());
        goto cleanup;
    }
    
    // Go ahead and load a module for testing.
    
    module = SymLoadModuleEx(hProcess,  // our unique id
                             NULL,      // no open file handle to image
                             argv[1],   // name of image to load
                             NULL,      // no module name - dbghelp will get it
                             0,         // no base address - dbghelp will get it
                             0,         // no module size - dbghelp will get it
                             NULL,      // no special MODLOAD_DATA structure
                             0);        // flags
    if (!module)
    {
        _tprintf(_T("Error 0x%x calling SymLoadModuleEx.\n"), GetLastError());
        goto cleanup;
    }
    rc = 0;
    
cleanup:
    SymCleanup(hProcess);
    
    return rc;    
}
```



Die Angabe von **null** als zweiten Parameter von [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) gibt an, dass der Symbol Handler den Standard Suchpfad verwenden soll, um Symbol Dateien zu suchen. Ausführliche Informationen dazu, wie der Symbol Handler Symbol Dateien sucht oder wie eine Anwendung einen Symbol Suchpfad angeben kann, finden Sie unter [Symbol Pfade](symbol-paths.md).

Das Ausführen dieses Programms zeigt, wie der Symbol Pfad verarbeitet wird. Da dbghelp den Symbol Pfad zum Suchen der Symbol Datei durchsucht, ruft er wiederholt [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) auf, die wiederum die folgenden Zeichen folgen anzeigt, die von dbghelp übermittelt werden.

``` syntax
d:\load.exe c:\home\dbghelp.dll
DBGHELP: No header for c:\home\dbghelp.dll.  Searching for image on disk
DBGHELP: c:\home\dbghelp.dll - OK
DBGHELP: .\dbghelp.pdb - file not found
DBGHELP: .\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\symbols\dll\dbghelp.pdb - file not found
DBGHELP: d:\nt.binaries.amd64chk\symbols.pri\dbg\dbghelp.pdb - file not found
DBGHELP: dbghelp - private symbols & lines
         dbghelp.pdb
```

 

 



