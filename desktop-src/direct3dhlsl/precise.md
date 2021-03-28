---
title: Precise (Genau)
description: Die pro-Anweisung-Deaktivierung des arithmetischen refactorings.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516478"
---
# <a name="precise"></a><span data-ttu-id="6e55e-103">Precise (Genau)</span><span class="sxs-lookup"><span data-stu-id="6e55e-103">Precise</span></span>

<span data-ttu-id="6e55e-104">Die pro-Anweisung-Deaktivierung des arithmetischen refactorings.</span><span class="sxs-lookup"><span data-stu-id="6e55e-104">Per-instruction disabling of arithmetic refactoring.</span></span>



| <span data-ttu-id="6e55e-105">präzise (Komponenten Maske)</span><span class="sxs-lookup"><span data-stu-id="6e55e-105">precise (component mask)</span></span> |
|--------------------------|



 

<span data-ttu-id="6e55e-106">Dieser Modifizierer erfordert das globale shaderflag "Refactoring \_ zugelassen".</span><span class="sxs-lookup"><span data-stu-id="6e55e-106">This modifier requires the global shader flag "REFACTORING\_ALLOWED".</span></span> <span data-ttu-id="6e55e-107">Wenn das Refactoring \_ zulässig ist, können einzelne Komponenten Ergebnisse einzelner Anweisungen erzwungen werden, damit Sie durch Compiler oder Treiber präzise oder nicht umgestaltbar bleiben.</span><span class="sxs-lookup"><span data-stu-id="6e55e-107">When REFACTORING\_ALLOWED is present, individual component results of individual instructions can be forced to remain precise or not-refactorable by compilers or drivers.</span></span> <span data-ttu-id="6e55e-108">Wenn die Komponenten einer [**Mad**](mad--sm4---asm-.md) -Anweisung als **präzise** gekennzeichnet sind, muss die Hardware eine **Mad** -Anweisung oder die exakte Entsprechung ausführen, und Sie kann Sie nicht in ein multiplizieren, gefolgt von einem Add-Wert, aufteilen.</span><span class="sxs-lookup"><span data-stu-id="6e55e-108">If components of a [**mad**](mad--sm4---asm-.md) instruction are tagged as **precise**, the hardware must execute a **mad** instruction or the exact equivalent, and it cannot split it into a multiply followed by an add.</span></span> <span data-ttu-id="6e55e-109">Umgekehrt kann ein multiplizieren, gefolgt von einem Add-in, bei dem entweder oder beide als **genau** gekennzeichnet sind, nicht mit einem gemergten **Mad** zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6e55e-109">Conversely, a multiply followed by an add, where either or both are flagged as **precise**, cannot be merged into a fused **mad**.</span></span>

<span data-ttu-id="6e55e-110">Wenn Refactoring \_ zugelassen nicht angegeben wurde, ist der **exakte** Modifizierer nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6e55e-110">If REFACTORING\_ALLOWED has not been specified, the **precise** modifier is not allowed.</span></span> <span data-ttu-id="6e55e-111">Er ist nicht erforderlich, da alles präzise ist.</span><span class="sxs-lookup"><span data-stu-id="6e55e-111">It is not needed because everything is precise.</span></span> <span data-ttu-id="6e55e-112">Der **genaue** Modifizierer wirkt sich auf jeden Vorgang aus, nicht nur auf Arithmetik.</span><span class="sxs-lookup"><span data-stu-id="6e55e-112">The **precise** modifier affects any operation, not just arithmetic.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6e55e-113">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6e55e-113">Minimum Shader Model</span></span>

<span data-ttu-id="6e55e-114">Dieser Modifizierer wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6e55e-114">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="6e55e-115">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6e55e-115">Shader Model</span></span>                                              | <span data-ttu-id="6e55e-116">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6e55e-116">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6e55e-117">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="6e55e-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6e55e-118">ja</span><span class="sxs-lookup"><span data-stu-id="6e55e-118">yes</span></span>       |
| [<span data-ttu-id="6e55e-119">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="6e55e-119">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6e55e-120">nein</span><span class="sxs-lookup"><span data-stu-id="6e55e-120">no</span></span>        |
| [<span data-ttu-id="6e55e-121">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="6e55e-121">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6e55e-122">ja</span><span class="sxs-lookup"><span data-stu-id="6e55e-122">yes</span></span>       |
| [<span data-ttu-id="6e55e-123">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e55e-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6e55e-124">nein</span><span class="sxs-lookup"><span data-stu-id="6e55e-124">no</span></span>        |
| [<span data-ttu-id="6e55e-125">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e55e-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6e55e-126">nein</span><span class="sxs-lookup"><span data-stu-id="6e55e-126">no</span></span>        |
| [<span data-ttu-id="6e55e-127">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6e55e-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6e55e-128">nein</span><span class="sxs-lookup"><span data-stu-id="6e55e-128">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6e55e-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e55e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e55e-130">Shader Model 5-Anweisungs modifiziererer</span><span class="sxs-lookup"><span data-stu-id="6e55e-130">Shader Model 5 Instruction Modifiers</span></span>](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




