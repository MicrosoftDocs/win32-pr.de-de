---
description: Definiert einen Satz von zwei booleschen Werten, die in der meshfacewrapper-Vorlage verwendet werden, um die Textur Topologie eines einzelnen Gesichts zu definieren. Verwenden Sie anstelle von Boolean2d, wenn die Texturkoordinaten (u, v) den Bereich von 0 bis 2 anstelle von 0 bis 1 umfassen.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: Materialwrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340066"
---
# <a name="materialwrap"></a><span data-ttu-id="a4dc2-104">Materialwrap</span><span class="sxs-lookup"><span data-stu-id="a4dc2-104">MaterialWrap</span></span>

<span data-ttu-id="a4dc2-105">Definiert einen Satz von zwei booleschen Werten, die in der [**meshfacewrapper**](meshfacewraps.md) -Vorlage verwendet werden, um die Textur Topologie eines einzelnen Gesichts zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a4dc2-105">Defines a set of two Boolean values used in the [**MeshFaceWraps**](meshfacewraps.md) template to define the texture topology of an individual face.</span></span> <span data-ttu-id="a4dc2-106">Verwenden Sie anstelle von [**Boolean2d**](boolean2d.md) , wenn die Texturkoordinaten (u, v) den Bereich von 0 bis 2 anstelle von 0 bis 1 umfassen.</span><span class="sxs-lookup"><span data-stu-id="a4dc2-106">Use instead of [**Boolean2d**](boolean2d.md) when the texture coordinates (u, v) span the range of 0 to 2 instead of 0 to 1.</span></span>

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

<span data-ttu-id="a4dc2-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="a4dc2-107">Where:</span></span>

-   <span data-ttu-id="a4dc2-108">u-boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="a4dc2-108">u - Boolean value.</span></span> <span data-ttu-id="a4dc2-109">Siehe [**Boolean**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="a4dc2-109">See [**Boolean**](boolean.md).</span></span>
-   <span data-ttu-id="a4dc2-110">v-boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="a4dc2-110">v - Boolean value.</span></span> <span data-ttu-id="a4dc2-111">Siehe [**Boolean**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="a4dc2-111">See [**Boolean**](boolean.md).</span></span>

> [!Note]  
> <span data-ttu-id="a4dc2-112">Die Vorlage " [**meshfacewrapper**](meshfacewraps.md) " wird nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4dc2-112">The [**MeshFaceWraps**](meshfacewraps.md) template is no longer used.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a4dc2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4dc2-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4dc2-114">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="a4dc2-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



