---
title: Wenn pred-PS
description: Start einer if bool-PS... Else-PS... der "eindif-PS"-Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719374"
---
# <a name="if-pred---ps"></a><span data-ttu-id="b0984-103">Wenn pred-PS</span><span class="sxs-lookup"><span data-stu-id="b0984-103">if pred - ps</span></span>

<span data-ttu-id="b0984-104">Start einer [if bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... der " [eindif-PS"-](endif---ps.md) Block mit der Bedingung, die vom Inhalt des Prädikats registriert wird.</span><span class="sxs-lookup"><span data-stu-id="b0984-104">Start of an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0984-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0984-105">Syntax</span></span>



| <span data-ttu-id="b0984-106">Wenn \[ ! \] pred. replialisieswizzle</span><span class="sxs-lookup"><span data-stu-id="b0984-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="b0984-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="b0984-107">Where:</span></span>

-   <span data-ttu-id="b0984-108">\[!\] ist ein optionaler not-Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="b0984-108">\[!\] is an optional NOT modifier.</span></span> <span data-ttu-id="b0984-109">Dadurch wird der Wert im Prädikat Register geändert.</span><span class="sxs-lookup"><span data-stu-id="b0984-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="b0984-110">pred ist das [Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="b0984-110">pred is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="b0984-111">repliereswizzle ist eine einzelne Komponente, die in alle vier Komponenten kopiert (oder repliziert) wird (swizzled).</span><span class="sxs-lookup"><span data-stu-id="b0984-111">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="b0984-112">Gültige Komponenten sind: \[ x, y, z, w \] oder \[ r, g, b, a \] .</span><span class="sxs-lookup"><span data-stu-id="b0984-112">Valid components are: \[x, y, z, w\] or \[r, g, b, a\].</span></span>

## <a name="remarks"></a><span data-ttu-id="b0984-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0984-113">Remarks</span></span>



| <span data-ttu-id="b0984-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b0984-114">Pixel shader versions</span></span> | <span data-ttu-id="b0984-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="b0984-115">1\_1</span></span> | <span data-ttu-id="b0984-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="b0984-116">1\_2</span></span> | <span data-ttu-id="b0984-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b0984-117">1\_3</span></span> | <span data-ttu-id="b0984-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="b0984-118">1\_4</span></span> | <span data-ttu-id="b0984-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0984-119">2\_0</span></span> | <span data-ttu-id="b0984-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b0984-120">2\_x</span></span> | <span data-ttu-id="b0984-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0984-121">2\_sw</span></span> | <span data-ttu-id="b0984-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b0984-122">3\_0</span></span> | <span data-ttu-id="b0984-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b0984-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b0984-124">Wenn \_ pred</span><span class="sxs-lookup"><span data-stu-id="b0984-124">if\_pred</span></span>              |      |      |      |      |      | <span data-ttu-id="b0984-125">x</span><span class="sxs-lookup"><span data-stu-id="b0984-125">x</span></span>    | <span data-ttu-id="b0984-126">x</span><span class="sxs-lookup"><span data-stu-id="b0984-126">x</span></span>     | <span data-ttu-id="b0984-127">x</span><span class="sxs-lookup"><span data-stu-id="b0984-127">x</span></span>    | <span data-ttu-id="b0984-128">x</span><span class="sxs-lookup"><span data-stu-id="b0984-128">x</span></span>     |



 

<span data-ttu-id="b0984-129">Diese Anweisung wird verwendet, um einen Codeblock auf Grundlage eines Kanals des Prädikats zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="b0984-129">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="b0984-130">Jeder, wenn der \_ pred-Block mit einer [else-PS](else---ps.md) -oder [EndIf-PS-](endif---ps.md) Anweisung enden muss.</span><span class="sxs-lookup"><span data-stu-id="b0984-130">Each if\_pred block must end with an [else - ps](else---ps.md) or [endif - ps](endif---ps.md) instruction.</span></span>

<span data-ttu-id="b0984-131">Es gelten folgende Beschränkungen:</span><span class="sxs-lookup"><span data-stu-id="b0984-131">Restrictions include:</span></span>

<span data-ttu-id="b0984-132">, wenn \_ pred-Blöcke eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b0984-132">if\_pred blocks can be nested.</span></span> <span data-ttu-id="b0984-133">Dadurch wird die gesamte dynamische Schachtelungs Tiefe zusammen mit [if \_ Comp](if-comp---ps.md) -Blöcken gezählt.</span><span class="sxs-lookup"><span data-stu-id="b0984-133">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---ps.md) blocks.</span></span>

<span data-ttu-id="b0984-134">Ein if \_ -pred-Block kann einen Schleifen Block nicht durchlaufen, er muss sich entweder vollständig darin befinden oder umschließen.</span><span class="sxs-lookup"><span data-stu-id="b0984-134">An if\_pred block cannot straddle a loop block; it should either be completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0984-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0984-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0984-136">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b0984-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




