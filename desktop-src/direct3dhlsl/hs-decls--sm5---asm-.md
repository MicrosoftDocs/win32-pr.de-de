---
title: hs_decls (SM5-ASM)
description: Startet die Deklarations Phase in einem Hull-Shader.
ms.assetid: 1C8552B1-F649-4B73-A365-D449A9121DAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e57207e35aab507a1404efaf90131a9648918ae7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101102"
---
# <a name="hs_decls-sm5---asm"></a><span data-ttu-id="eecd3-103">HS \_ decls (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="eecd3-103">hs\_decls (sm5 - asm)</span></span>

<span data-ttu-id="eecd3-104">Startet die Deklarations Phase in einem Hull-Shader.</span><span class="sxs-lookup"><span data-stu-id="eecd3-104">Start the declarations phase in a hull shader.</span></span>



| <span data-ttu-id="eecd3-105">HS- \_ decls</span><span class="sxs-lookup"><span data-stu-id="eecd3-105">hs\_decls</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="eecd3-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eecd3-106">Remarks</span></span>

<span data-ttu-id="eecd3-107">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="eecd3-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eecd3-108">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="eecd3-108">Vertex</span></span> | <span data-ttu-id="eecd3-109">Hülle</span><span class="sxs-lookup"><span data-stu-id="eecd3-109">Hull</span></span> | <span data-ttu-id="eecd3-110">Domain</span><span class="sxs-lookup"><span data-stu-id="eecd3-110">Domain</span></span> | <span data-ttu-id="eecd3-111">Geometrie</span><span class="sxs-lookup"><span data-stu-id="eecd3-111">Geometry</span></span> | <span data-ttu-id="eecd3-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="eecd3-112">Pixel</span></span> | <span data-ttu-id="eecd3-113">Compute</span><span class="sxs-lookup"><span data-stu-id="eecd3-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="eecd3-114">X</span><span class="sxs-lookup"><span data-stu-id="eecd3-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eecd3-115">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="eecd3-115">Minimum Shader Model</span></span>

<span data-ttu-id="eecd3-116">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="eecd3-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="eecd3-117">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="eecd3-117">Shader Model</span></span>                                              | <span data-ttu-id="eecd3-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="eecd3-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eecd3-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="eecd3-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eecd3-120">ja</span><span class="sxs-lookup"><span data-stu-id="eecd3-120">yes</span></span>       |
| [<span data-ttu-id="eecd3-121">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="eecd3-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eecd3-122">nein</span><span class="sxs-lookup"><span data-stu-id="eecd3-122">no</span></span>        |
| [<span data-ttu-id="eecd3-123">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="eecd3-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eecd3-124">nein</span><span class="sxs-lookup"><span data-stu-id="eecd3-124">no</span></span>        |
| [<span data-ttu-id="eecd3-125">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eecd3-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eecd3-126">nein</span><span class="sxs-lookup"><span data-stu-id="eecd3-126">no</span></span>        |
| [<span data-ttu-id="eecd3-127">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eecd3-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eecd3-128">nein</span><span class="sxs-lookup"><span data-stu-id="eecd3-128">no</span></span>        |
| [<span data-ttu-id="eecd3-129">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eecd3-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eecd3-130">nein</span><span class="sxs-lookup"><span data-stu-id="eecd3-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eecd3-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eecd3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eecd3-132">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eecd3-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




