---
title: Wenn bool-vs
description: Startet eine, wenn... else... der umdif-vs-Block.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038306"
---
# <a name="if-bool---vs"></a><span data-ttu-id="8969e-103">Wenn bool-vs</span><span class="sxs-lookup"><span data-stu-id="8969e-103">if bool - vs</span></span>

<span data-ttu-id="8969e-104">Startet eine, wenn... [else](else---vs.md)... der [umdif-vs-](endif---vs.md) Block.</span><span class="sxs-lookup"><span data-stu-id="8969e-104">Starts an if...[else](else---vs.md)...[endif - vs](endif---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="8969e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8969e-105">Syntax</span></span>



| <span data-ttu-id="8969e-106">Wenn bool</span><span class="sxs-lookup"><span data-stu-id="8969e-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="8969e-107">Dabei ist bool eine boolesche Registernummer.</span><span class="sxs-lookup"><span data-stu-id="8969e-107">where bool is a bool register number.</span></span> <span data-ttu-id="8969e-108">Siehe [konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="8969e-108">See [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8969e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8969e-109">Remarks</span></span>



| <span data-ttu-id="8969e-110">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="8969e-110">Vertex shader versions</span></span> | <span data-ttu-id="8969e-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="8969e-111">1\_1</span></span> | <span data-ttu-id="8969e-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8969e-112">2\_0</span></span> | <span data-ttu-id="8969e-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8969e-113">2\_x</span></span> | <span data-ttu-id="8969e-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8969e-114">2\_sw</span></span> | <span data-ttu-id="8969e-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8969e-115">3\_0</span></span> | <span data-ttu-id="8969e-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8969e-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8969e-117">Wenn bool</span><span class="sxs-lookup"><span data-stu-id="8969e-117">if bool</span></span>                |      | <span data-ttu-id="8969e-118">x</span><span class="sxs-lookup"><span data-stu-id="8969e-118">x</span></span>    | <span data-ttu-id="8969e-119">x</span><span class="sxs-lookup"><span data-stu-id="8969e-119">x</span></span>    | <span data-ttu-id="8969e-120">x</span><span class="sxs-lookup"><span data-stu-id="8969e-120">x</span></span>     | <span data-ttu-id="8969e-121">x</span><span class="sxs-lookup"><span data-stu-id="8969e-121">x</span></span>    | <span data-ttu-id="8969e-122">x</span><span class="sxs-lookup"><span data-stu-id="8969e-122">x</span></span>     |



 

<span data-ttu-id="8969e-123">Wenn das boolesche Quell Konto in der if-Anweisung "true" ist, wird der Code, der von der if-Anweisung und dem entsprechenden anderen eingeschlossen wird, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8969e-123">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching else is run.</span></span> <span data-ttu-id="8969e-124">Andernfalls wird der Code, der von der [else](else---vs.md)... [EndIf-vs-](endif---vs.md) Anweisungen werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8969e-124">Otherwise, the code enclosed by the [else](else---vs.md)...[endif - vs](endif---vs.md) statements is run.</span></span> <span data-ttu-id="8969e-125">Diese Anweisung verwendet einen Anweisungs Slot.</span><span class="sxs-lookup"><span data-stu-id="8969e-125">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="8969e-126">, wenn Blöcke eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="8969e-126">if blocks can be nested.</span></span>

<span data-ttu-id="8969e-127">Ein If-Block kann einen Schleifen Block nicht verspannen.</span><span class="sxs-lookup"><span data-stu-id="8969e-127">An if block cannot straddle a loop block.</span></span>

## <a name="example"></a><span data-ttu-id="8969e-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8969e-128">Example</span></span>

<span data-ttu-id="8969e-129">Diese Anweisung stellt bedingte statische Fluss Steuerung bereit.</span><span class="sxs-lookup"><span data-stu-id="8969e-129">This instruction provides conditional static flow control.</span></span>


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="8969e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8969e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8969e-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="8969e-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="8969e-132">Else-vs</span><span class="sxs-lookup"><span data-stu-id="8969e-132">else - vs</span></span>](else---vs.md)
</dt> <dt>

[<span data-ttu-id="8969e-133">umdif-vs</span><span class="sxs-lookup"><span data-stu-id="8969e-133">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 




