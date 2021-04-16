---
description: Bei Bedarf wurde die DbgHelp-Bibliothek erweitert, um sowohl 32-als auch 64-Bit-Windows zu unterstützen.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Aktualisierte Plattformunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523667"
---
# <a name="updated-platform-support"></a>Aktualisierte Plattformunterstützung

Bei Bedarf wurde die DbgHelp-Bibliothek erweitert, um sowohl 32-als auch 64-Bit-Windows zu unterstützen. Die ursprünglichen Funktions-und Strukturdefinitionen befinden sich weiterhin in "dbghelp. h", aber es gibt auch aktualisierte Versionen dieser Definitionen, die mit 64-Bit-Fenstern kompatibel sind. Wenn Sie die aktualisierten Funktionen in Ihrem Code verwenden, können Sie für 32-und 64-Bit-Fenster kompiliert werden. Der Code ist auch effizienter, da die ursprünglichen Funktionen einfach die aktualisierten Funktionen aufzurufen, um die Arbeit auszuführen.

"Dbghelp. h" enthält beispielsweise Definitionen für **symunloadmodule** (ursprüngliche Funktion) und **SymUnloadModule64** (aktualisierte Funktion). Diese Definitionen sind nahezu identisch, verwenden jedoch unterschiedliche Typen für den *baseof* -Parameter. (**Symunloadmodule** verwendet den **DWORD** -Typ, während **SymUnloadModule64** den **DWORD64** -Typ verwendet.) Wenn Sie den Code für die Verwendung von **SymUnloadModule64** schreiben, kann er für 32-und 64-Bit-Fenster kompiliert werden. Der Code ist auch effizienter, als wenn er " **symunloadmodule**" aufruft.

Im folgenden finden Sie eine Liste der aktualisierten Funktionen:

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

Im folgenden finden Sie eine Liste der aktualisierten Strukturen:

<dl>

[**ADDRESS64**](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[**Zurück gestelltes imagehlp- \_ \_ Symbol \_ LOAD64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[**Imagehlp \_ SYMBOL64 duplizieren \_**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[**Imagehlp \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[**Imagehlp \_ MODULE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[**Imagehlp \_ SYMBOL64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[**KDHELP64**](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[**STACKFRAME64**](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



