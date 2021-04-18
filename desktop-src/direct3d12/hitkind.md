---
description: Gibt den Wert zurück, der als hitkind-Parameter an Report Thread übergeben wird.
ms.assetid: ''
title: Hitkind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345449"
---
# <a name="hitkind"></a><span data-ttu-id="032e9-103">Hitkind</span><span class="sxs-lookup"><span data-stu-id="032e9-103">HitKind</span></span>

<span data-ttu-id="032e9-104">Gibt den Wert zurück, der als **hitkind** -Parameter an Report [**Thread**](reporthit-function.md)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="032e9-104">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="032e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="032e9-105">Syntax</span></span>

```
uint HitKind();

```



## <a name="remarks"></a><span data-ttu-id="032e9-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="032e9-106">Remarks</span></span>

<span data-ttu-id="032e9-107">Wenn die Schnittmenge von Dreiecks Schnittstellen mit fester Funktionsweise berichtet wurde, ist **hitkind** eines der **Treffer \_ Kind-Dreieck- \_ \_ Vorder \_** Seite (254) oder **Treffer Kind- \_ \_ Dreiecks \_ Rückseite \_** (255).</span><span class="sxs-lookup"><span data-stu-id="032e9-107">If the intersection was reported by fixed-function triangle intersection, **HitKind** will be one of **HIT\_KIND\_TRIANGLE\_FRONT\_FACE** (254) or **HIT\_KIND\_TRIANGLE\_BACK\_FACE** (255).</span></span>

<span data-ttu-id="032e9-108">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="032e9-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="032e9-109">**Any Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="032e9-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="032e9-110">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="032e9-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="032e9-111">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="032e9-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="032e9-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="032e9-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032e9-113">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="032e9-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




