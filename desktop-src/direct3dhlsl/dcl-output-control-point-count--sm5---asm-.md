---
title: dcl_output_control_point_count (SM5-ASM)
description: Deklariert die Anzahl der Ausgabe Kontrollpunkte des Hull-Shader.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038372"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a><span data-ttu-id="fd213-103">Anzahl der DCL \_ \_ -Ausgabe Kontroll \_ Punkte \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="fd213-103">dcl\_output\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="fd213-104">Deklariert die Anzahl der Ausgabe Kontrollpunkte des Hull-Shader.</span><span class="sxs-lookup"><span data-stu-id="fd213-104">Declares the hull shader output control point count.</span></span>



| <span data-ttu-id="fd213-105">DCL \_ - \_ Ausgabe \_ Kontrollpunkt- \_ Anzahl N</span><span class="sxs-lookup"><span data-stu-id="fd213-105">dcl\_output\_control\_point\_count N</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="fd213-106">Element</span><span class="sxs-lookup"><span data-stu-id="fd213-106">Item</span></span>                                                   | <span data-ttu-id="fd213-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd213-107">Description</span></span>                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd213-108"><span id="N"></span><span id="n"></span>*Nr*</span><span class="sxs-lookup"><span data-stu-id="fd213-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="fd213-109">\[in \] einem ganzzahligen Wert von 0 bis 32, der die Anzahl von Ausgabe Kontrollpunkten angibt.</span><span class="sxs-lookup"><span data-stu-id="fd213-109">\[in\] An integer value from 0 to 32 that specifies the output control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd213-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd213-110">Remarks</span></span>

<span data-ttu-id="fd213-111">Der Hull-Shader kann 0-Kontrollpunkte ausgeben, wenn Sie nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd213-111">The hull shader can output 0 control points if they are not needed.</span></span>

<span data-ttu-id="fd213-112">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="fd213-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fd213-113">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="fd213-113">Vertex</span></span> | <span data-ttu-id="fd213-114">Hülle</span><span class="sxs-lookup"><span data-stu-id="fd213-114">Hull</span></span>                 | <span data-ttu-id="fd213-115">Domain</span><span class="sxs-lookup"><span data-stu-id="fd213-115">Domain</span></span> | <span data-ttu-id="fd213-116">Geometrie</span><span class="sxs-lookup"><span data-stu-id="fd213-116">Geometry</span></span> | <span data-ttu-id="fd213-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="fd213-117">Pixel</span></span> | <span data-ttu-id="fd213-118">Compute</span><span class="sxs-lookup"><span data-stu-id="fd213-118">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="fd213-119">Deklarations Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fd213-119">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fd213-120">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="fd213-120">Minimum Shader Model</span></span>

<span data-ttu-id="fd213-121">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fd213-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="fd213-122">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fd213-122">Shader Model</span></span>                                              | <span data-ttu-id="fd213-123">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd213-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fd213-124">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="fd213-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fd213-125">ja</span><span class="sxs-lookup"><span data-stu-id="fd213-125">yes</span></span>       |
| [<span data-ttu-id="fd213-126">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="fd213-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fd213-127">nein</span><span class="sxs-lookup"><span data-stu-id="fd213-127">no</span></span>        |
| [<span data-ttu-id="fd213-128">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="fd213-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fd213-129">nein</span><span class="sxs-lookup"><span data-stu-id="fd213-129">no</span></span>        |
| [<span data-ttu-id="fd213-130">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd213-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fd213-131">nein</span><span class="sxs-lookup"><span data-stu-id="fd213-131">no</span></span>        |
| [<span data-ttu-id="fd213-132">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd213-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fd213-133">nein</span><span class="sxs-lookup"><span data-stu-id="fd213-133">no</span></span>        |
| [<span data-ttu-id="fd213-134">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd213-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fd213-135">nein</span><span class="sxs-lookup"><span data-stu-id="fd213-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fd213-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd213-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd213-137">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd213-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





