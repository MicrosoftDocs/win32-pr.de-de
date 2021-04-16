---
description: Im folgenden finden Sie die dbghelp-Funktionen.
ms.assetid: 7b28f70b-2d97-4cc2-8064-dfb806f9cffa
title: Dbghelp-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db65e46fe407b26b1a6ec9ae3cb8d5d7301d5821
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524072"
---
# <a name="dbghelp-functions"></a>Dbghelp-Funktionen

Im folgenden finden Sie die dbghelp-Funktionen.

## <a name="general"></a>Allgemein

Im folgenden sind allgemeine Hilfsfunktionen aufgeführt:

<dl>

[**Enumdirtree**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[**Imagehlpapiversion**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[**Imagehlpapiversionex**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[**Makesuredirectoriypathist vorhanden**](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[**Searchtreeforfile**](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a>Debugger

Die Debugging-Dienstfunktionen sind die Funktionen, die am besten für die Verwendung durch einen Debugger oder den Debugcode in einer Anwendung geeignet sind. Diese Funktionen können gemeinsam mit den Symbol Handlerfunktionen verwendet werden, um die Verwendung zu vereinfachen.

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**Enumerateloadedmodulesex**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[**Finddebuginfofile**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[**Finddebuginfofileex**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[**Findexecutableimage**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[**Findexecutableimageex**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**Symsetpartwindow**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[**Undecoratesymbolname**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a>Bildzugriff

Die Bild Zugriffs Funktionen greifen auf die Daten in einem ausführbaren Image zu. Die-Funktionen bieten Zugriff auf hoher Ebene auf die Basis von Bildern und einen sehr spezifischen Zugriff auf die gängigsten Teile der Daten eines Bilds.

<dl>

[**Gettimestampforloadedlibrary**](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[**Fehler bei imagedirectoryentrytodata**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[**Imagedirectoriyentry"dataex"**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[**Imagenderader**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[**Imagervatosection**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[**Imagervatova**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a>Symbol Handler

Mit den Funktionen des [Symbol Handlers](symbol-handling.md) können Anwendungen einfach und portabel auf die symbolischen Debuginformationen eines Bilds zugreifen. Diese Funktionen sollten ausschließlich verwendet werden, um den Zugriff auf symbolische Informationen sicherzustellen. Dies ist erforderlich, da diese Funktionen die Anwendung vom Symbol Format isolieren.

<dl>

[**Symaddsourcestream**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[**Symaddsymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[**Symcleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[**Symdelta etesymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**Symenumlines**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[**Symenum Processes**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[**Symenzusourcefiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[**Symenum SourceLines**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[**Symenum Symbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[**Symen-symbolsforaddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[**Symenenumtypes**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[**Symenentypesbyname**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[**Symfinddebuginfofile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[**Symfindexecutableimage**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[**Symfindfileinpath**](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[**Symfromaddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[**Symfromindex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[**Symfromname**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[**Symfromtoken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetFileLineOffsets64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[**Symgethomedirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**Symgetomaps**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[**Symgetoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[**Symgetscope**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[**Symgetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[**Symgetsymbolfile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[**Symgettypeer FromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[**Symgettypeingefo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[**Symgettypeingefoex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[**Syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**Symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[**Symmatchfilename**](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[**Symmatchstring**](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[**Symnext**](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[**Symprev**](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[**Symaktumodulelist**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**Symsearch**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[**Symsetcontext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[**SYM-thomedirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[**Symabtoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[**Symsetscopefromaddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[**Symsetscopefromindex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[**Symsetsearchpath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a>Symbol Server

Der [Symbol Server](symbol-servers-and-symbol-stores.md) ermöglicht es Debuggern, die richtigen Symbol Dateien ohne Produktnamen, Releases oder Buildnummern automatisch abzurufen. Die folgenden Funktionen werden mit dem Symbol Server verwendet.

<dl>

[**Symsrvdelta Name**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[**Symsrvgetfileingedexes**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[**Symsrvgetfileindexinfo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[**Symsrvgetfileingedexstring**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[**Symsrvgetsupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[**Symsrvisstore**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[**Symsrvstorefile**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[**Symsrvstoresupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a>Minidump-Dateien im Benutzermodus

Die Minidump-Funktionen bieten eine Möglichkeit für Anwendungen, crashdump-Dateien zu erstellen, die eine nützliche Teilmenge des gesamten Prozess Kontexts enthalten. Dies wird als [Minidumpdatei](minidump-files.md)bezeichnet. Die folgenden Funktionen werden für Minidump-Dateien verwendet.

<dl>

[**Minidumpcallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**Minidumpreaddumpstream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a>Quellserver

Der [Quell Server](source-server-and-source-indexing.md) ermöglicht einem Client das Abrufen der exakten Version der Quelldateien, die zum Erstellen einer Anwendung verwendet wurden. Die folgenden Funktionen werden mit dem Quell Server verwendet.

-   [**Symgetsourcefile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [**Symenzusourcefiletokens**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [**Symenum SourceFile-SPROC**](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [**Symgetsourcefilefromtoken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [**Symgetsourcefiletoken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [**Symgetsourcevarfromtoken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a>Veraltete Funktionen

<dl>

[**Mapdebuginformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**Unmapdebuginformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



