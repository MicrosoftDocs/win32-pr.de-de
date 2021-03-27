---
title: maxtess Factor
description: Gibt den maximalen Wert an, den der Hull-Shader für jeden Mosaik Faktor zurückgeben würde.
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857792"
---
# <a name="maxtessfactor"></a><span data-ttu-id="01840-103">maxtess Factor</span><span class="sxs-lookup"><span data-stu-id="01840-103">maxtessfactor</span></span>

<span data-ttu-id="01840-104">Gibt den maximalen Wert an, den der Hull-Shader für jeden Mosaik Faktor zurückgeben würde.</span><span class="sxs-lookup"><span data-stu-id="01840-104">Indicates the maximum value that the hull shader would return for any tessellation factor.</span></span>


```
maxtessfactor(X)   
```



## <a name="remarks"></a><span data-ttu-id="01840-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01840-105">Remarks</span></span>

<span data-ttu-id="01840-106">Mit diesem Attribut wird eine obere Grenze für die angeforderte Mosaik Menge festgelegt, um einem Treiber zu helfen, die maximale Menge an Ressourcen festzulegen, die für das Mosaik benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="01840-106">This attribute puts an upper bound on the amount of tessellation requested to help a driver determine the maximum amount of resources required for tessellation.</span></span>

<span data-ttu-id="01840-107">Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="01840-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="01840-108">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="01840-108">Vertex</span></span> | <span data-ttu-id="01840-109">Hülle</span><span class="sxs-lookup"><span data-stu-id="01840-109">Hull</span></span> | <span data-ttu-id="01840-110">Domain</span><span class="sxs-lookup"><span data-stu-id="01840-110">Domain</span></span> | <span data-ttu-id="01840-111">Geometrie</span><span class="sxs-lookup"><span data-stu-id="01840-111">Geometry</span></span> | <span data-ttu-id="01840-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="01840-112">Pixel</span></span> | <span data-ttu-id="01840-113">Compute</span><span class="sxs-lookup"><span data-stu-id="01840-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="01840-114">x</span><span class="sxs-lookup"><span data-stu-id="01840-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="01840-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01840-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01840-116">Shader Model 5-Attribute</span><span class="sxs-lookup"><span data-stu-id="01840-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="01840-117">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="01840-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




