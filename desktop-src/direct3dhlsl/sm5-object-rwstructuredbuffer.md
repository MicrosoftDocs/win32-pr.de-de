---
title: Rwstructuredbuffer
description: Ein Lese-/Schreibpuffer, der einen T-Typ, der eine Struktur ist, annehmen kann.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- Rwstructuredbuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390497"
---
# <a name="rwstructuredbuffer"></a><span data-ttu-id="c47cb-104">Rwstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="c47cb-104">RWStructuredBuffer</span></span>

<span data-ttu-id="c47cb-105">Ein Lese-/Schreibpuffer, der einen T-Typ, der eine Struktur ist, annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="c47cb-105">A read/write buffer that can take a T type that is a structure.</span></span>



| <span data-ttu-id="c47cb-106">Methode</span><span class="sxs-lookup"><span data-stu-id="c47cb-106">Method</span></span>                                                                     | <span data-ttu-id="c47cb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c47cb-107">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="c47cb-108">**Dekrementcounter**</span><span class="sxs-lookup"><span data-stu-id="c47cb-108">**DecrementCounter**</span></span>](sm5-object-rwstructuredbuffer-decrementcounter.md) | <span data-ttu-id="c47cb-109">Dekremente den ausgeblendeten Wert des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c47cb-109">Decrements the object's hidden counter.</span></span> |
| [<span data-ttu-id="c47cb-110">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="c47cb-110">**GetDimensions**</span></span>](sm5-object-rwstructuredbuffer-getdimensions.md)       | <span data-ttu-id="c47cb-111">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="c47cb-111">Gets the resource dimensions.</span></span>           |
| [<span data-ttu-id="c47cb-112">**Incrementcounter**</span><span class="sxs-lookup"><span data-stu-id="c47cb-112">**IncrementCounter**</span></span>](sm5-object-rwstructuredbuffer-incrementcounter.md) | <span data-ttu-id="c47cb-113">Erhöht den ausgeblendeten Wert des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c47cb-113">Increments the object's hidden counter.</span></span> |
| [<span data-ttu-id="c47cb-114">**Laden**</span><span class="sxs-lookup"><span data-stu-id="c47cb-114">**Load**</span></span>](rwstructuredbuffer-load.md)                                    | <span data-ttu-id="c47cb-115">Liest Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="c47cb-115">Reads buffer data.</span></span>                      |
| <span data-ttu-id="c47cb-116">[**KOM\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="c47cb-116">[**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)</span></span>        | <span data-ttu-id="c47cb-117">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="c47cb-117">Returns a resource variable.</span></span>            |



 

<span data-ttu-id="c47cb-118">Eine Ressourcen Variable kann auch an einen ungeordneten oder Interlocked-Vorgang übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c47cb-118">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="c47cb-119">Rwstructuredbuffer-Objekten kann die Speicher Klasse **globallycoherent** vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c47cb-119">RWStructuredBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="c47cb-120">Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können.</span><span class="sxs-lookup"><span data-stu-id="c47cb-120">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="c47cb-121">Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung nur eine UAV innerhalb der aktuellen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c47cb-121">Without this specifier, a memory barrier or sync will only flush a UAV within the current group.</span></span>

<span data-ttu-id="c47cb-122">Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="c47cb-122">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_UNKNOWN format.</span></span>

<span data-ttu-id="c47cb-123">Weitere Informationen über [strukturierte Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)finden Sie im Übersichts Material.</span><span class="sxs-lookup"><span data-stu-id="c47cb-123">To find out more about [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), see the overview material.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c47cb-124">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c47cb-124">Minimum Shader Model</span></span>

<span data-ttu-id="c47cb-125">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c47cb-125">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="c47cb-126">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c47cb-126">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="c47cb-127">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c47cb-127">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c47cb-128">Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle [Shader Model 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mithilfe der 10,0-oder 10,1-Featureebene ([**D3D \_ Feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) auf Geräten, die Compute-Shader unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c47cb-128">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="c47cb-129">Weitere Informationen zur Unterstützung von Compute-Shadern auf downlevelhardware finden Sie unter Compute-Shader [auf downlevelhardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="c47cb-129">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="c47cb-130">ja</span><span class="sxs-lookup"><span data-stu-id="c47cb-130">yes</span></span>       |



 

<span data-ttu-id="c47cb-131">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c47cb-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c47cb-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c47cb-132">Vertex</span></span> | <span data-ttu-id="c47cb-133">Hülle</span><span class="sxs-lookup"><span data-stu-id="c47cb-133">Hull</span></span> | <span data-ttu-id="c47cb-134">Domain</span><span class="sxs-lookup"><span data-stu-id="c47cb-134">Domain</span></span> | <span data-ttu-id="c47cb-135">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c47cb-135">Geometry</span></span> | <span data-ttu-id="c47cb-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="c47cb-136">Pixel</span></span> | <span data-ttu-id="c47cb-137">Compute</span><span class="sxs-lookup"><span data-stu-id="c47cb-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c47cb-138">x</span><span class="sxs-lookup"><span data-stu-id="c47cb-138">x</span></span>     | <span data-ttu-id="c47cb-139">x</span><span class="sxs-lookup"><span data-stu-id="c47cb-139">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c47cb-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c47cb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47cb-141">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="c47cb-141">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

