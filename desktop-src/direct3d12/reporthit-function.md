---
description: Wird von einem Schnittmengen-Shader aufgerufen, um eine Strahl Überschneidung zu melden.
ms.assetid: ''
title: ReportHit-Funktion
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343195"
---
# <a name="reporthit-function"></a><span data-ttu-id="451ae-103">ReportHit-Funktion</span><span class="sxs-lookup"><span data-stu-id="451ae-103">ReportHit function</span></span>

<span data-ttu-id="451ae-104">Wird von einem [Schnittmengen-Shader](intersection-shader.md) aufgerufen, um eine Strahl Überschneidung zu melden.</span><span class="sxs-lookup"><span data-stu-id="451ae-104">Called by an [intersection shader](intersection-shader.md) to report a ray intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="451ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="451ae-105">Syntax</span></span>
<span data-ttu-id="451ae-106">Diese intrinsische Funktionsdefinition entspricht der folgenden Funktions Vorlage:</span><span class="sxs-lookup"><span data-stu-id="451ae-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a><span data-ttu-id="451ae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="451ae-107">Parameters</span></span>

`THit`

<span data-ttu-id="451ae-108">Ein float-Wert, der den parametrischen Abstand der Schnittmenge angibt.</span><span class="sxs-lookup"><span data-stu-id="451ae-108">A float value specifying the parametric distance of the intersection..</span></span>

`HitKind`

<span data-ttu-id="451ae-109">Eine Ganzzahl ohne Vorzeichen, die den Typ des aufgetretenen Treffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="451ae-109">An unsigned integer that identifies the type of hit that occurred.</span></span>  <span data-ttu-id="451ae-110">Dies ist ein vom Benutzer angegebener Wert im Bereich von 0-127.</span><span class="sxs-lookup"><span data-stu-id="451ae-110">This is a user-specified value in the range of 0-127.</span></span>  <span data-ttu-id="451ae-111">Der Wert kann von [jeder Treffer](any-hit-shader.md) -oder [nächster Treffer](closest-hit-shader.md) -Shader mit der systeminternen Funktion " **hitkind** " gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="451ae-111">The value can be read by [any hit](any-hit-shader.md) or [closest hit](closest-hit-shader.md) shaders with the **HitKind** intrinsic.</span></span>

`Attributes`

<span data-ttu-id="451ae-112">Die benutzerdefinierte Schnittmengen- [**Attribut Struktur**](intersection-attributes.md) Struktur, die die Schnittmengen Attribute angibt.</span><span class="sxs-lookup"><span data-stu-id="451ae-112">The user-defined [**Intersection Attribute Structure**](intersection-attributes.md) structure specifying the intersection attributes.</span></span>  

## <a name="return-value"></a><span data-ttu-id="451ae-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="451ae-113">Return Value</span></span>

<span data-ttu-id="451ae-114">**bool** True, wenn der Treffer akzeptiert wurde.</span><span class="sxs-lookup"><span data-stu-id="451ae-114">**bool** True if the hit was accepted.</span></span>  <span data-ttu-id="451ae-115">Ein Treffer wird zurückgewiesen *, wenn der* Wert außerhalb des aktuellen Ray-Intervalls liegt oder der any Hit-Shader [**ignorehit**](ignorehit-function.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="451ae-115">A hit is rejected if *THit* is outside the current ray interval, or the any hit shader calls [**IgnoreHit**](ignorehit-function.md).</span></span>  <span data-ttu-id="451ae-116">Das aktuelle Ray-Intervall wird durch **raytmin** und **raytcurrent** definiert.</span><span class="sxs-lookup"><span data-stu-id="451ae-116">The current ray interval is defined by **RayTMin** and **RayTCurrent**.</span></span>

## <a name="remarks"></a><span data-ttu-id="451ae-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="451ae-117">Remarks</span></span>

<span data-ttu-id="451ae-118">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="451ae-118">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="451ae-119">**Intersection-Shader**</span><span class="sxs-lookup"><span data-stu-id="451ae-119">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="451ae-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="451ae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451ae-121">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="451ae-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




