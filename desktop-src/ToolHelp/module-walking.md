---
title: Modul läuft
description: Eine Momentaufnahme, die die Modulliste für einen angegebenen Prozess enthält, enthält Informationen zu den einzelnen Modulen, ausführbaren Dateien oder DLL-Dateien (Dynamic Link Library), die vom angegebenen Prozess verwendet werden.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- Dynamic Link Libraries
- Dynamic-Link-Bibliotheken, Enumerieren von DLLs
- Auflisten
- auflisten, DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101754"
---
# <a name="module-walking"></a><span data-ttu-id="081b1-107">Modul läuft</span><span class="sxs-lookup"><span data-stu-id="081b1-107">Module Walking</span></span>

<span data-ttu-id="081b1-108">Eine Momentaufnahme, die die Modulliste für einen angegebenen Prozess enthält, enthält Informationen zu den einzelnen Modulen, ausführbaren Dateien oder DLL-Dateien (Dynamic Link Library), die vom angegebenen Prozess verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="081b1-108">A snapshot that includes the module list for a specified process contains information about each module, executable file, or dynamic-link library (DLL), used by the specified process.</span></span> <span data-ttu-id="081b1-109">Mit der [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) -Funktion können Sie Informationen für das erste Modul in der Liste abrufen.</span><span class="sxs-lookup"><span data-stu-id="081b1-109">You can retrieve information for the first module in the list by using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) function.</span></span> <span data-ttu-id="081b1-110">Nachdem Sie das erste Modul in der Liste abgerufen haben, können Sie mithilfe der [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) -Funktion Informationen für nachfolgende Module in der Liste abrufen.</span><span class="sxs-lookup"><span data-stu-id="081b1-110">After retrieving the first module in the list, you can retrieve information for subsequent modules in the list by using the [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) function.</span></span> <span data-ttu-id="081b1-111">**Module32First** und **Module32Next** füllen eine [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) -Struktur mit Informationen über das Modul.</span><span class="sxs-lookup"><span data-stu-id="081b1-111">**Module32First** and **Module32Next** fill a [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) structure with information about the module.</span></span>

<span data-ttu-id="081b1-112">Mit der [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion können Sie einen erweiterten Fehlerstatus Code für [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) und [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) abrufen.</span><span class="sxs-lookup"><span data-stu-id="081b1-112">You can retrieve an extended error status code for [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="081b1-113">Der Modul Bezeichner, der im **th32ModuleID** -Member von [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)angegeben ist, hat nur eine Bedeutung in 16-Bit-Fenstern.</span><span class="sxs-lookup"><span data-stu-id="081b1-113">The module identifier, which is specified in the **th32ModuleID** member of [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), only has meaning in 16-bit Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="081b1-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="081b1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="081b1-115">Durchlaufen der Modulliste</span><span class="sxs-lookup"><span data-stu-id="081b1-115">Traversing the Module List</span></span>](traversing-the-module-list.md)
</dt> </dl>

 

 