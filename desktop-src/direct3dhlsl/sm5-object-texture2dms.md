---
title: Texture2DMS
description: Texture2DMS Type (wie er in Shader Model 4 vorhanden ist) plus Ressourcenvariablen.
ms.assetid: afda7324-680e-432a-a445-d90bd708e5e0
keywords:
- Texture2DMS HLSL
topic_type:
- apiref
api_name:
- Texture2DMS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c16c69a4fa0fd35ce7b12d69f880daa4b8345d02
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037872"
---
# <a name="texture2dms"></a><span data-ttu-id="ef38b-104">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="ef38b-104">Texture2DMS</span></span>

<span data-ttu-id="ef38b-105">Texture2DMS Type (wie er in Shader Model 4 vorhanden ist) plus Ressourcenvariablen.</span><span class="sxs-lookup"><span data-stu-id="ef38b-105">Texture2DMS type (as it exists in Shader Model 4) plus resource variables.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef38b-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ef38b-106">In this section</span></span>



| <span data-ttu-id="ef38b-107">Thema</span><span class="sxs-lookup"><span data-stu-id="ef38b-107">Topic</span></span>                                                                                    | <span data-ttu-id="ef38b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef38b-108">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef38b-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="ef38b-109">**GetDimensions**</span></span>](sm5-object-texture2dms-getdimensions.md)<br/>                 | <span data-ttu-id="ef38b-110">Gibt die Dimensionen der Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="ef38b-110">Returns the dimensions of the resource.</span></span><br/>                                          |
| [<span data-ttu-id="ef38b-111">**Getsampleposition**</span><span class="sxs-lookup"><span data-stu-id="ef38b-111">**GetSamplePosition**</span></span>](sm5-object-texture2dms-getsampleposition.md)<br/>         | <span data-ttu-id="ef38b-112">Gibt die Beispiel Position für den bereitgestellten Beispiel Index zurück.</span><span class="sxs-lookup"><span data-stu-id="ef38b-112">Returns the sample position for the sample index provided.</span></span><br/>                       |
| [<span data-ttu-id="ef38b-113">**Lade Methoden**</span><span class="sxs-lookup"><span data-stu-id="ef38b-113">**Load methods**</span></span>](texture2dms-load.md)<br/>                                      | <span data-ttu-id="ef38b-114">Ruft einen Wert aus der Ressource an dem Speicherort und dem angegebenen Beispiel Index ab.</span><span class="sxs-lookup"><span data-stu-id="ef38b-114">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="ef38b-115">[**Blutprobe. KOM\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="ef38b-115">[**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span></span><br/> | <span data-ttu-id="ef38b-116">Ruft einen Wert aus der Ressource an dem Speicherort und dem angegebenen Beispiel Index ab.</span><span class="sxs-lookup"><span data-stu-id="ef38b-116">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="ef38b-117">[**KOM\[\]**](sm5-object-texture2dms-operator1.md)</span><span class="sxs-lookup"><span data-stu-id="ef38b-117">[**Operator\[\]**](sm5-object-texture2dms-operator1.md)</span></span><br/>                      | <span data-ttu-id="ef38b-118">Ruft einen Wert aus der Ressource an dem Speicherort ab, der im Beispiel Index 0 angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ef38b-118">Retrieves a value from the resource at the location provided at sample index 0.</span></span> <br/> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ef38b-119">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ef38b-119">Minimum Shader Model</span></span>

<span data-ttu-id="ef38b-120">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef38b-120">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="ef38b-121">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ef38b-121">Shader Model</span></span>              | <span data-ttu-id="ef38b-122">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ef38b-122">Supported</span></span> |
|---------------------------|-----------|
| <span data-ttu-id="ef38b-123">Shadermodell 4 und höher</span><span class="sxs-lookup"><span data-stu-id="ef38b-123">Shader model 4 and higher</span></span> | <span data-ttu-id="ef38b-124">ja</span><span class="sxs-lookup"><span data-stu-id="ef38b-124">yes</span></span>       |



 

<span data-ttu-id="ef38b-125">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ef38b-125">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ef38b-126">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ef38b-126">Vertex</span></span> | <span data-ttu-id="ef38b-127">Hülle</span><span class="sxs-lookup"><span data-stu-id="ef38b-127">Hull</span></span> | <span data-ttu-id="ef38b-128">Domain</span><span class="sxs-lookup"><span data-stu-id="ef38b-128">Domain</span></span> | <span data-ttu-id="ef38b-129">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ef38b-129">Geometry</span></span> | <span data-ttu-id="ef38b-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="ef38b-130">Pixel</span></span> | <span data-ttu-id="ef38b-131">Compute</span><span class="sxs-lookup"><span data-stu-id="ef38b-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ef38b-132">x</span><span class="sxs-lookup"><span data-stu-id="ef38b-132">x</span></span>      | <span data-ttu-id="ef38b-133">x</span><span class="sxs-lookup"><span data-stu-id="ef38b-133">x</span></span>    | <span data-ttu-id="ef38b-134">x</span><span class="sxs-lookup"><span data-stu-id="ef38b-134">x</span></span>      | <span data-ttu-id="ef38b-135">x</span><span class="sxs-lookup"><span data-stu-id="ef38b-135">x</span></span>        | <span data-ttu-id="ef38b-136">x</span><span class="sxs-lookup"><span data-stu-id="ef38b-136">x</span></span>     | <span data-ttu-id="ef38b-137">x</span><span class="sxs-lookup"><span data-stu-id="ef38b-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ef38b-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef38b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef38b-139">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="ef38b-139">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





