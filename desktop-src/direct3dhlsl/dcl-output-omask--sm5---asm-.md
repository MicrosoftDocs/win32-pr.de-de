---
title: dcl_output omask (SM5-ASM)
description: Deklarieren Sie ein Ausgabe Register, das vom Shader geschrieben werden soll.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389597"
---
# <a name="dcl_output-omask-sm5---asm"></a><span data-ttu-id="11358-103">DCL- \_ Ausgabe-omask (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="11358-103">dcl\_output oMask (sm5 - asm)</span></span>

<span data-ttu-id="11358-104">Deklarieren Sie ein Ausgabe Register, das vom Shader geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="11358-104">Declare an output register to be written by the shader.</span></span>



| <span data-ttu-id="11358-105">DCL- \_ Ausgabe o \# \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="11358-105">dcl\_output o\#\[.mask\]</span></span> |
|--------------------------|



 



| <span data-ttu-id="11358-106">Element</span><span class="sxs-lookup"><span data-stu-id="11358-106">Item</span></span>                                                   | <span data-ttu-id="11358-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11358-107">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="11358-108"><span id="o"></span><span id="O"></span>*'*</span><span class="sxs-lookup"><span data-stu-id="11358-108"><span id="o"></span><span id="O"></span>*o*</span></span><br/> | <span data-ttu-id="11358-109">\[im \] Ausgabe Register.</span><span class="sxs-lookup"><span data-stu-id="11358-109">\[in\] The output register.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11358-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11358-110">Remarks</span></span>


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a><span data-ttu-id="11358-111">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="11358-111">Restrictions</span></span>

-   <span data-ttu-id="11358-112">Die Komponenten Maske kann eine beliebige Teilmenge von \[ xyzw sein \] .</span><span class="sxs-lookup"><span data-stu-id="11358-112">The component mask can be any subset of \[xyzw\].</span></span> <span data-ttu-id="11358-113">Lücken zwischen den Komponenten zu belassen, verschwendet jedoch Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="11358-113">However, leaving gaps between components wastes space.</span></span>
-   <span data-ttu-id="11358-114">Es ist zulässig, eine in der nächsten Phase für die Eingabe deklarierte übergeordnete Komponente der Komponenten Maske zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="11358-114">It is legal to declare a superset of the component mask declared for input by the next stage.</span></span> <span data-ttu-id="11358-115">Sich gegenseitig ausschließende Masken sind jedoch nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="11358-115">However mutually exclusive masks are not allowed.</span></span> <span data-ttu-id="11358-116">Der Vertex-Shader gibt "O3. XY" aus, d. h., der Pixelshader, der "v3. z" ist, ist ungültig, aber die Eingabe von "v3. x", "v3. y" oder "v3.</span><span class="sxs-lookup"><span data-stu-id="11358-116">The vertex shader outputting o3.xy, means the pixel shader inputting v3.z is invalid, but inputting v3.x or v3.y or v3.xy is valid.</span></span>

<span data-ttu-id="11358-117">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="11358-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="11358-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="11358-118">Vertex</span></span> | <span data-ttu-id="11358-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="11358-119">Hull</span></span> | <span data-ttu-id="11358-120">Domain</span><span class="sxs-lookup"><span data-stu-id="11358-120">Domain</span></span> | <span data-ttu-id="11358-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="11358-121">Geometry</span></span> | <span data-ttu-id="11358-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="11358-122">Pixel</span></span> | <span data-ttu-id="11358-123">Compute</span><span class="sxs-lookup"><span data-stu-id="11358-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="11358-124">X</span><span class="sxs-lookup"><span data-stu-id="11358-124">X</span></span>      | <span data-ttu-id="11358-125">X</span><span class="sxs-lookup"><span data-stu-id="11358-125">X</span></span>    | <span data-ttu-id="11358-126">X</span><span class="sxs-lookup"><span data-stu-id="11358-126">X</span></span>      | <span data-ttu-id="11358-127">X</span><span class="sxs-lookup"><span data-stu-id="11358-127">X</span></span>        | <span data-ttu-id="11358-128">X</span><span class="sxs-lookup"><span data-stu-id="11358-128">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11358-129">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="11358-129">Minimum Shader Model</span></span>

<span data-ttu-id="11358-130">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="11358-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="11358-131">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="11358-131">Shader Model</span></span>                                              | <span data-ttu-id="11358-132">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="11358-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="11358-133">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="11358-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="11358-134">ja</span><span class="sxs-lookup"><span data-stu-id="11358-134">yes</span></span>       |
| [<span data-ttu-id="11358-135">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="11358-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="11358-136">nein</span><span class="sxs-lookup"><span data-stu-id="11358-136">no</span></span>        |
| [<span data-ttu-id="11358-137">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="11358-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="11358-138">nein</span><span class="sxs-lookup"><span data-stu-id="11358-138">no</span></span>        |
| [<span data-ttu-id="11358-139">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11358-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="11358-140">nein</span><span class="sxs-lookup"><span data-stu-id="11358-140">no</span></span>        |
| [<span data-ttu-id="11358-141">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11358-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="11358-142">nein</span><span class="sxs-lookup"><span data-stu-id="11358-142">no</span></span>        |
| [<span data-ttu-id="11358-143">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11358-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="11358-144">nein</span><span class="sxs-lookup"><span data-stu-id="11358-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="11358-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11358-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11358-146">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11358-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





