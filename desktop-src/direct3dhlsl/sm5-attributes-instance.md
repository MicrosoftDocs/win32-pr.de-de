---
title: instance
description: Verwenden Sie dieses Attribut, um einen Geometry-Shader zu verwenden.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038353"
---
# <a name="instance"></a><span data-ttu-id="84262-103">instance</span><span class="sxs-lookup"><span data-stu-id="84262-103">instance</span></span>

<span data-ttu-id="84262-104">Verwenden Sie dieses Attribut, um einen Geometry-Shader zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84262-104">Use this attribute to instance a geometry shader.</span></span>


```
instance(X)   
```



## <a name="remarks"></a><span data-ttu-id="84262-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84262-105">Remarks</span></span>

<span data-ttu-id="84262-106">X ist ein ganzzahliger Index, der die Anzahl der Instanzen angibt, die für jedes gezeichnete Element ausgeführt werden sollen (z. b. für jedes Dreieck).</span><span class="sxs-lookup"><span data-stu-id="84262-106">X is an integer index that indicates the number of instances to be executed for each drawn item (for example, for each triangle).</span></span> <span data-ttu-id="84262-107">Verwenden Sie bei Verwendung dieses Attributs [SV \_ gsinstanceid](sv-gsinstanceid.md) , um zu ermitteln, welche Instanz eines Geometry-Shaders ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84262-107">When using this attribute, use [SV\_GSInstanceID](sv-gsinstanceid.md) to identify which instance of a geometry shader is being executed.</span></span>

<span data-ttu-id="84262-108">Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="84262-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="84262-109">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="84262-109">Vertex</span></span> | <span data-ttu-id="84262-110">Hülle</span><span class="sxs-lookup"><span data-stu-id="84262-110">Hull</span></span> | <span data-ttu-id="84262-111">Domain</span><span class="sxs-lookup"><span data-stu-id="84262-111">Domain</span></span> | <span data-ttu-id="84262-112">Geometrie</span><span class="sxs-lookup"><span data-stu-id="84262-112">Geometry</span></span> | <span data-ttu-id="84262-113">Pixel</span><span class="sxs-lookup"><span data-stu-id="84262-113">Pixel</span></span> | <span data-ttu-id="84262-114">Compute</span><span class="sxs-lookup"><span data-stu-id="84262-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="84262-115">x</span><span class="sxs-lookup"><span data-stu-id="84262-115">x</span></span>        |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="84262-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84262-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84262-117">Shader Model 5-Attribute</span><span class="sxs-lookup"><span data-stu-id="84262-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="84262-118">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="84262-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




