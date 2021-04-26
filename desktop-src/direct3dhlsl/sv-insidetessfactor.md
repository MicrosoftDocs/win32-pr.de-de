---
title: SV_InsideTessFactor
description: Definiert den Mosaikbetrag innerhalb einer Patchoberfläche.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d047f7961868de020ac50ffce22b6ce02d078a5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996917"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="cbcae-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="cbcae-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="cbcae-105">Definiert den Mosaikbetrag innerhalb einer Patchoberfläche.</span><span class="sxs-lookup"><span data-stu-id="cbcae-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="cbcae-106">Typ</span><span class="sxs-lookup"><span data-stu-id="cbcae-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="cbcae-107">Typ</span><span class="sxs-lookup"><span data-stu-id="cbcae-107">Type</span></span>       | <span data-ttu-id="cbcae-108">Eingabetopologie</span><span class="sxs-lookup"><span data-stu-id="cbcae-108">Input Topology</span></span> |
| <span data-ttu-id="cbcae-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="cbcae-109">float\[2\]</span></span> | <span data-ttu-id="cbcae-110">Quad-Patch</span><span class="sxs-lookup"><span data-stu-id="cbcae-110">quad patch</span></span>     |
| <span data-ttu-id="cbcae-111">float</span><span class="sxs-lookup"><span data-stu-id="cbcae-111">float</span></span>      | <span data-ttu-id="cbcae-112">Tri Patch</span><span class="sxs-lookup"><span data-stu-id="cbcae-112">tri patch</span></span>      |
| <span data-ttu-id="cbcae-113">unused</span><span class="sxs-lookup"><span data-stu-id="cbcae-113">unused</span></span>     | <span data-ttu-id="cbcae-114">Isoline</span><span class="sxs-lookup"><span data-stu-id="cbcae-114">isoline</span></span>        |



 

<span data-ttu-id="cbcae-115">Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="cbcae-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbcae-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cbcae-116">Remarks</span></span>

<span data-ttu-id="cbcae-117">Dieser Wert muss während der Patchkonstantenfunktion des Hüllen-Shaders definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cbcae-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="cbcae-118">Erforderlicher Ausgabewert für den Hüllen-Shader bei Verwendung von Quad- oder Tri-Patches.</span><span class="sxs-lookup"><span data-stu-id="cbcae-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="cbcae-119">Dieser Wert ist eine erforderliche Eingabe für den Domänen-Shader, damit die Hardware mit den Signaturen über den Mosaikator übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cbcae-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="cbcae-120">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cbcae-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cbcae-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="cbcae-121">Vertex</span></span> | <span data-ttu-id="cbcae-122">Rumpf</span><span class="sxs-lookup"><span data-stu-id="cbcae-122">Hull</span></span> | <span data-ttu-id="cbcae-123">Domain</span><span class="sxs-lookup"><span data-stu-id="cbcae-123">Domain</span></span> | <span data-ttu-id="cbcae-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="cbcae-124">Geometry</span></span> | <span data-ttu-id="cbcae-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="cbcae-125">Pixel</span></span> | <span data-ttu-id="cbcae-126">Compute</span><span class="sxs-lookup"><span data-stu-id="cbcae-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="cbcae-127">x</span><span class="sxs-lookup"><span data-stu-id="cbcae-127">x</span></span>    | <span data-ttu-id="cbcae-128">x</span><span class="sxs-lookup"><span data-stu-id="cbcae-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="cbcae-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cbcae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcae-130">Semantik</span><span class="sxs-lookup"><span data-stu-id="cbcae-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="cbcae-131">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="cbcae-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




