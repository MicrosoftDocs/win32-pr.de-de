---
description: Wird von einem beliebigen Treffer-Shader aufgerufen, um den Treffer zu verwerfen und den Shader zu beenden.
ms.assetid: ''
title: IgnoreHit-Funktion
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343615"
---
# <a name="ignorehit-function"></a><span data-ttu-id="b1d0e-103">IgnoreHit-Funktion</span><span class="sxs-lookup"><span data-stu-id="b1d0e-103">IgnoreHit function</span></span>

<span data-ttu-id="b1d0e-104">Wird von einem [beliebigen Treffer-Shader](any-hit-shader.md) aufgerufen, um den Treffer zu verwerfen und den Shader zu beenden.</span><span class="sxs-lookup"><span data-stu-id="b1d0e-104">Called from an [any hit shader](any-hit-shader.md) to reject the hit and end the shader.</span></span> <span data-ttu-id="b1d0e-105">Die Treffer Suche wird fortgesetzt, ohne dass der Abstand und die Attribute für den aktuellen Treffer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b1d0e-105">The hit search continues on without committing the distance and attributes for the current hit.</span></span>  <span data-ttu-id="b1d0e-106">Der [**reporthit**](reporthit-function.md) -Befehl wird im [schnittsshader](intersection-shader.md)aufgerufen, falls vorhanden, gibt false zurück.</span><span class="sxs-lookup"><span data-stu-id="b1d0e-106">The [**ReportHit**](reporthit-function.md) call in the [intersection shader](intersection-shader.md), if there is one, will return false.</span></span>  <span data-ttu-id="b1d0e-107">Alle Änderungen, die bis zu diesem Punkt in einem beliebigen Treffer-Shader an der Ray-Nutzlast vorgenommen werden, werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b1d0e-107">Any modifications made to the ray payload up to this point in the any hit shader are preserved.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d0e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1d0e-108">Syntax</span></span>

```
void IgnoreHit();

```


## <a name="return-value"></a><span data-ttu-id="b1d0e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1d0e-109">Return Value</span></span>

<span data-ttu-id="b1d0e-110">**void**</span><span class="sxs-lookup"><span data-stu-id="b1d0e-110">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="b1d0e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1d0e-111">Remarks</span></span>

<span data-ttu-id="b1d0e-112">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="b1d0e-112">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="b1d0e-113">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="b1d0e-113">**Any Hit Shader**</span></span>](any-hit-shader.md)




## <a name="see-also"></a><span data-ttu-id="b1d0e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1d0e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d0e-115">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="b1d0e-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




