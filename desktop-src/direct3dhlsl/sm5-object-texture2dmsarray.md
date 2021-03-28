---
title: Texture2DMSArray
description: Texture2DMSArray
ms.assetid: 4200eba8-a9e5-41ba-b04c-4ac7b20274d2
keywords:
- Texture2DMSArray HLSL
topic_type:
- apiref
api_name:
- Texture2DMSArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: effe4819c674a7909cc445b9e9f7b5322fae7676
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104218958"
---
# <a name="texture2dmsarray"></a><span data-ttu-id="10d52-104">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="10d52-104">Texture2DMSArray</span></span>

<span data-ttu-id="10d52-105">Texture2DMSArray Type (wie er in Shader Model 4 vorhanden ist) plus Ressourcenvariablen.</span><span class="sxs-lookup"><span data-stu-id="10d52-105">Texture2DMSArray type (as it exists in Shader Model 4) plus resource variables.</span></span>



| <span data-ttu-id="10d52-106">Methode</span><span class="sxs-lookup"><span data-stu-id="10d52-106">Method</span></span>                                                                             | <span data-ttu-id="10d52-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10d52-107">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="10d52-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="10d52-108">**GetDimensions**</span></span>](sm5-object-texture2dmsarray-getdimensions.md)                  | <span data-ttu-id="10d52-109">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="10d52-109">Gets the resource dimensions.</span></span>                      |
| [<span data-ttu-id="10d52-110">**Getsampleposition**</span><span class="sxs-lookup"><span data-stu-id="10d52-110">**GetSamplePosition**</span></span>](sm5-object-texture2dmsarray-getsampleposition.md)          | <span data-ttu-id="10d52-111">Ruft die Position des angegebenen Beispiels ab.</span><span class="sxs-lookup"><span data-stu-id="10d52-111">Gets the position of the specified sample.</span></span>         |
| [<span data-ttu-id="10d52-112">**Laden**</span><span class="sxs-lookup"><span data-stu-id="10d52-112">**Load**</span></span>](texture2dmsarray-load.md)                                               | <span data-ttu-id="10d52-113">Ruft einen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="10d52-113">Gets one value.</span></span>                                    |
| <span data-ttu-id="10d52-114">[**Blutprobe. KOM\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="10d52-114">[**sample.Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span></span>  | <span data-ttu-id="10d52-115">Ruft eine schreibgeschützte Ressourcen Variable ab.</span><span class="sxs-lookup"><span data-stu-id="10d52-115">Gets a read-only resource variable.</span></span>                |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="10d52-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="10d52-116">Minimum Shader Model</span></span>

<span data-ttu-id="10d52-117">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10d52-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="10d52-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="10d52-118">Shader Model</span></span>                                                                | <span data-ttu-id="10d52-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="10d52-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="10d52-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="10d52-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="10d52-121">ja</span><span class="sxs-lookup"><span data-stu-id="10d52-121">yes</span></span>       |



 

<span data-ttu-id="10d52-122">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="10d52-122">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="10d52-123">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="10d52-123">Vertex</span></span> | <span data-ttu-id="10d52-124">Hülle</span><span class="sxs-lookup"><span data-stu-id="10d52-124">Hull</span></span> | <span data-ttu-id="10d52-125">Domain</span><span class="sxs-lookup"><span data-stu-id="10d52-125">Domain</span></span> | <span data-ttu-id="10d52-126">Geometrie</span><span class="sxs-lookup"><span data-stu-id="10d52-126">Geometry</span></span> | <span data-ttu-id="10d52-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="10d52-127">Pixel</span></span> | <span data-ttu-id="10d52-128">Compute</span><span class="sxs-lookup"><span data-stu-id="10d52-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="10d52-129">x</span><span class="sxs-lookup"><span data-stu-id="10d52-129">x</span></span>      | <span data-ttu-id="10d52-130">x</span><span class="sxs-lookup"><span data-stu-id="10d52-130">x</span></span>    | <span data-ttu-id="10d52-131">x</span><span class="sxs-lookup"><span data-stu-id="10d52-131">x</span></span>      | <span data-ttu-id="10d52-132">x</span><span class="sxs-lookup"><span data-stu-id="10d52-132">x</span></span>        | <span data-ttu-id="10d52-133">x</span><span class="sxs-lookup"><span data-stu-id="10d52-133">x</span></span>     | <span data-ttu-id="10d52-134">x</span><span class="sxs-lookup"><span data-stu-id="10d52-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="10d52-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="10d52-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d52-136">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="10d52-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




