---
title: dcl_input_control_point_count (SM5-ASM)
description: Deklarieren Sie die Eingabe Steuerungspunkt-Anzahl von Hull-Shader im Abschnitt "Hull Shader Declaration".
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389602"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a><span data-ttu-id="53a5b-103">Anzahl der DCL \_ \_ -Eingabe Kontroll \_ Punkte \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="53a5b-103">dcl\_input\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="53a5b-104">Deklarieren Sie die Eingabe Steuerungspunkt-Anzahl von Hull-Shader im Abschnitt "Hull Shader Declaration".</span><span class="sxs-lookup"><span data-stu-id="53a5b-104">Declare the hull shader input control point count in the hull shader declaration section.</span></span>



| <span data-ttu-id="53a5b-105">DCL- \_ Eingabe \_ Steuerungspunkt- \_ \_ Anzahl {1.. 32}</span><span class="sxs-lookup"><span data-stu-id="53a5b-105">dcl\_input\_control\_point\_count {1..32}</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="53a5b-106">Element</span><span class="sxs-lookup"><span data-stu-id="53a5b-106">Item</span></span>                                                   | <span data-ttu-id="53a5b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53a5b-107">Description</span></span>                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="53a5b-108"><span id="N"></span><span id="n"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="53a5b-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="53a5b-109">\[in \] der Eingabe Steuerungspunkt-Anzahl.</span><span class="sxs-lookup"><span data-stu-id="53a5b-109">\[in\] The input control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53a5b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53a5b-110">Remarks</span></span>

<span data-ttu-id="53a5b-111">Mindestens ein Eingabe Steuerungspunkt ist erforderlich. Sie kann leer sein, wenn Sie nicht benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="53a5b-111">At least 1 input control point is required; it can be empty if it is not needed.</span></span>

<span data-ttu-id="53a5b-112">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="53a5b-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="53a5b-113">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="53a5b-113">Vertex</span></span> | <span data-ttu-id="53a5b-114">Hülle</span><span class="sxs-lookup"><span data-stu-id="53a5b-114">Hull</span></span> | <span data-ttu-id="53a5b-115">Domain</span><span class="sxs-lookup"><span data-stu-id="53a5b-115">Domain</span></span> | <span data-ttu-id="53a5b-116">Geometrie</span><span class="sxs-lookup"><span data-stu-id="53a5b-116">Geometry</span></span> | <span data-ttu-id="53a5b-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="53a5b-117">Pixel</span></span> | <span data-ttu-id="53a5b-118">Compute</span><span class="sxs-lookup"><span data-stu-id="53a5b-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="53a5b-119">X</span><span class="sxs-lookup"><span data-stu-id="53a5b-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="53a5b-120">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="53a5b-120">Minimum Shader Model</span></span>

<span data-ttu-id="53a5b-121">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="53a5b-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="53a5b-122">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="53a5b-122">Shader Model</span></span>                                              | <span data-ttu-id="53a5b-123">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="53a5b-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="53a5b-124">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="53a5b-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="53a5b-125">ja</span><span class="sxs-lookup"><span data-stu-id="53a5b-125">yes</span></span>       |
| [<span data-ttu-id="53a5b-126">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="53a5b-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="53a5b-127">nein</span><span class="sxs-lookup"><span data-stu-id="53a5b-127">no</span></span>        |
| [<span data-ttu-id="53a5b-128">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="53a5b-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="53a5b-129">nein</span><span class="sxs-lookup"><span data-stu-id="53a5b-129">no</span></span>        |
| [<span data-ttu-id="53a5b-130">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53a5b-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="53a5b-131">nein</span><span class="sxs-lookup"><span data-stu-id="53a5b-131">no</span></span>        |
| [<span data-ttu-id="53a5b-132">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53a5b-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="53a5b-133">nein</span><span class="sxs-lookup"><span data-stu-id="53a5b-133">no</span></span>        |
| [<span data-ttu-id="53a5b-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53a5b-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="53a5b-135">nein</span><span class="sxs-lookup"><span data-stu-id="53a5b-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="53a5b-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53a5b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53a5b-137">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53a5b-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





