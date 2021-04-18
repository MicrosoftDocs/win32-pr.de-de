---
description: 'Dieser Abschnitt enthält Informationen zu den folgenden Funktionen:'
ms.assetid: b76643f0-387f-49c6-80e5-4d7b406b4db7
title: Effekt Funktionen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111fdcb34bbf1d9a86a295e62f734938991dda99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523851"
---
# <a name="effect-functions-direct3d-10"></a><span data-ttu-id="59135-103">Effekt Funktionen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="59135-103">Effect Functions (Direct3D 10)</span></span>

<span data-ttu-id="59135-104">Dieser Abschnitt enthält Informationen zu den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="59135-104">This section contains information about the following effect functions:</span></span>



| <span data-ttu-id="59135-105">Functions</span><span class="sxs-lookup"><span data-stu-id="59135-105">Functions</span></span>                                                                      | <span data-ttu-id="59135-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59135-106">Description</span></span>                                                         |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="59135-107">**D3D10CompileEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="59135-107">**D3D10CompileEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)           | <span data-ttu-id="59135-108">Kompilieren eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="59135-108">Compile an effect.</span></span>                                                  |
| [<span data-ttu-id="59135-109">**D3D10CreateEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="59135-109">**D3D10CreateEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectfrommemory)             | <span data-ttu-id="59135-110">Erstellen Sie einen Effekt.</span><span class="sxs-lookup"><span data-stu-id="59135-110">Create an effect.</span></span>                                                   |
| [<span data-ttu-id="59135-111">**D3D10CreateEffectPoolFromMemory**</span><span class="sxs-lookup"><span data-stu-id="59135-111">**D3D10CreateEffectPoolFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectpoolfrommemory)     | <span data-ttu-id="59135-112">Erstellen Sie einen Effekt Pool.</span><span class="sxs-lookup"><span data-stu-id="59135-112">Create an effect pool.</span></span>                                              |
| [<span data-ttu-id="59135-113">**D3D10CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="59135-113">**D3D10CreateStateBlock**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createstateblock)                         | <span data-ttu-id="59135-114">Erstellen Sie einen Zustands Block.</span><span class="sxs-lookup"><span data-stu-id="59135-114">Create a state block.</span></span>                                               |
| [<span data-ttu-id="59135-115">**D3D10DisassembleEffect**</span><span class="sxs-lookup"><span data-stu-id="59135-115">**D3D10DisassembleEffect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10disassembleeffect)                       | <span data-ttu-id="59135-116">Disassemblieren eines kompilierten Effekts in shaderassemblyanweisungen.</span><span class="sxs-lookup"><span data-stu-id="59135-116">Disassemble a compiled effect into shader assembly instructions.</span></span>    |
| [<span data-ttu-id="59135-117">**D3D10StateBlockMaskDifference**</span><span class="sxs-lookup"><span data-stu-id="59135-117">**D3D10StateBlockMaskDifference**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdifference)         | <span data-ttu-id="59135-118">Kombinieren Sie zwei State-Block-Masken mit einem bitweisen XOR.</span><span class="sxs-lookup"><span data-stu-id="59135-118">Combine two state-block masks with a bitwise XOR.</span></span>                   |
| [<span data-ttu-id="59135-119">**D3D10StateBlockMaskDisableAll**</span><span class="sxs-lookup"><span data-stu-id="59135-119">**D3D10StateBlockMaskDisableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisableall)         | <span data-ttu-id="59135-120">Deaktivieren Sie die Zustands Erfassung.</span><span class="sxs-lookup"><span data-stu-id="59135-120">Disable state capturing.</span></span>                                            |
| [<span data-ttu-id="59135-121">**D3D10StateBlockMaskDisableCapture**</span><span class="sxs-lookup"><span data-stu-id="59135-121">**D3D10StateBlockMaskDisableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisablecapture) | <span data-ttu-id="59135-122">Deaktivieren Sie die Zustands Erfassung mit einer Status Block Maske.</span><span class="sxs-lookup"><span data-stu-id="59135-122">Disable state capturing with a state-block mask.</span></span>                    |
| [<span data-ttu-id="59135-123">**D3D10StateBlockMaskEnableAll**</span><span class="sxs-lookup"><span data-stu-id="59135-123">**D3D10StateBlockMaskEnableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenableall)           | <span data-ttu-id="59135-124">Aktivieren Sie eine Zustands Block Maske, um alle Zustandsvariablen zu erfassen und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="59135-124">Enable a state-block mask to capture and apply all state variables.</span></span> |
| [<span data-ttu-id="59135-125">**D3D10StateBlockMaskEnableCapture**</span><span class="sxs-lookup"><span data-stu-id="59135-125">**D3D10StateBlockMaskEnableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenablecapture)   | <span data-ttu-id="59135-126">Aktivieren Sie einen Bereich von Zustands Werten in einer Zustands Block Maske.</span><span class="sxs-lookup"><span data-stu-id="59135-126">Enable a range of state values in a state block mask.</span></span>               |
| [<span data-ttu-id="59135-127">**D3D10StateBlockMaskGetSetting**</span><span class="sxs-lookup"><span data-stu-id="59135-127">**D3D10StateBlockMaskGetSetting**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskgetsetting)         | <span data-ttu-id="59135-128">Ein Element in einer Zustands Block Maske erhalten.</span><span class="sxs-lookup"><span data-stu-id="59135-128">Get an element in a state-block mask.</span></span>                               |
| [<span data-ttu-id="59135-129">**D3D10StateBlockMaskIntersect**</span><span class="sxs-lookup"><span data-stu-id="59135-129">**D3D10StateBlockMaskIntersect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskintersect)           | <span data-ttu-id="59135-130">Kombinieren Sie zwei State-Block-Masken mit einem bitweisen and.</span><span class="sxs-lookup"><span data-stu-id="59135-130">Combine two state-block masks with a bitwise AND.</span></span>                   |
| [<span data-ttu-id="59135-131">**D3D10StateBlockMaskUnion**</span><span class="sxs-lookup"><span data-stu-id="59135-131">**D3D10StateBlockMaskUnion**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskunion)                   | <span data-ttu-id="59135-132">Kombinieren Sie zwei State-Block-Masken mit einem bitweisen OR-Operator.</span><span class="sxs-lookup"><span data-stu-id="59135-132">Combine two state-block masks with a bitwise OR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="59135-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59135-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59135-134">Effekt Referenz</span><span class="sxs-lookup"><span data-stu-id="59135-134">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



