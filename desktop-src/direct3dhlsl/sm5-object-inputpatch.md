---
title: Input Patch
description: Stellt ein Array von Steuerungs Punkten dar, die dem Hull-Shader als Eingaben zur Verfügung stehen.
ms.assetid: a2eeb45a-85b2-4ed0-b071-fcbb8abf4f2d
keywords:
- Inputpatch HLSL
topic_type:
- apiref
api_name:
- InputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a882d032133ccb7bc98a34b3ef99551aa18fa51b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992887"
---
# <a name="inputpatch"></a><span data-ttu-id="01a86-104">Input Patch</span><span class="sxs-lookup"><span data-stu-id="01a86-104">InputPatch</span></span>

<span data-ttu-id="01a86-105">Stellt ein Array von Steuerungs Punkten dar, die dem Hull-Shader als Eingaben zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="01a86-105">Represents an array of control points that are available to the hull shader as inputs.</span></span>



| <span data-ttu-id="01a86-106">Methode</span><span class="sxs-lookup"><span data-stu-id="01a86-106">Method</span></span>                                                      | <span data-ttu-id="01a86-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01a86-107">Description</span></span>                         |
|-------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="01a86-108">[**KOM\[\]**](sm5-object-inputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="01a86-108">[**Operator\[\]**](sm5-object-inputpatch-operatorindex.md)</span></span> | <span data-ttu-id="01a86-109">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="01a86-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="01a86-110">Die inputpatch-Klasse unterstützt auch die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="01a86-110">The InputPatch class also supports the following properties:</span></span>



| <span data-ttu-id="01a86-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01a86-111">Properties</span></span> | <span data-ttu-id="01a86-112">type</span><span class="sxs-lookup"><span data-stu-id="01a86-112">Type</span></span> | <span data-ttu-id="01a86-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01a86-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="01a86-114">Länge</span><span class="sxs-lookup"><span data-stu-id="01a86-114">Length</span></span>     | <span data-ttu-id="01a86-115">uint</span><span class="sxs-lookup"><span data-stu-id="01a86-115">uint</span></span> | <span data-ttu-id="01a86-116">Die Anzahl der Kontrollpunkte.</span><span class="sxs-lookup"><span data-stu-id="01a86-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01a86-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="01a86-117">Minimum Shader Model</span></span>

<span data-ttu-id="01a86-118">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01a86-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="01a86-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="01a86-119">Shader Model</span></span>                                                                | <span data-ttu-id="01a86-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="01a86-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="01a86-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="01a86-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="01a86-122">ja</span><span class="sxs-lookup"><span data-stu-id="01a86-122">yes</span></span>       |



 

<span data-ttu-id="01a86-123">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="01a86-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="01a86-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="01a86-124">Vertex</span></span> | <span data-ttu-id="01a86-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="01a86-125">Hull</span></span> | <span data-ttu-id="01a86-126">Domain</span><span class="sxs-lookup"><span data-stu-id="01a86-126">Domain</span></span> | <span data-ttu-id="01a86-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="01a86-127">Geometry</span></span> | <span data-ttu-id="01a86-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="01a86-128">Pixel</span></span> | <span data-ttu-id="01a86-129">Compute</span><span class="sxs-lookup"><span data-stu-id="01a86-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="01a86-130">x</span><span class="sxs-lookup"><span data-stu-id="01a86-130">x</span></span>    |        | <span data-ttu-id="01a86-131">x</span><span class="sxs-lookup"><span data-stu-id="01a86-131">x</span></span>        |       |         |



 

## <a name="see-also"></a><span data-ttu-id="01a86-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01a86-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a86-133">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="01a86-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




