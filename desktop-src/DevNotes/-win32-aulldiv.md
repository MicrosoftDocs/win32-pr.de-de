---
title: _aulldiv-Routine
description: Dividiert zwei ULONGLONG-Ganzzahlen.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104472204"
---
# <a name="_aulldiv-routine"></a><span data-ttu-id="e3937-103">\_aulldiv-Routine</span><span class="sxs-lookup"><span data-stu-id="e3937-103">\_aulldiv Routine</span></span>

<span data-ttu-id="e3937-104">Dividiert zwei **ULONGLONG** -Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="e3937-104">Divides two **ULONGLONG** integers.</span></span>
<span data-ttu-id="e3937-105">Wenn Sie z. b. zwei UInt64-Werte aufteilen möchten, generiert der Compiler möglicherweise einen-Rückruf der **\_ aulldiv** -Routine.</span><span class="sxs-lookup"><span data-stu-id="e3937-105">For example, to divide two uint64 values the compiler might generate a call to the **\_aulldiv** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3937-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3937-106">Remarks</span></span>

<span data-ttu-id="e3937-107">Die **\_ aulldiv** -Routine ist eine Hilfsroutine für den C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="e3937-107">The **\_aulldiv** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="e3937-108">Ob der Compiler **\_ aulldiv** verwendet, ist vollständig von der Optimierungs Gruppe abhängig.</span><span class="sxs-lookup"><span data-stu-id="e3937-108">Whether the compiler uses **\_aulldiv** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="e3937-109">Diese Funktion wird nur auf x86-Plattformen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3937-109">This function is used only on x86 platforms.</span></span>
