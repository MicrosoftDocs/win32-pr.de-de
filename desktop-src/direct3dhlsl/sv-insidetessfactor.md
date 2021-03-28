---
title: SV_InsideTessFactor
description: Definiert den Mosaik Betrag innerhalb einer patchoberfläche.
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
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976209"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="29a9b-104">SV \_ insidetess Factor</span><span class="sxs-lookup"><span data-stu-id="29a9b-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="29a9b-105">Definiert den Mosaik Betrag innerhalb einer patchoberfläche.</span><span class="sxs-lookup"><span data-stu-id="29a9b-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="29a9b-106">Typ</span><span class="sxs-lookup"><span data-stu-id="29a9b-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="29a9b-107">Typ</span><span class="sxs-lookup"><span data-stu-id="29a9b-107">Type</span></span>       | <span data-ttu-id="29a9b-108">Eingabe Topologie</span><span class="sxs-lookup"><span data-stu-id="29a9b-108">Input Topology</span></span> |
| <span data-ttu-id="29a9b-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="29a9b-109">float\[2\]</span></span> | <span data-ttu-id="29a9b-110">Quad-Patch</span><span class="sxs-lookup"><span data-stu-id="29a9b-110">quad patch</span></span>     |
| <span data-ttu-id="29a9b-111">float</span><span class="sxs-lookup"><span data-stu-id="29a9b-111">float</span></span>      | <span data-ttu-id="29a9b-112">Tri-Patch</span><span class="sxs-lookup"><span data-stu-id="29a9b-112">tri patch</span></span>      |
| <span data-ttu-id="29a9b-113">unused</span><span class="sxs-lookup"><span data-stu-id="29a9b-113">unused</span></span>     | <span data-ttu-id="29a9b-114">Isolation</span><span class="sxs-lookup"><span data-stu-id="29a9b-114">isoline</span></span>        |



 

<span data-ttu-id="29a9b-115">Mosaik Faktoren müssen als Array deklariert werden. Sie können nicht in einen einzigen Vektor gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="29a9b-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="29a9b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29a9b-116">Remarks</span></span>

<span data-ttu-id="29a9b-117">Dieser Wert muss während der Funktion Patch Constant des Hull-Shaders definiert werden.</span><span class="sxs-lookup"><span data-stu-id="29a9b-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="29a9b-118">Erforderlicher Ausgabewert für den Hull-Shader bei Verwendung von Quad-oder Tri-Patches.</span><span class="sxs-lookup"><span data-stu-id="29a9b-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="29a9b-119">Bei diesem Wert handelt es sich um eine erforderliche Eingabe für den Domänen-Shader, damit die Hardware die Signaturen über den Mosaik Prozess abgleichen kann.</span><span class="sxs-lookup"><span data-stu-id="29a9b-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="29a9b-120">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="29a9b-120">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="29a9b-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="29a9b-121">Vertex</span></span> | <span data-ttu-id="29a9b-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="29a9b-122">Hull</span></span> | <span data-ttu-id="29a9b-123">Domain</span><span class="sxs-lookup"><span data-stu-id="29a9b-123">Domain</span></span> | <span data-ttu-id="29a9b-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="29a9b-124">Geometry</span></span> | <span data-ttu-id="29a9b-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="29a9b-125">Pixel</span></span> | <span data-ttu-id="29a9b-126">Compute</span><span class="sxs-lookup"><span data-stu-id="29a9b-126">Compute</span></span> |
|        | <span data-ttu-id="29a9b-127">x</span><span class="sxs-lookup"><span data-stu-id="29a9b-127">x</span></span>    | <span data-ttu-id="29a9b-128">x</span><span class="sxs-lookup"><span data-stu-id="29a9b-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="29a9b-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="29a9b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a9b-130">Semantik</span><span class="sxs-lookup"><span data-stu-id="29a9b-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="29a9b-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="29a9b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




