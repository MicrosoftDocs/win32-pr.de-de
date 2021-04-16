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
# <a name="updated-platform-support"></a><span data-ttu-id="b7874-103">Aktualisierte Plattformunterstützung</span><span class="sxs-lookup"><span data-stu-id="b7874-103">Updated Platform Support</span></span>

<span data-ttu-id="b7874-104">Bei Bedarf wurde die DbgHelp-Bibliothek erweitert, um sowohl 32-als auch 64-Bit-Windows zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b7874-104">Where necessary, the DbgHelp library has been widened to support both 32- and 64-bit Windows.</span></span> <span data-ttu-id="b7874-105">Die ursprünglichen Funktions-und Strukturdefinitionen befinden sich weiterhin in "dbghelp. h", aber es gibt auch aktualisierte Versionen dieser Definitionen, die mit 64-Bit-Fenstern kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="b7874-105">The original function and structure definitions are still in DbgHelp.h, but there are also updated versions of these definitions that are compatible with 64-bit Windows.</span></span> <span data-ttu-id="b7874-106">Wenn Sie die aktualisierten Funktionen in Ihrem Code verwenden, können Sie für 32-und 64-Bit-Fenster kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="b7874-106">If you use the updated functions in your code, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="b7874-107">Der Code ist auch effizienter, da die ursprünglichen Funktionen einfach die aktualisierten Funktionen aufzurufen, um die Arbeit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b7874-107">Your code will also be more efficient, since the original functions simply call the updated functions to perform the work.</span></span>

<span data-ttu-id="b7874-108">"Dbghelp. h" enthält beispielsweise Definitionen für **symunloadmodule** (ursprüngliche Funktion) und **SymUnloadModule64** (aktualisierte Funktion).</span><span class="sxs-lookup"><span data-stu-id="b7874-108">For example, DbgHelp.h contains definitions for **SymUnloadModule** (original function) and **SymUnloadModule64** (updated function).</span></span> <span data-ttu-id="b7874-109">Diese Definitionen sind nahezu identisch, verwenden jedoch unterschiedliche Typen für den *baseof* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b7874-109">These definitions are nearly identical, but use different types for the *BaseOfDll* parameter.</span></span> <span data-ttu-id="b7874-110">(**Symunloadmodule** verwendet den **DWORD** -Typ, während **SymUnloadModule64** den **DWORD64** -Typ verwendet.) Wenn Sie den Code für die Verwendung von **SymUnloadModule64** schreiben, kann er für 32-und 64-Bit-Fenster kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="b7874-110">(**SymUnloadModule** uses the **DWORD** type, while **SymUnloadModule64** uses the **DWORD64** type.) If you write your code to use **SymUnloadModule64**, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="b7874-111">Der Code ist auch effizienter, als wenn er " **symunloadmodule**" aufruft.</span><span class="sxs-lookup"><span data-stu-id="b7874-111">The code is also more efficient than if it were to call **SymUnloadModule**.</span></span>

<span data-ttu-id="b7874-112">Im folgenden finden Sie eine Liste der aktualisierten Funktionen:</span><span class="sxs-lookup"><span data-stu-id="b7874-112">The following is a list of the updated functions:</span></span>

<dl>

[<span data-ttu-id="b7874-113">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="b7874-113">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="b7874-114">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="b7874-114">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="b7874-115">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="b7874-115">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="b7874-116">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="b7874-116">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="b7874-117">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="b7874-117">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="b7874-118">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="b7874-118">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="b7874-119">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="b7874-119">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="b7874-120">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="b7874-120">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="b7874-121">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="b7874-121">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="b7874-122">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="b7874-122">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="b7874-123">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="b7874-123">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="b7874-124">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="b7874-124">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="b7874-125">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="b7874-125">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="b7874-126">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="b7874-126">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="b7874-127">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="b7874-127">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="b7874-128">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="b7874-128">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="b7874-129">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="b7874-129">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="b7874-130">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="b7874-130">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="b7874-131">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="b7874-131">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="b7874-132">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="b7874-132">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

<span data-ttu-id="b7874-133">Im folgenden finden Sie eine Liste der aktualisierten Strukturen:</span><span class="sxs-lookup"><span data-stu-id="b7874-133">The following is a list of the updated structures:</span></span>

<dl>

[<span data-ttu-id="b7874-134">**ADDRESS64**</span><span class="sxs-lookup"><span data-stu-id="b7874-134">**ADDRESS64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[<span data-ttu-id="b7874-135">**Zurück gestelltes imagehlp- \_ \_ Symbol \_ LOAD64**</span><span class="sxs-lookup"><span data-stu-id="b7874-135">**IMAGEHLP\_DEFERRED\_SYMBOL\_LOAD64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[<span data-ttu-id="b7874-136">**Imagehlp \_ SYMBOL64 duplizieren \_**</span><span class="sxs-lookup"><span data-stu-id="b7874-136">**IMAGEHLP\_DUPLICATE\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[<span data-ttu-id="b7874-137">**Imagehlp \_ LINE64**</span><span class="sxs-lookup"><span data-stu-id="b7874-137">**IMAGEHLP\_LINE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[<span data-ttu-id="b7874-138">**Imagehlp \_ MODULE64**</span><span class="sxs-lookup"><span data-stu-id="b7874-138">**IMAGEHLP\_MODULE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[<span data-ttu-id="b7874-139">**Imagehlp \_ SYMBOL64**</span><span class="sxs-lookup"><span data-stu-id="b7874-139">**IMAGEHLP\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[<span data-ttu-id="b7874-140">**KDHELP64**</span><span class="sxs-lookup"><span data-stu-id="b7874-140">**KDHELP64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[<span data-ttu-id="b7874-141">**STACKFRAME64**</span><span class="sxs-lookup"><span data-stu-id="b7874-141">**STACKFRAME64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



