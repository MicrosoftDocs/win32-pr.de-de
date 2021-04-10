---
title: _allmul-Routine
description: Multipliziert zwei ganze Zahlen vom Typ "Longlong" oder "ULONGLONG".
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104038469"
---
# <a name="_allmul-routine"></a><span data-ttu-id="5be06-103">\_allmul-Routine</span><span class="sxs-lookup"><span data-stu-id="5be06-103">\_allmul Routine</span></span>

<span data-ttu-id="5be06-104">Multipliziert zwei ganze Zahlen vom Typ " **Longlong** " oder " **ULONGLONG** ".</span><span class="sxs-lookup"><span data-stu-id="5be06-104">Multiplies two **LONGLONG** or **ULONGLONG** integers.</span></span>
<span data-ttu-id="5be06-105">Um z. b. zwei Int64-Werte zu multiplizieren, generiert der Compiler möglicherweise einen-Rückruf für die **\_ allmul** -Routine.</span><span class="sxs-lookup"><span data-stu-id="5be06-105">For example, to multiply two int64 values the compiler might generate a call to the **\_allmul** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="5be06-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5be06-106">Remarks</span></span>

<span data-ttu-id="5be06-107">Die **\_ allmul** -Routine ist eine Hilfsroutine für den C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="5be06-107">The **\_allmul** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="5be06-108">Ob der Compiler **\_ allmul** verwendet, ist vollständig vom Optimierungs Satz abhängig.</span><span class="sxs-lookup"><span data-stu-id="5be06-108">Whether the compiler uses **\_allmul** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="5be06-109">Diese Routine wird nur auf x86-Plattformen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5be06-109">This routine is used only on x86 platforms.</span></span>
