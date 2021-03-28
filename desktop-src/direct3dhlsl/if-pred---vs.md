---
title: Wenn pred-vs
description: Start von, wenn pred-vs... Else-vs... der "eindif-vs"-Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313637"
---
# <a name="if-pred---vs"></a><span data-ttu-id="bc95c-103">Wenn pred-vs</span><span class="sxs-lookup"><span data-stu-id="bc95c-103">if pred - vs</span></span>

<span data-ttu-id="bc95c-104">Start von, wenn pred-vs... [else-vs](else---vs.md)... der " [eindif-vs"-](endif---vs.md) Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.</span><span class="sxs-lookup"><span data-stu-id="bc95c-104">Start of an if pred - vs...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc95c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc95c-105">Syntax</span></span>



| <span data-ttu-id="bc95c-106">Wenn \[ ! \] pred. replialisieswizzle</span><span class="sxs-lookup"><span data-stu-id="bc95c-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="bc95c-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="bc95c-107">Where:</span></span>

-   <span data-ttu-id="bc95c-108">\[!\] ein optionaler not-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="bc95c-108">\[!\] an optional NOT modifier.</span></span> <span data-ttu-id="bc95c-109">Dadurch wird der Wert im Prädikat Register geändert.</span><span class="sxs-lookup"><span data-stu-id="bc95c-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="bc95c-110">pred ist das Prädikat Register, p0.</span><span class="sxs-lookup"><span data-stu-id="bc95c-110">pred is the predicate register, p0.</span></span> <span data-ttu-id="bc95c-111">Siehe [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="bc95c-111">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="bc95c-112">repliereswizzle ist eine einzelne Komponente, die in alle vier Komponenten kopiert (oder repliziert) wird (swizzled).</span><span class="sxs-lookup"><span data-stu-id="bc95c-112">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="bc95c-113">Gültige Komponenten sind: x, y, z, w oder r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="bc95c-113">Valid components are: x, y, z, w or r, g, b, a.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc95c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc95c-114">Remarks</span></span>



| <span data-ttu-id="bc95c-115">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="bc95c-115">Vertex shader versions</span></span> | <span data-ttu-id="bc95c-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="bc95c-116">1\_1</span></span> | <span data-ttu-id="bc95c-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc95c-117">2\_0</span></span> | <span data-ttu-id="bc95c-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bc95c-118">2\_x</span></span> | <span data-ttu-id="bc95c-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bc95c-119">2\_sw</span></span> | <span data-ttu-id="bc95c-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc95c-120">3\_0</span></span> | <span data-ttu-id="bc95c-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bc95c-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bc95c-122">Wenn pred</span><span class="sxs-lookup"><span data-stu-id="bc95c-122">if pred</span></span>                |      |      | <span data-ttu-id="bc95c-123">x</span><span class="sxs-lookup"><span data-stu-id="bc95c-123">x</span></span>    | <span data-ttu-id="bc95c-124">x</span><span class="sxs-lookup"><span data-stu-id="bc95c-124">x</span></span>     | <span data-ttu-id="bc95c-125">x</span><span class="sxs-lookup"><span data-stu-id="bc95c-125">x</span></span>    | <span data-ttu-id="bc95c-126">x</span><span class="sxs-lookup"><span data-stu-id="bc95c-126">x</span></span>     |



 

<span data-ttu-id="bc95c-127">Diese Anweisung wird verwendet, um einen Codeblock auf Grundlage eines Kanals des Prädikats zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="bc95c-127">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="bc95c-128">Jeder, wenn der \_ pred-Block mit einer Else-oder endif-Anweisung enden muss.</span><span class="sxs-lookup"><span data-stu-id="bc95c-128">Each if\_pred block must end with an else or endif instruction.</span></span>

<span data-ttu-id="bc95c-129">Es gelten folgende Beschränkungen:</span><span class="sxs-lookup"><span data-stu-id="bc95c-129">Restrictions include:</span></span>

<span data-ttu-id="bc95c-130">, wenn \_ pred-Blöcke eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="bc95c-130">if\_pred blocks can be nested.</span></span> <span data-ttu-id="bc95c-131">Dadurch wird die gesamte dynamische Schachtelungs Tiefe zusammen mit [if \_ Comp](if-comp---vs.md) -Blöcken gezählt.</span><span class="sxs-lookup"><span data-stu-id="bc95c-131">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---vs.md) blocks.</span></span>

<span data-ttu-id="bc95c-132">Ein if \_ -pred-Block kann einen Schleifen Block nicht durchlaufen, er muss sich entweder vollständig darin befinden oder umschließen.</span><span class="sxs-lookup"><span data-stu-id="bc95c-132">An if\_pred block cannot straddle a loop block, it should be either completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc95c-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc95c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc95c-134">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="bc95c-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




