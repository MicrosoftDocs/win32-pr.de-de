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
# <a name="dbghelp-functions"></a><span data-ttu-id="fe5f0-103">Dbghelp-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fe5f0-103">DbgHelp Functions</span></span>

<span data-ttu-id="fe5f0-104">Im folgenden finden Sie die dbghelp-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-104">The following are the DbgHelp functions.</span></span>

## <a name="general"></a><span data-ttu-id="fe5f0-105">Allgemein</span><span class="sxs-lookup"><span data-stu-id="fe5f0-105">General</span></span>

<span data-ttu-id="fe5f0-106">Im folgenden sind allgemeine Hilfsfunktionen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="fe5f0-106">The following are general helper functions:</span></span>

<dl>

[<span data-ttu-id="fe5f0-107">**Enumdirtree**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-107">**EnumDirTree**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[<span data-ttu-id="fe5f0-108">**Imagehlpapiversion**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-108">**ImagehlpApiVersion**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[<span data-ttu-id="fe5f0-109">**Imagehlpapiversionex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-109">**ImagehlpApiVersionEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[<span data-ttu-id="fe5f0-110">**Makesuredirectoriypathist vorhanden**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-110">**MakeSureDirectoryPathExists**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[<span data-ttu-id="fe5f0-111">**Searchtreeforfile**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-111">**SearchTreeForFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a><span data-ttu-id="fe5f0-112">Debugger</span><span class="sxs-lookup"><span data-stu-id="fe5f0-112">Debugger</span></span>

<span data-ttu-id="fe5f0-113">Die Debugging-Dienstfunktionen sind die Funktionen, die am besten für die Verwendung durch einen Debugger oder den Debugcode in einer Anwendung geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-113">The debugging service functions are the functions most suited for use by a debugger or the debugging code in an application.</span></span> <span data-ttu-id="fe5f0-114">Diese Funktionen können gemeinsam mit den Symbol Handlerfunktionen verwendet werden, um die Verwendung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-114">These functions can be used in concert with the symbol handler functions for easier use.</span></span>

<dl>

[<span data-ttu-id="fe5f0-115">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-115">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="fe5f0-116">**Enumerateloadedmodulesex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-116">**EnumerateLoadedModulesEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[<span data-ttu-id="fe5f0-117">**Finddebuginfofile**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-117">**FindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[<span data-ttu-id="fe5f0-118">**Finddebuginfofileex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-118">**FindDebugInfoFileEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[<span data-ttu-id="fe5f0-119">**Findexecutableimage**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-119">**FindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[<span data-ttu-id="fe5f0-120">**Findexecutableimageex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-120">**FindExecutableImageEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[<span data-ttu-id="fe5f0-121">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-121">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="fe5f0-122">**Symsetpartwindow**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-122">**SymSetParentWindow**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[<span data-ttu-id="fe5f0-123">**Undecoratesymbolname**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-123">**UnDecorateSymbolName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a><span data-ttu-id="fe5f0-124">Bildzugriff</span><span class="sxs-lookup"><span data-stu-id="fe5f0-124">Image Access</span></span>

<span data-ttu-id="fe5f0-125">Die Bild Zugriffs Funktionen greifen auf die Daten in einem ausführbaren Image zu.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-125">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="fe5f0-126">Die-Funktionen bieten Zugriff auf hoher Ebene auf die Basis von Bildern und einen sehr spezifischen Zugriff auf die gängigsten Teile der Daten eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-126">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="fe5f0-127">**Gettimestampforloadedlibrary**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-127">**GetTimestampForLoadedLibrary**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[<span data-ttu-id="fe5f0-128">**Fehler bei imagedirectoryentrytodata**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-128">**ImageDirectoryEntryToData**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[<span data-ttu-id="fe5f0-129">**Imagedirectoriyentry"dataex"**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-129">**ImageDirectoryEntryToDataEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[<span data-ttu-id="fe5f0-130">**Imagenderader**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-130">**ImageNtHeader**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[<span data-ttu-id="fe5f0-131">**Imagervatosection**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-131">**ImageRvaToSection**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[<span data-ttu-id="fe5f0-132">**Imagervatova**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-132">**ImageRvaToVa**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a><span data-ttu-id="fe5f0-133">Symbol Handler</span><span class="sxs-lookup"><span data-stu-id="fe5f0-133">Symbol Handler</span></span>

<span data-ttu-id="fe5f0-134">Mit den Funktionen des [Symbol Handlers](symbol-handling.md) können Anwendungen einfach und portabel auf die symbolischen Debuginformationen eines Bilds zugreifen.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-134">The [symbol handler](symbol-handling.md) functions give applications easy and portable access to the symbolic debugging information of an image.</span></span> <span data-ttu-id="fe5f0-135">Diese Funktionen sollten ausschließlich verwendet werden, um den Zugriff auf symbolische Informationen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-135">These functions should be used exclusively to ensure access to symbolic information.</span></span> <span data-ttu-id="fe5f0-136">Dies ist erforderlich, da diese Funktionen die Anwendung vom Symbol Format isolieren.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-136">This is necessary because these functions isolate the application from the symbol format.</span></span>

<dl>

[<span data-ttu-id="fe5f0-137">**Symaddsourcestream**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-137">**SymAddSourceStream**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[<span data-ttu-id="fe5f0-138">**Symaddsymbol**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-138">**SymAddSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[<span data-ttu-id="fe5f0-139">**Symcleanup**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-139">**SymCleanup**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[<span data-ttu-id="fe5f0-140">**Symdelta etesymbol**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-140">**SymDeleteSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[<span data-ttu-id="fe5f0-141">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-141">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="fe5f0-142">**Symenumlines**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-142">**SymEnumLines**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[<span data-ttu-id="fe5f0-143">**Symenum Processes**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-143">**SymEnumProcesses**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[<span data-ttu-id="fe5f0-144">**Symenzusourcefiles**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-144">**SymEnumSourceFiles**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[<span data-ttu-id="fe5f0-145">**Symenum SourceLines**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-145">**SymEnumSourceLines**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[<span data-ttu-id="fe5f0-146">**Symenum Symbols**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-146">**SymEnumSymbols**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[<span data-ttu-id="fe5f0-147">**Symen-symbolsforaddr**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-147">**SymEnumSymbolsForAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[<span data-ttu-id="fe5f0-148">**Symenenumtypes**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-148">**SymEnumTypes**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[<span data-ttu-id="fe5f0-149">**Symenentypesbyname**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-149">**SymEnumTypesByName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[<span data-ttu-id="fe5f0-150">**Symfinddebuginfofile**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-150">**SymFindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[<span data-ttu-id="fe5f0-151">**Symfindexecutableimage**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-151">**SymFindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[<span data-ttu-id="fe5f0-152">**Symfindfileinpath**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-152">**SymFindFileInPath**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[<span data-ttu-id="fe5f0-153">**Symfromaddr**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-153">**SymFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[<span data-ttu-id="fe5f0-154">**Symfromindex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-154">**SymFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[<span data-ttu-id="fe5f0-155">**Symfromname**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-155">**SymFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[<span data-ttu-id="fe5f0-156">**Symfromtoken**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-156">**SymFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[<span data-ttu-id="fe5f0-157">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-157">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="fe5f0-158">**SymGetFileLineOffsets64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-158">**SymGetFileLineOffsets64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[<span data-ttu-id="fe5f0-159">**Symgethomedirectory**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-159">**SymGetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[<span data-ttu-id="fe5f0-160">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-160">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="fe5f0-161">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-161">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="fe5f0-162">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-162">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="fe5f0-163">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-163">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="fe5f0-164">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-164">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="fe5f0-165">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-165">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="fe5f0-166">**Symgetomaps**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-166">**SymGetOmaps**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[<span data-ttu-id="fe5f0-167">**Symgetoptions**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-167">**SymGetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[<span data-ttu-id="fe5f0-168">**Symgetscope**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-168">**SymGetScope**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[<span data-ttu-id="fe5f0-169">**Symgetsearchpath**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-169">**SymGetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[<span data-ttu-id="fe5f0-170">**Symgetsymbolfile**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-170">**SymGetSymbolFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[<span data-ttu-id="fe5f0-171">**Symgettypeer FromName**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-171">**SymGetTypeFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[<span data-ttu-id="fe5f0-172">**Symgettypeingefo**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-172">**SymGetTypeInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[<span data-ttu-id="fe5f0-173">**Symgettypeingefoex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-173">**SymGetTypeInfoEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[<span data-ttu-id="fe5f0-174">**Syminitialize**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-174">**SymInitialize**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[<span data-ttu-id="fe5f0-175">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-175">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="fe5f0-176">**Symloadmoduleex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-176">**SymLoadModuleEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[<span data-ttu-id="fe5f0-177">**Symmatchfilename**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-177">**SymMatchFileName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[<span data-ttu-id="fe5f0-178">**Symmatchstring**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-178">**SymMatchString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[<span data-ttu-id="fe5f0-179">**Symnext**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-179">**SymNext**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[<span data-ttu-id="fe5f0-180">**Symprev**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-180">**SymPrev**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[<span data-ttu-id="fe5f0-181">**Symaktumodulelist**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-181">**SymRefreshModuleList**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[<span data-ttu-id="fe5f0-182">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-182">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="fe5f0-183">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-183">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="fe5f0-184">**Symsearch**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-184">**SymSearch**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[<span data-ttu-id="fe5f0-185">**Symsetcontext**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-185">**SymSetContext**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[<span data-ttu-id="fe5f0-186">**SYM-thomedirectory**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-186">**SymSetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[<span data-ttu-id="fe5f0-187">**Symabtoptions**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-187">**SymSetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[<span data-ttu-id="fe5f0-188">**Symsetscopefromaddr**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-188">**SymSetScopeFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[<span data-ttu-id="fe5f0-189">**Symsetscopefromindex**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-189">**SymSetScopeFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[<span data-ttu-id="fe5f0-190">**Symsetsearchpath**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-190">**SymSetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[<span data-ttu-id="fe5f0-191">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-191">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="fe5f0-192">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-192">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a><span data-ttu-id="fe5f0-193">Symbol Server</span><span class="sxs-lookup"><span data-stu-id="fe5f0-193">Symbol Server</span></span>

<span data-ttu-id="fe5f0-194">Der [Symbol Server](symbol-servers-and-symbol-stores.md) ermöglicht es Debuggern, die richtigen Symbol Dateien ohne Produktnamen, Releases oder Buildnummern automatisch abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-194">The [symbol server](symbol-servers-and-symbol-stores.md) enables debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="fe5f0-195">Die folgenden Funktionen werden mit dem Symbol Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-195">The following functions are used with the symbol server.</span></span>

<dl>

[<span data-ttu-id="fe5f0-196">**Symsrvdelta Name**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-196">**SymSrvDeltaName**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[<span data-ttu-id="fe5f0-197">**Symsrvgetfileingedexes**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-197">**SymSrvGetFileIndexes**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[<span data-ttu-id="fe5f0-198">**Symsrvgetfileindexinfo**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-198">**SymSrvGetFileIndexInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[<span data-ttu-id="fe5f0-199">**Symsrvgetfileingedexstring**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-199">**SymSrvGetFileIndexString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[<span data-ttu-id="fe5f0-200">**Symsrvgetsupplement**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-200">**SymSrvGetSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[<span data-ttu-id="fe5f0-201">**Symsrvisstore**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-201">**SymSrvIsStore**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[<span data-ttu-id="fe5f0-202">**Symsrvstorefile**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-202">**SymSrvStoreFile**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[<span data-ttu-id="fe5f0-203">**Symsrvstoresupplement**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-203">**SymSrvStoreSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a><span data-ttu-id="fe5f0-204">Minidump-Dateien im Benutzermodus</span><span class="sxs-lookup"><span data-stu-id="fe5f0-204">User-mode Minidump Files</span></span>

<span data-ttu-id="fe5f0-205">Die Minidump-Funktionen bieten eine Möglichkeit für Anwendungen, crashdump-Dateien zu erstellen, die eine nützliche Teilmenge des gesamten Prozess Kontexts enthalten. Dies wird als [Minidumpdatei](minidump-files.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-205">The minidump functions provide a way for applications to produce crashdump files that contain a useful subset of the entire process context; this is known as a [minidump file](minidump-files.md).</span></span> <span data-ttu-id="fe5f0-206">Die folgenden Funktionen werden für Minidump-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-206">The following functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="fe5f0-207">**Minidumpcallback**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-207">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="fe5f0-208">**Minidumpreaddumpstream**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-208">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="fe5f0-209">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-209">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a><span data-ttu-id="fe5f0-210">Quellserver</span><span class="sxs-lookup"><span data-stu-id="fe5f0-210">Source Server</span></span>

<span data-ttu-id="fe5f0-211">Der [Quell Server](source-server-and-source-indexing.md) ermöglicht einem Client das Abrufen der exakten Version der Quelldateien, die zum Erstellen einer Anwendung verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-211">[Source server](source-server-and-source-indexing.md) enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="fe5f0-212">Die folgenden Funktionen werden mit dem Quell Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-212">The following functions are used with source server.</span></span>

-   [<span data-ttu-id="fe5f0-213">**Symgetsourcefile**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-213">**SymGetSourceFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [<span data-ttu-id="fe5f0-214">**Symenzusourcefiletokens**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-214">**SymEnumSourceFileTokens**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [<span data-ttu-id="fe5f0-215">**Symenum SourceFile-SPROC**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-215">**SymEnumSourceFileTokensProc**</span></span>](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [<span data-ttu-id="fe5f0-216">**Symgetsourcefilefromtoken**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-216">**SymGetSourceFileFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [<span data-ttu-id="fe5f0-217">**Symgetsourcefiletoken**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-217">**SymGetSourceFileToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [<span data-ttu-id="fe5f0-218">**Symgetsourcevarfromtoken**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-218">**SymGetSourceVarFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a><span data-ttu-id="fe5f0-219">Veraltete Funktionen</span><span class="sxs-lookup"><span data-stu-id="fe5f0-219">Obsolete Functions</span></span>

<dl>

[<span data-ttu-id="fe5f0-220">**Mapdebuginformation**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-220">**MapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[<span data-ttu-id="fe5f0-221">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-221">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="fe5f0-222">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-222">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="fe5f0-223">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-223">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="fe5f0-224">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-224">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="fe5f0-225">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-225">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="fe5f0-226">**Unmapdebuginformation**</span><span class="sxs-lookup"><span data-stu-id="fe5f0-226">**UnMapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



