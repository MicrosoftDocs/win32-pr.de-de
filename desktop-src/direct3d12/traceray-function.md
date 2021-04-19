---
description: Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungs Struktur.
ms.assetid: ''
title: TraceRay-Funktion
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106355728"
---
# <a name="traceray-function"></a><span data-ttu-id="02858-103">TraceRay-Funktion</span><span class="sxs-lookup"><span data-stu-id="02858-103">TraceRay function</span></span>

<span data-ttu-id="02858-104">Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="02858-104">Sends a ray into a search for hits in an acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="02858-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02858-105">Syntax</span></span>
<span data-ttu-id="02858-106">Diese intrinsische Funktionsdefinition entspricht der folgenden Funktions Vorlage:</span><span class="sxs-lookup"><span data-stu-id="02858-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a><span data-ttu-id="02858-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02858-107">Parameters</span></span>

`AccelerationStructure`

<span data-ttu-id="02858-108">Die zu verwendende Beschleunigungs Struktur auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="02858-108">The top-level acceleration structure to use.</span></span> <span data-ttu-id="02858-109">Die Angabe einer NULL-Beschleunigungs Struktur erzwingt einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="02858-109">Specifying a NULL acceleration structure forces a miss.</span></span>

`RayFlags`

<span data-ttu-id="02858-110">Gültige Kombination von [ray_flag](ray_flag.md) Werten.</span><span class="sxs-lookup"><span data-stu-id="02858-110">Valid combination of [ray_flag](ray_flag.md) values.</span></span> <span data-ttu-id="02858-111">Nur definierte Ray-Flags werden vom System weitergegeben, d. h., Sie sind für den systeminternen [rayflags](rayflags.md) -Shader sichtbar.</span><span class="sxs-lookup"><span data-stu-id="02858-111">Only defined ray flags are propagated by the system, i.e. are visible to the [RayFlags](rayflags.md) shader intrinsic.</span></span>

`InstanceInclusionMask`

<span data-ttu-id="02858-112">Eine ganze Zahl ohne Vorzeichen, von der die unteren 8 Bits verwendet werden, um geometry-Instanzen auf der Grundlage von instancemask in jeder Instanz einzubeziehen oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="02858-112">An unsigned integer, the bottom 8 bits of which are used to include or reject geometry instances based on the InstanceMask in each instance.</span></span> <span data-ttu-id="02858-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="02858-113">For example:</span></span>
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

<span data-ttu-id="02858-114">Eine ganze Zahl ohne Vorzeichen, die den Offset angibt, der zur Adressierung von Berechnungen in shadertabellen für die Treffer Gruppen Indizierung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="02858-114">An unsigned integer specifying the offset to add into addressing calculations within shader tables for hit group indexing.</span></span>  <span data-ttu-id="02858-115">Nur die untersten 4 Bits dieses Werts werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="02858-115">Only the bottom 4 bits of this value are used.</span></span>

`MultiplierForGeometryContributionToHitGroupIndex`

<span data-ttu-id="02858-116">Eine Ganzzahl ohne Vorzeichen, die den Schritt angibt, der von *geometrycontributiontohitgroupindex* multipliziert werden soll. Hierbei handelt es sich nur um den 0-basierten Index, den die Geometrie von der app in der Struktur der untersten Beschleunigung bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="02858-116">An unsigned integer specifying the stride to multiply by *GeometryContributionToHitGroupIndex*, which is just the 0 based index the geometry was supplied by the app into its bottom-level acceleration structure.</span></span> <span data-ttu-id="02858-117">Es werden nur die untersten 16 Bits dieses Multiplikator-Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="02858-117">Only the bottom 16 bits of this multiplier value are used.</span></span>

`MissShaderIndex`

<span data-ttu-id="02858-118">Eine ganze Zahl ohne Vorzeichen, die den Index des fehlshaders innerhalb einer shadertabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="02858-118">An unsigned integer specifying the index of the miss shader within a shader table.</span></span>

`Ray`

<span data-ttu-id="02858-119">Ein [**raydebug**](raydesc.md) -Objekt, das den zu über mittelenden Strahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="02858-119">A [**RayDesc**](raydesc.md) representing the ray to be traced.</span></span>

`Payload`

<span data-ttu-id="02858-120">Eine benutzerdefinierte Strahl Nutzlast, auf die sowohl für die Eingabe als auch für die Ausgabe durch Shader zugegriffen wird, die während der Raytracing</span><span class="sxs-lookup"><span data-stu-id="02858-120">A user defined ray payload accessed both for both input and output by shaders invoked during raytracing.</span></span>  <span data-ttu-id="02858-121">Nachdem [**traceray**](traceray-function.md) abgeschlossen ist, kann der Aufrufer auch auf die Nutzlast zugreifen.</span><span class="sxs-lookup"><span data-stu-id="02858-121">After [**TraceRay**](traceray-function.md) completes, the caller can access the payload as well.</span></span>

## <a name="return-value"></a><span data-ttu-id="02858-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02858-122">Return Value</span></span>

<span data-ttu-id="02858-123">**void**</span><span class="sxs-lookup"><span data-stu-id="02858-123">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="02858-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02858-124">Remarks</span></span>

<span data-ttu-id="02858-125">Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="02858-125">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="02858-126">**Closest Hit-Shader**</span><span class="sxs-lookup"><span data-stu-id="02858-126">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="02858-127">**Miss-Shader**</span><span class="sxs-lookup"><span data-stu-id="02858-127">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="02858-128">**Ray Generation-Shader**</span><span class="sxs-lookup"><span data-stu-id="02858-128">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="02858-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02858-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02858-130">Direct3D 12-Raytracing, HLSL-Referenz</span><span class="sxs-lookup"><span data-stu-id="02858-130">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




