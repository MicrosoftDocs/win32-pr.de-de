---
title: dcl_input vjoininstanceid (SM5-ASM)
description: Deklarieren Sie die Instanz-ID in einer Hull-Shader-joinphase.
ms.assetid: 2EABB24A-7ED7-460D-A2AD-D2C40DCCB2DC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bae9351fc7183aa37cd660c265aab803f4661e9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948332"
---
# <a name="dcl_input-vjoininstanceid-sm5---asm"></a><span data-ttu-id="11b79-103">DCL \_ -Eingabe vjoininstanceid (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="11b79-103">dcl\_input vJoinInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="11b79-104">Deklarieren Sie die Instanz-ID in einer Hull-Shader-joinphase.</span><span class="sxs-lookup"><span data-stu-id="11b79-104">Declare the instance ID in a hull shader join phase.</span></span>



| <span data-ttu-id="11b79-105">DCL \_ -Eingabe vjoininstanceid</span><span class="sxs-lookup"><span data-stu-id="11b79-105">dcl\_input vJoinInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="11b79-106">Element</span><span class="sxs-lookup"><span data-stu-id="11b79-106">Item</span></span>                                                                                                                               | <span data-ttu-id="11b79-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11b79-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="11b79-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vjoininstanceid*</span><span class="sxs-lookup"><span data-stu-id="11b79-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span></span><br/> | <span data-ttu-id="11b79-109">\[in \] der Instanz-ID.</span><span class="sxs-lookup"><span data-stu-id="11b79-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11b79-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11b79-110">Remarks</span></span>

<span data-ttu-id="11b79-111">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="11b79-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="11b79-112">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="11b79-112">Vertex</span></span> | <span data-ttu-id="11b79-113">Hülle</span><span class="sxs-lookup"><span data-stu-id="11b79-113">Hull</span></span> | <span data-ttu-id="11b79-114">Domain</span><span class="sxs-lookup"><span data-stu-id="11b79-114">Domain</span></span> | <span data-ttu-id="11b79-115">Geometrie</span><span class="sxs-lookup"><span data-stu-id="11b79-115">Geometry</span></span> | <span data-ttu-id="11b79-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="11b79-116">Pixel</span></span> | <span data-ttu-id="11b79-117">Compute</span><span class="sxs-lookup"><span data-stu-id="11b79-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="11b79-118">X</span><span class="sxs-lookup"><span data-stu-id="11b79-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11b79-119">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="11b79-119">Minimum Shader Model</span></span>

<span data-ttu-id="11b79-120">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="11b79-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="11b79-121">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="11b79-121">Shader Model</span></span>                                              | <span data-ttu-id="11b79-122">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="11b79-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="11b79-123">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="11b79-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="11b79-124">ja</span><span class="sxs-lookup"><span data-stu-id="11b79-124">yes</span></span>       |
| [<span data-ttu-id="11b79-125">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="11b79-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="11b79-126">nein</span><span class="sxs-lookup"><span data-stu-id="11b79-126">no</span></span>        |
| [<span data-ttu-id="11b79-127">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="11b79-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="11b79-128">nein</span><span class="sxs-lookup"><span data-stu-id="11b79-128">no</span></span>        |
| [<span data-ttu-id="11b79-129">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11b79-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="11b79-130">nein</span><span class="sxs-lookup"><span data-stu-id="11b79-130">no</span></span>        |
| [<span data-ttu-id="11b79-131">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11b79-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="11b79-132">nein</span><span class="sxs-lookup"><span data-stu-id="11b79-132">no</span></span>        |
| [<span data-ttu-id="11b79-133">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11b79-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="11b79-134">nein</span><span class="sxs-lookup"><span data-stu-id="11b79-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="11b79-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11b79-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11b79-136">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="11b79-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





