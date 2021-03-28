---
title: dcl_tessellator_domain (SM5-ASM)
description: Deklarieren Sie die Domäne für den Mosaik Prozess in einem Hull-Shader-Deklarations Abschnitt und dem Domänen-Shader.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389591"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a><span data-ttu-id="90247-103">DCL \_ \_ -Mosaik Domäne (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="90247-103">dcl\_tessellator\_domain (sm5 - asm)</span></span>

<span data-ttu-id="90247-104">Deklarieren Sie die Domäne für den Mosaik Prozess in einem Hull-Shader-Deklarations Abschnitt und dem Domänen-Shader.</span><span class="sxs-lookup"><span data-stu-id="90247-104">Declare the tessellator domain in a hull shader declaration section, and the domain shader.</span></span>



| <span data-ttu-id="90247-105">DCL-Mosaik \_ \_ Domäne {Domänen \_ Isolat </span><span class="sxs-lookup"><span data-stu-id="90247-105">dcl\_tessellator\_domain {domain\_isoline </span></span>\| <span data-ttu-id="90247-106">Domäne \_ Tri </span><span class="sxs-lookup"><span data-stu-id="90247-106">domain\_tri </span></span>\| <span data-ttu-id="90247-107">Domäne \_ Quad}</span><span class="sxs-lookup"><span data-stu-id="90247-107">domain\_quad}</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="90247-108">Element</span><span class="sxs-lookup"><span data-stu-id="90247-108">Item</span></span>                                                                                                                                                                                | <span data-ttu-id="90247-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90247-109">Description</span></span>                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="90247-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*Domäne \_ isolin \| Domäne \_ Tri \| Domäne \_ Quad*</span><span class="sxs-lookup"><span data-stu-id="90247-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain\_isoline \| domain\_tri \| domain\_quad*</span></span><br/> | <span data-ttu-id="90247-111">\[in \] der Domäne.</span><span class="sxs-lookup"><span data-stu-id="90247-111">\[in\] The domain.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90247-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90247-112">Remarks</span></span>

<span data-ttu-id="90247-113">Das Verhalten ist nicht definiert, wenn der Hull-Shader und der Domänen-Shader nicht übereinstimmende Domänen oder andere widersprüchliche Abweichungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="90247-113">Behavior is undefined if the hull shader and domain shader provide mismatching domains or any other conflicting decalarations.</span></span>

<span data-ttu-id="90247-114">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="90247-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="90247-115">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="90247-115">Vertex</span></span> | <span data-ttu-id="90247-116">Hülle</span><span class="sxs-lookup"><span data-stu-id="90247-116">Hull</span></span>                 | <span data-ttu-id="90247-117">Domain</span><span class="sxs-lookup"><span data-stu-id="90247-117">Domain</span></span> | <span data-ttu-id="90247-118">Geometrie</span><span class="sxs-lookup"><span data-stu-id="90247-118">Geometry</span></span> | <span data-ttu-id="90247-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="90247-119">Pixel</span></span> | <span data-ttu-id="90247-120">Compute</span><span class="sxs-lookup"><span data-stu-id="90247-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="90247-121">Deklarations Abschnitt</span><span class="sxs-lookup"><span data-stu-id="90247-121">Declarations Section</span></span> | <span data-ttu-id="90247-122">X</span><span class="sxs-lookup"><span data-stu-id="90247-122">X</span></span>      |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="90247-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="90247-123">Minimum Shader Model</span></span>

<span data-ttu-id="90247-124">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="90247-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="90247-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="90247-125">Shader Model</span></span>                                              | <span data-ttu-id="90247-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="90247-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="90247-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="90247-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="90247-128">ja</span><span class="sxs-lookup"><span data-stu-id="90247-128">yes</span></span>       |
| [<span data-ttu-id="90247-129">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="90247-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="90247-130">nein</span><span class="sxs-lookup"><span data-stu-id="90247-130">no</span></span>        |
| [<span data-ttu-id="90247-131">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="90247-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="90247-132">nein</span><span class="sxs-lookup"><span data-stu-id="90247-132">no</span></span>        |
| [<span data-ttu-id="90247-133">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90247-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="90247-134">nein</span><span class="sxs-lookup"><span data-stu-id="90247-134">no</span></span>        |
| [<span data-ttu-id="90247-135">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90247-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="90247-136">nein</span><span class="sxs-lookup"><span data-stu-id="90247-136">no</span></span>        |
| [<span data-ttu-id="90247-137">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90247-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="90247-138">nein</span><span class="sxs-lookup"><span data-stu-id="90247-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="90247-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90247-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90247-140">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90247-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





