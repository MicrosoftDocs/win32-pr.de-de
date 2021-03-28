---
title: earlydepthstencil
description: Erzwingt tiefen Schablonen Tests, bevor ein Shader ausgeführt wird.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993183"
---
# <a name="earlydepthstencil"></a><span data-ttu-id="91ccc-103">earlydepthstencil</span><span class="sxs-lookup"><span data-stu-id="91ccc-103">earlydepthstencil</span></span>

<span data-ttu-id="91ccc-104">Erzwingt tiefen Schablonen Tests, bevor ein Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91ccc-104">Forces depth-stencil testing before a shader executes.</span></span>


```
earlydepthstencil   
```



## <a name="remarks"></a><span data-ttu-id="91ccc-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91ccc-105">Remarks</span></span>

<span data-ttu-id="91ccc-106">Das Testen der tiefen Schablone erfolgt in der Regel während der Pixel Verarbeitung durch einen PixelShader.</span><span class="sxs-lookup"><span data-stu-id="91ccc-106">Depth-stencil testing is normally done during pixel processing by a pixel shader.</span></span> <span data-ttu-id="91ccc-107">Durch das Erzwingen einer frühen Tiefe der Schablone werden die Tests vor der Ausführung des Shaders durchgeführt. der Zweck besteht darin, die Leistung pro Pixel zu verbessern, indem eine nicht benötigte Pixel Verarbeitung durchgeführt/reduziert/vermieden wird.</span><span class="sxs-lookup"><span data-stu-id="91ccc-107">Forcing early depth-stencil testing causes the testing to be done prior to the shader execution; the purpose is to improve per-pixel performance by culling/reducing/avoiding unnecessary pixel processing.</span></span>

<span data-ttu-id="91ccc-108">Eine Anwendung kann eine frühe tiefen Schablone durch Bereitstellen des-Attributs erzwingen, oder die Hardware kann frühe tiefen Tests ausführen, wenn keine tiefen Werte geschrieben werden und keine ungeordneten Zugriffs Vorgänge in einem Shader als Optimierung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="91ccc-108">An application can force early depth-stencil testing by supplying the attribute or the hardware may execute early depth-stencil testing provided no depth values are written and no unordered access operations are performed in a shader as an optimization.</span></span>

<span data-ttu-id="91ccc-109">Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="91ccc-109">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="91ccc-110">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="91ccc-110">Vertex</span></span> | <span data-ttu-id="91ccc-111">Hülle</span><span class="sxs-lookup"><span data-stu-id="91ccc-111">Hull</span></span> | <span data-ttu-id="91ccc-112">Domain</span><span class="sxs-lookup"><span data-stu-id="91ccc-112">Domain</span></span> | <span data-ttu-id="91ccc-113">Geometrie</span><span class="sxs-lookup"><span data-stu-id="91ccc-113">Geometry</span></span> | <span data-ttu-id="91ccc-114">Pixel</span><span class="sxs-lookup"><span data-stu-id="91ccc-114">Pixel</span></span> | <span data-ttu-id="91ccc-115">Compute</span><span class="sxs-lookup"><span data-stu-id="91ccc-115">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="91ccc-116">x</span><span class="sxs-lookup"><span data-stu-id="91ccc-116">x</span></span>     |         |



 

## <a name="related-topics"></a><span data-ttu-id="91ccc-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91ccc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ccc-118">Shader Model 5-Attribute</span><span class="sxs-lookup"><span data-stu-id="91ccc-118">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="91ccc-119">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="91ccc-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




