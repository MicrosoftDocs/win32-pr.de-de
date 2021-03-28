---
title: dcl_tessellator_output_primitive (SM5-ASM)
description: Deklarieren Sie den primitiven Typ der Mosaik Ausgabe in einem Hull-Shader-Deklarations Abschnitt.
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038368"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a><span data-ttu-id="f66b8-103">DCL \_ \_ \_ -Mosaik-Ausgabe primitive (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f66b8-103">dcl\_tessellator\_output\_primitive (sm5 - asm)</span></span>

<span data-ttu-id="f66b8-104">Deklarieren Sie den primitiven Typ der Mosaik Ausgabe in einem Hull-Shader-Deklarations Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="f66b8-104">Declare the tessellator output primitive type in a hull shader declaration section.</span></span>



| <span data-ttu-id="f66b8-105">DCL-Mosaik \_ \_ Ausgabe \_ primitive {Ausgabe \_ Punkt </span><span class="sxs-lookup"><span data-stu-id="f66b8-105">dcl\_tessellator\_output\_primitive {output\_point </span></span>\| <span data-ttu-id="f66b8-106">Ausgabe \_ Zeile </span><span class="sxs-lookup"><span data-stu-id="f66b8-106">output\_line </span></span>\| <span data-ttu-id="f66b8-107">ausgabeausgabe \_ e \_ CW </span><span class="sxs-lookup"><span data-stu-id="f66b8-107">triangloutput\_e\_cw </span></span>\| <span data-ttu-id="f66b8-108">Ausgabe \_ Dreieck \_ CCW}</span><span class="sxs-lookup"><span data-stu-id="f66b8-108">output\_triangle\_ccw}</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f66b8-109">Element</span><span class="sxs-lookup"><span data-stu-id="f66b8-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="f66b8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f66b8-110">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="f66b8-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*Ausgabe \_ Punkt \| Ausgabe \_ Zeile \| triangloutput \_ e \_ CW \| Ausgabe \_ Dreieck \_ CCW*</span><span class="sxs-lookup"><span data-stu-id="f66b8-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*output\_point \| output\_line \| triangloutput\_e\_cw \| output\_triangle\_ccw*</span></span><br/> | <span data-ttu-id="f66b8-112">\[im \] Ausgabe primitiven Typ.</span><span class="sxs-lookup"><span data-stu-id="f66b8-112">\[in\] The output primitive type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f66b8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f66b8-113">Remarks</span></span>

<span data-ttu-id="f66b8-114">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="f66b8-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f66b8-115">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f66b8-115">Vertex</span></span> | <span data-ttu-id="f66b8-116">Hülle</span><span class="sxs-lookup"><span data-stu-id="f66b8-116">Hull</span></span>                 | <span data-ttu-id="f66b8-117">Domain</span><span class="sxs-lookup"><span data-stu-id="f66b8-117">Domain</span></span> | <span data-ttu-id="f66b8-118">Geometrie</span><span class="sxs-lookup"><span data-stu-id="f66b8-118">Geometry</span></span> | <span data-ttu-id="f66b8-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="f66b8-119">Pixel</span></span> | <span data-ttu-id="f66b8-120">Compute</span><span class="sxs-lookup"><span data-stu-id="f66b8-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="f66b8-121">Deklarations Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f66b8-121">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f66b8-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="f66b8-122">Minimum Shader Model</span></span>

<span data-ttu-id="f66b8-123">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f66b8-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f66b8-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="f66b8-124">Shader Model</span></span>                                              | <span data-ttu-id="f66b8-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="f66b8-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f66b8-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="f66b8-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f66b8-127">ja</span><span class="sxs-lookup"><span data-stu-id="f66b8-127">yes</span></span>       |
| [<span data-ttu-id="f66b8-128">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="f66b8-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f66b8-129">nein</span><span class="sxs-lookup"><span data-stu-id="f66b8-129">no</span></span>        |
| [<span data-ttu-id="f66b8-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="f66b8-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f66b8-131">nein</span><span class="sxs-lookup"><span data-stu-id="f66b8-131">no</span></span>        |
| [<span data-ttu-id="f66b8-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f66b8-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f66b8-133">nein</span><span class="sxs-lookup"><span data-stu-id="f66b8-133">no</span></span>        |
| [<span data-ttu-id="f66b8-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f66b8-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f66b8-135">nein</span><span class="sxs-lookup"><span data-stu-id="f66b8-135">no</span></span>        |
| [<span data-ttu-id="f66b8-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f66b8-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f66b8-137">nein</span><span class="sxs-lookup"><span data-stu-id="f66b8-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f66b8-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f66b8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f66b8-139">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f66b8-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





