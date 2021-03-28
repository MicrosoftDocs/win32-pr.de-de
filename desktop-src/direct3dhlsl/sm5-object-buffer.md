---
title: Buffer
description: Buffer
ms.assetid: 7f552b9b-c5fb-4bc2-a7ae-61983379db38
keywords:
- Puffer-HLSL
topic_type:
- apiref
api_name:
- Buffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1754272fd90cedc5a806543dd83a99cdcd9455
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389250"
---
# <a name="buffer"></a><span data-ttu-id="3a2f6-104">Buffer</span><span class="sxs-lookup"><span data-stu-id="3a2f6-104">Buffer</span></span>

<span data-ttu-id="3a2f6-105">Der Puffertyp, wie er in Shader Model 4 und Ressourcenvariablen und Puffer Info vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3a2f6-105">Buffer type as it exists in Shader Model 4 plus resource variables and buffer info.</span></span>



| <span data-ttu-id="3a2f6-106">Methode</span><span class="sxs-lookup"><span data-stu-id="3a2f6-106">Method</span></span>                                                   | <span data-ttu-id="3a2f6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a2f6-107">Description</span></span>                         |
|----------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="3a2f6-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="3a2f6-108">**GetDimensions**</span></span>](sm5-object-buffer-getdimensions.md) | <span data-ttu-id="3a2f6-109">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="3a2f6-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="3a2f6-110">**Laden**</span><span class="sxs-lookup"><span data-stu-id="3a2f6-110">**Load**</span></span>](buffer-load.md)                              | <span data-ttu-id="3a2f6-111">Liest Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="3a2f6-111">Reads buffer data.</span></span>                  |
| <span data-ttu-id="3a2f6-112">[**KOM\[\]**](sm5-object-buffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="3a2f6-112">[**Operator\[\]**](sm5-object-buffer-operatorindex.md)</span></span>  | <span data-ttu-id="3a2f6-113">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="3a2f6-113">Gets a read-only resource variable.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a2f6-114">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="3a2f6-114">Minimum Shader Model</span></span>

<span data-ttu-id="3a2f6-115">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a2f6-115">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="3a2f6-116">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="3a2f6-116">Shader Model</span></span>                                                                | <span data-ttu-id="3a2f6-117">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="3a2f6-117">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3a2f6-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="3a2f6-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3a2f6-119">ja</span><span class="sxs-lookup"><span data-stu-id="3a2f6-119">yes</span></span>       |



 

<span data-ttu-id="3a2f6-120">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3a2f6-120">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3a2f6-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="3a2f6-121">Vertex</span></span> | <span data-ttu-id="3a2f6-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="3a2f6-122">Hull</span></span> | <span data-ttu-id="3a2f6-123">Domain</span><span class="sxs-lookup"><span data-stu-id="3a2f6-123">Domain</span></span> | <span data-ttu-id="3a2f6-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="3a2f6-124">Geometry</span></span> | <span data-ttu-id="3a2f6-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="3a2f6-125">Pixel</span></span> | <span data-ttu-id="3a2f6-126">Compute</span><span class="sxs-lookup"><span data-stu-id="3a2f6-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3a2f6-127">x</span><span class="sxs-lookup"><span data-stu-id="3a2f6-127">x</span></span>      | <span data-ttu-id="3a2f6-128">x</span><span class="sxs-lookup"><span data-stu-id="3a2f6-128">x</span></span>    | <span data-ttu-id="3a2f6-129">x</span><span class="sxs-lookup"><span data-stu-id="3a2f6-129">x</span></span>      | <span data-ttu-id="3a2f6-130">x</span><span class="sxs-lookup"><span data-stu-id="3a2f6-130">x</span></span>        | <span data-ttu-id="3a2f6-131">x</span><span class="sxs-lookup"><span data-stu-id="3a2f6-131">x</span></span>     | <span data-ttu-id="3a2f6-132">x</span><span class="sxs-lookup"><span data-stu-id="3a2f6-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3a2f6-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a2f6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2f6-134">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="3a2f6-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




