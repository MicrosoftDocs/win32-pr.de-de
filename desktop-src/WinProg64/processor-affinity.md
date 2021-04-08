---
title: Prozessor Affinität unter WOW64
description: 32-Bit-Windows unterstützt maximal 32 Prozessoren. Daher simulieren Funktionen wie z. b. getprocessaffinitymask einen Computer mit 32-Prozessoren, wenn Sie unter WOW64 aufgerufen werden.
ms.assetid: f50a03e8-1c23-4eb0-a1ff-471c28d6b611
keywords:
- Prozessor Affinität 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows-Programmierung, Prozessor Affinität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60ad6cf5055737dc39abd735211c5b4ec4ab9d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728409"
---
# <a name="processor-affinity-under-wow64"></a><span data-ttu-id="cfcd1-106">Prozessor Affinität unter WOW64</span><span class="sxs-lookup"><span data-stu-id="cfcd1-106">Processor Affinity Under WOW64</span></span>

<span data-ttu-id="cfcd1-107">32-Bit-Windows unterstützt maximal 32 Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="cfcd1-107">32-bit Windows supports a maximum of 32 processors.</span></span> <span data-ttu-id="cfcd1-108">Daher simulieren Funktionen wie z. b. [**getprocessaffinitymask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) einen Computer mit 32-Prozessoren, wenn Sie unter WOW64 aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cfcd1-108">Therefore, functions such as [**GetProcessAffinityMask**](/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask) simulate a computer with 32 processors when called under WOW64.</span></span>

<span data-ttu-id="cfcd1-109">Die Affinitäts Maske wird ermittelt, indem eine bitweise OR-Operation der obersten 32 Bits der Maske mit den unteren 32 Bits durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfcd1-109">The affinity mask is obtained by performing a bitwise OR operation of the top 32 bits of the mask with the low 32 bits.</span></span> <span data-ttu-id="cfcd1-110">Wenn ein Thread über eine Affinität für die Prozessoren 0, 1 und 32 verfügt, meldet WOW64 die Affinität daher als 0 und 1, da der Prozessor 32 dem Prozessor 0 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cfcd1-110">Therefore, if a thread has affinity for processors 0, 1, and 32, WOW64 reports the affinity as 0 and 1, because processor 32 maps to processor 0.</span></span> <span data-ttu-id="cfcd1-111">Funktionen, die Prozessor Affinität festlegen, wie z. b. [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), schränken Prozessoren auf die ersten 32-Prozessoren unter WOW64 ein.</span><span class="sxs-lookup"><span data-stu-id="cfcd1-111">Functions that set processor affinity, such as [**SetThreadAffinityMask**](/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask), restrict processors to the first 32 processors under WOW64.</span></span>

<span data-ttu-id="cfcd1-112">Weitere Informationen zur Prozessor Affinität finden Sie unter [mehrere Prozessoren](/windows/desktop/ProcThread/multiple-processors).</span><span class="sxs-lookup"><span data-stu-id="cfcd1-112">For more information about processor affinity, see [Multiple Processors](/windows/desktop/ProcThread/multiple-processors).</span></span>

 

 