---
title: Outputpatch
description: Outputpatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- Outputpatch HLSL
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037832"
---
# <a name="outputpatch"></a><span data-ttu-id="419a1-104">Outputpatch</span><span class="sxs-lookup"><span data-stu-id="419a1-104">OutputPatch</span></span>

<span data-ttu-id="419a1-105">Stellt ein Array von Ausgabe Steuerungs Punkten dar, die für die Patch-Konstante-Funktion des Hull-Shader sowie für den Domänen-Shader verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="419a1-105">Represents an array of output control points that are available to the hull shader's patch-constant function as well as the domain shader.</span></span>



| <span data-ttu-id="419a1-106">Methode</span><span class="sxs-lookup"><span data-stu-id="419a1-106">Method</span></span>                                                       | <span data-ttu-id="419a1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="419a1-107">Description</span></span>                         |
|--------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="419a1-108">[**KOM\[\]**](sm5-object-outputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="419a1-108">[**Operator\[\]**](sm5-object-outputpatch-operatorindex.md)</span></span> | <span data-ttu-id="419a1-109">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="419a1-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="419a1-110">Außerdem unterstützt die inputpatch-Klasse die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="419a1-110">In addition, the InputPatch class supports the following properties:</span></span>



| <span data-ttu-id="419a1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="419a1-111">Properties</span></span> | <span data-ttu-id="419a1-112">type</span><span class="sxs-lookup"><span data-stu-id="419a1-112">Type</span></span> | <span data-ttu-id="419a1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="419a1-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="419a1-114">Länge</span><span class="sxs-lookup"><span data-stu-id="419a1-114">Length</span></span>     | <span data-ttu-id="419a1-115">uint</span><span class="sxs-lookup"><span data-stu-id="419a1-115">uint</span></span> | <span data-ttu-id="419a1-116">Die Anzahl der Kontrollpunkte.</span><span class="sxs-lookup"><span data-stu-id="419a1-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="419a1-117">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="419a1-117">Minimum Shader Model</span></span>

<span data-ttu-id="419a1-118">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="419a1-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="419a1-119">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="419a1-119">Shader Model</span></span>                                                                | <span data-ttu-id="419a1-120">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="419a1-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="419a1-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="419a1-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="419a1-122">ja</span><span class="sxs-lookup"><span data-stu-id="419a1-122">yes</span></span>       |



 

<span data-ttu-id="419a1-123">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="419a1-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="419a1-124">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="419a1-124">Vertex</span></span> | <span data-ttu-id="419a1-125">Hülle</span><span class="sxs-lookup"><span data-stu-id="419a1-125">Hull</span></span> | <span data-ttu-id="419a1-126">Domain</span><span class="sxs-lookup"><span data-stu-id="419a1-126">Domain</span></span> | <span data-ttu-id="419a1-127">Geometrie</span><span class="sxs-lookup"><span data-stu-id="419a1-127">Geometry</span></span> | <span data-ttu-id="419a1-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="419a1-128">Pixel</span></span> | <span data-ttu-id="419a1-129">Compute</span><span class="sxs-lookup"><span data-stu-id="419a1-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="419a1-130">x</span><span class="sxs-lookup"><span data-stu-id="419a1-130">x</span></span>    | <span data-ttu-id="419a1-131">x</span><span class="sxs-lookup"><span data-stu-id="419a1-131">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="419a1-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="419a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419a1-133">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="419a1-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




