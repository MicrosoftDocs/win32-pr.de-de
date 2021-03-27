---
title: Rwbyteaddressbuffer
description: Ein Lese-/Schreibpuffer, der in Bytes indiziert.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- Rwbyteaddressbuffer HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390345"
---
# <a name="rwbyteaddressbuffer"></a><span data-ttu-id="6fd3e-104">Rwbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="6fd3e-104">RWByteAddressBuffer</span></span>

<span data-ttu-id="6fd3e-105">Ein Lese-/Schreibpuffer, der in Bytes indiziert.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-105">A read/write buffer that indexes in bytes.</span></span>



| <span data-ttu-id="6fd3e-106">Methode</span><span class="sxs-lookup"><span data-stu-id="6fd3e-106">Method</span></span>                                                                                          | <span data-ttu-id="6fd3e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fd3e-107">Description</span></span>                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="6fd3e-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-108">**GetDimensions**</span></span>](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | <span data-ttu-id="6fd3e-109">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="6fd3e-110">**Interlockedadd**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-110">**InterlockedAdd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | <span data-ttu-id="6fd3e-111">Fügt atomisch hinzu.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-111">Adds, atomically.</span></span>                   |
| [<span data-ttu-id="6fd3e-112">**Interlockedand**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-112">**InterlockedAnd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | <span data-ttu-id="6fd3e-113">, Atomisch.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-113">ANDs, atomically.</span></span>                   |
| [<span data-ttu-id="6fd3e-114">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-114">**InterlockedCompareExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | <span data-ttu-id="6fd3e-115">Vergleicht und tauscht atomarisch aus.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-115">Compares and exchanges, atomically.</span></span> |
| [<span data-ttu-id="6fd3e-116">**Interlockedcomparestore**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-116">**InterlockedCompareStore**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | <span data-ttu-id="6fd3e-117">Vergleicht und speichert atomisch.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-117">Compares and stores, atomically.</span></span>    |
| [<span data-ttu-id="6fd3e-118">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-118">**InterlockedExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | <span data-ttu-id="6fd3e-119">Tauscht atomarisch aus.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-119">Exchanges, atomically.</span></span>              |
| [<span data-ttu-id="6fd3e-120">**Interlockedmax**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-120">**InterlockedMax**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | <span data-ttu-id="6fd3e-121">Sucht den maximalen, atomisch.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-121">Finds the max, atomically.</span></span>          |
| [<span data-ttu-id="6fd3e-122">**Interlockedmin**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-122">**InterlockedMin**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | <span data-ttu-id="6fd3e-123">Suchen Sie den Mindestwert atomarisch.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-123">Find the min, atomically.</span></span>           |
| [<span data-ttu-id="6fd3e-124">**Interlockedor**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-124">**InterlockedOr**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | <span data-ttu-id="6fd3e-125">, Atomarisch.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-125">ORs, atomically.</span></span>                    |
| [<span data-ttu-id="6fd3e-126">**Interlockedxor**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-126">**InterlockedXor**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | <span data-ttu-id="6fd3e-127">Xors, atomisch.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-127">XORs, atomically.</span></span>                   |
| [<span data-ttu-id="6fd3e-128">**Laden**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-128">**Load**</span></span>](rwbyteaddressbuffer-load.md)                                                        | <span data-ttu-id="6fd3e-129">Ruft einen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-129">Gets one value.</span></span>                     |
| [<span data-ttu-id="6fd3e-130">**Load2**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-130">**Load2**</span></span>](rwbyteaddressbuffer-load2.md)                                                      | <span data-ttu-id="6fd3e-131">Ruft zwei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-131">Gets two values.</span></span>                    |
| [<span data-ttu-id="6fd3e-132">**Load3**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-132">**Load3**</span></span>](rwbyteaddressbuffer-load3.md)                                                      | <span data-ttu-id="6fd3e-133">Ruft drei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-133">Gets three values.</span></span>                  |
| [<span data-ttu-id="6fd3e-134">**Load4**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-134">**Load4**</span></span>](rwbyteaddressbuffer-load4.md)                                                      | <span data-ttu-id="6fd3e-135">Ruft vier Werte ab.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-135">Gets four values.</span></span>                   |
| [<span data-ttu-id="6fd3e-136">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-136">**Store**</span></span>](sm5-object-rwbyteaddressbuffer-store.md)                                           | <span data-ttu-id="6fd3e-137">Legt einen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-137">Sets one value.</span></span>                     |
| [<span data-ttu-id="6fd3e-138">**Store2**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-138">**Store2**</span></span>](sm5-object-rwbyteaddressbuffer-store2.md)                                         | <span data-ttu-id="6fd3e-139">Legt zwei Werte fest.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-139">Sets two values.</span></span>                    |
| [<span data-ttu-id="6fd3e-140">**Store3**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-140">**Store3**</span></span>](sm5-object-rwbyteaddressbuffer-store3.md)                                         | <span data-ttu-id="6fd3e-141">Legt drei Werte fest.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-141">Sets three values.</span></span>                  |
| [<span data-ttu-id="6fd3e-142">**Store4**</span><span class="sxs-lookup"><span data-stu-id="6fd3e-142">**Store4**</span></span>](sm5-object-rwbyteaddressbuffer-store4.md)                                         | <span data-ttu-id="6fd3e-143">Legt vier Werte fest.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-143">Sets four values.</span></span>                   |



 

<span data-ttu-id="6fd3e-144">Rwbyteaddressbuffer-Objekten kann die Speicher Klasse **globallycoherent** vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-144">RWByteAddressBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="6fd3e-145">Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-145">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="6fd3e-146">Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-146">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="6fd3e-147">Das an diese Ressource gebundene UAV-Format muss mit dem typlosen DXGI-Format (Format) erstellt werden \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6fd3e-147">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_R32\_TYPELESS format.</span></span>

<span data-ttu-id="6fd3e-148">Die an diese Ressource gebundene UAV muss mit dem [**D3D11-Puffer- \_ \_ UAV- \_ Flag \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-148">The UAV bound to this resource must have been created with the [**D3D11\_BUFFER\_UAV\_FLAG\_RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="6fd3e-149">Sie können den **rwbyteaddressbuffer** -Objekttyp verwenden, wenn Sie mit Rohdaten Puffer arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-149">You can use the **RWByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="6fd3e-150">Weitere Informationen zur unformatierten Anzeige von Puffern finden Sie unter unformatierte [Ansichten von Puffern](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="6fd3e-150">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6fd3e-151">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="6fd3e-151">Minimum Shader Model</span></span>

<span data-ttu-id="6fd3e-152">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-152">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="6fd3e-153">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="6fd3e-153">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="6fd3e-154">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="6fd3e-154">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6fd3e-155">Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle [Shader Model 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mithilfe der 10,0-oder 10,1-Featureebene ([**D3D \_ Feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) auf Geräten, die Compute-Shader unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6fd3e-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="6fd3e-156">Weitere Informationen zur Unterstützung von Compute-Shadern auf downlevelhardware finden Sie unter Compute-Shader [auf downlevelhardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="6fd3e-156">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="6fd3e-157">ja</span><span class="sxs-lookup"><span data-stu-id="6fd3e-157">yes</span></span>       |



 

<span data-ttu-id="6fd3e-158">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6fd3e-158">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6fd3e-159">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="6fd3e-159">Vertex</span></span> | <span data-ttu-id="6fd3e-160">Hülle</span><span class="sxs-lookup"><span data-stu-id="6fd3e-160">Hull</span></span> | <span data-ttu-id="6fd3e-161">Domain</span><span class="sxs-lookup"><span data-stu-id="6fd3e-161">Domain</span></span> | <span data-ttu-id="6fd3e-162">Geometrie</span><span class="sxs-lookup"><span data-stu-id="6fd3e-162">Geometry</span></span> | <span data-ttu-id="6fd3e-163">Pixel</span><span class="sxs-lookup"><span data-stu-id="6fd3e-163">Pixel</span></span> | <span data-ttu-id="6fd3e-164">Compute</span><span class="sxs-lookup"><span data-stu-id="6fd3e-164">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6fd3e-165">x</span><span class="sxs-lookup"><span data-stu-id="6fd3e-165">x</span></span>     | <span data-ttu-id="6fd3e-166">x</span><span class="sxs-lookup"><span data-stu-id="6fd3e-166">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6fd3e-167">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6fd3e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd3e-168">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="6fd3e-168">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

