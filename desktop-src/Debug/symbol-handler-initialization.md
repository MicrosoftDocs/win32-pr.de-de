---
description: Der Symbol Handler dient zum Nachverfolgen verschiedener Sätze von Symbol Dateien.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Initialisierung von Symbol Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126050"
---
# <a name="symbol-handler-initialization"></a><span data-ttu-id="04649-103">Initialisierung von Symbol Handlern</span><span class="sxs-lookup"><span data-stu-id="04649-103">Symbol Handler Initialization</span></span>

<span data-ttu-id="04649-104">Der Symbol Handler dient zum Nachverfolgen verschiedener Sätze von Symbol Dateien.</span><span class="sxs-lookup"><span data-stu-id="04649-104">The symbol handler is designed to track various sets of symbol files.</span></span>

<span data-ttu-id="04649-105">Zum Initialisieren des Symbol Handlers wird die [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="04649-105">To initialize the symbol handler, call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="04649-106">Der *hProcess* -Parameter kann eine eindeutige beliebige Zahl, ein Wert, der von der [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) -Funktion zurückgegeben wird, oder der Bezeichner eines beliebigen laufenden Prozesses sein.</span><span class="sxs-lookup"><span data-stu-id="04649-106">The *hProcess* parameter can be a unique arbitrary number, a value returned from the [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) function, or the identifier of any running process.</span></span> <span data-ttu-id="04649-107">Der *finvadeprocess* -Parameter gibt an, ob der Symbol Handler die vom Prozess geladenen Module aufzählen und Symbole für die einzelnen Module laden soll.</span><span class="sxs-lookup"><span data-stu-id="04649-107">The *fInvadeProcess* parameter indicates whether the symbol handler should enumerate the modules loaded by the process and load symbols for each of its modules.</span></span> <span data-ttu-id="04649-108">Wenn *finvadeprocess* auf **true** festgelegt ist, muss der *hProcess* -Parameter der von **GetCurrentProcess** zurückgegebene Wert oder der Bezeichner eines vorhandenen Prozesses sein.</span><span class="sxs-lookup"><span data-stu-id="04649-108">If *fInvadeProcess* is **TRUE**, the *hProcess* parameter must be the value returned from **GetCurrentProcess** or the identifier of an existing process.</span></span> <span data-ttu-id="04649-109">Um diese Liste zu aktualisieren, verwenden Sie die [**symrefresh modulelist**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="04649-109">To refresh this list, use the [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) function.</span></span>

<span data-ttu-id="04649-110">Die Verwendung von *finvadeprocess* ist eine einfache Möglichkeit, alle Symbol Dateien für einen Prozess zu laden.</span><span class="sxs-lookup"><span data-stu-id="04649-110">Using *fInvadeProcess* is a simple way to load all symbol files for a process.</span></span> <span data-ttu-id="04649-111">Der Symbol Handler versucht jedoch nicht, Symbole für Module zu laden, die anschließend von der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion geladen werden.</span><span class="sxs-lookup"><span data-stu-id="04649-111">However, the symbol handler will not attempt to load symbols for modules subsequently loaded by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="04649-112">In diesem Fall müssen Sie die [**symloadmoduleex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="04649-112">You must use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function in this case.</span></span>

 

 
