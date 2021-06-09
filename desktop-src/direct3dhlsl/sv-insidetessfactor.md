---
title: SV_InsideTessFactor
description: Definiert die Mosaikmenge innerhalb einer Patchoberfläche.
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
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826614"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="7cdfc-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="7cdfc-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="7cdfc-105">Definiert die Mosaikmenge innerhalb einer Patchoberfläche.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="7cdfc-106">Typ</span><span class="sxs-lookup"><span data-stu-id="7cdfc-106">Type</span></span>



|  <span data-ttu-id="7cdfc-107">Typ</span><span class="sxs-lookup"><span data-stu-id="7cdfc-107">Type</span></span>          | <span data-ttu-id="7cdfc-108">Eingabetopologie</span><span class="sxs-lookup"><span data-stu-id="7cdfc-108">Input topology</span></span>               |
|------------|----------------|
| <span data-ttu-id="7cdfc-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="7cdfc-109">float\[2\]</span></span> | <span data-ttu-id="7cdfc-110">Quad Patch</span><span class="sxs-lookup"><span data-stu-id="7cdfc-110">quad patch</span></span>     |
| <span data-ttu-id="7cdfc-111">float</span><span class="sxs-lookup"><span data-stu-id="7cdfc-111">float</span></span>      | <span data-ttu-id="7cdfc-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="7cdfc-112">tri patch</span></span>      |
| <span data-ttu-id="7cdfc-113">unused</span><span class="sxs-lookup"><span data-stu-id="7cdfc-113">unused</span></span>     | <span data-ttu-id="7cdfc-114">isoline</span><span class="sxs-lookup"><span data-stu-id="7cdfc-114">isoline</span></span>        |



 

<span data-ttu-id="7cdfc-115">Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cdfc-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7cdfc-116">Remarks</span></span>

<span data-ttu-id="7cdfc-117">Dieser Wert muss während der Patchkonst constant-Funktion des Hüllen-Shaders definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="7cdfc-118">Erforderlicher Ausgabewert für den Hüllen-Shader, wenn Quad- oder Tri-Patches verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="7cdfc-119">Dieser Wert ist eine erforderliche Eingabe für den Domänen-Shader, damit Die Hardware mit den Signaturen über den Mosaik-Shader übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="7cdfc-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="7cdfc-120">Diese Funktion wird in den folgenden Shadertypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7cdfc-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7cdfc-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="7cdfc-121">Vertex</span></span> | <span data-ttu-id="7cdfc-122">Rumpf</span><span class="sxs-lookup"><span data-stu-id="7cdfc-122">Hull</span></span> | <span data-ttu-id="7cdfc-123">Domain</span><span class="sxs-lookup"><span data-stu-id="7cdfc-123">Domain</span></span> | <span data-ttu-id="7cdfc-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="7cdfc-124">Geometry</span></span> | <span data-ttu-id="7cdfc-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="7cdfc-125">Pixel</span></span> | <span data-ttu-id="7cdfc-126">Compute</span><span class="sxs-lookup"><span data-stu-id="7cdfc-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7cdfc-127">x</span><span class="sxs-lookup"><span data-stu-id="7cdfc-127">x</span></span>    | <span data-ttu-id="7cdfc-128">x</span><span class="sxs-lookup"><span data-stu-id="7cdfc-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7cdfc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cdfc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cdfc-130">Semantik</span><span class="sxs-lookup"><span data-stu-id="7cdfc-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="7cdfc-131">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="7cdfc-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




