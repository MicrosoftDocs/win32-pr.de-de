---
title: Byteaddressbuffer
description: Byteaddressbuffer
ms.assetid: 809b5ee8-0a25-402e-8cf2-f5e7a8094ec6
keywords:
- Byteaddressbuffer HLSL
topic_type:
- apiref
api_name:
- ByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03e89f56522d941db4447b33b55cbedc7c73303f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976825"
---
# <a name="byteaddressbuffer"></a><span data-ttu-id="ac65e-104">Byteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="ac65e-104">ByteAddressBuffer</span></span>

<span data-ttu-id="ac65e-105">Ein Schreib geschützter Puffer, der in Bytes indiziert ist.</span><span class="sxs-lookup"><span data-stu-id="ac65e-105">A read-only buffer that is indexed in bytes.</span></span>



| <span data-ttu-id="ac65e-106">Methode</span><span class="sxs-lookup"><span data-stu-id="ac65e-106">Method</span></span>                                                              | <span data-ttu-id="ac65e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac65e-107">Description</span></span>                   |
|---------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="ac65e-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="ac65e-108">**GetDimensions**</span></span>](sm5-object-byteaddressbuffer-getdimensions.md) | <span data-ttu-id="ac65e-109">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="ac65e-109">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="ac65e-110">**Laden**</span><span class="sxs-lookup"><span data-stu-id="ac65e-110">**Load**</span></span>](byteaddressbuffer-load.md)                              | <span data-ttu-id="ac65e-111">Ruft einen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="ac65e-111">Gets one value.</span></span>               |
| [<span data-ttu-id="ac65e-112">**Load2**</span><span class="sxs-lookup"><span data-stu-id="ac65e-112">**Load2**</span></span>](byteaddressbuffer-load2.md)                            | <span data-ttu-id="ac65e-113">Ruft zwei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="ac65e-113">Gets two values.</span></span>              |
| [<span data-ttu-id="ac65e-114">**Load3**</span><span class="sxs-lookup"><span data-stu-id="ac65e-114">**Load3**</span></span>](byteaddressbuffer-load3.md)                            | <span data-ttu-id="ac65e-115">Ruft drei Werte ab.</span><span class="sxs-lookup"><span data-stu-id="ac65e-115">Gets three values.</span></span>            |
| [<span data-ttu-id="ac65e-116">**Load4**</span><span class="sxs-lookup"><span data-stu-id="ac65e-116">**Load4**</span></span>](byteaddressbuffer-load4.md)                            | <span data-ttu-id="ac65e-117">Ruft vier Werte ab.</span><span class="sxs-lookup"><span data-stu-id="ac65e-117">Gets four values.</span></span>             |



 

<span data-ttu-id="ac65e-118">Sie können den **byteaddressbuffer** -Objekttyp verwenden, wenn Sie mit Rohdaten Puffer arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac65e-118">You can use the **ByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="ac65e-119">Weitere Informationen zur unformatierten Anzeige von Puffern finden Sie unter unformatierte [Ansichten von Puffern](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="ac65e-119">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ac65e-120">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="ac65e-120">Minimum Shader Model</span></span>

<span data-ttu-id="ac65e-121">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac65e-121">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="ac65e-122">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="ac65e-122">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="ac65e-123">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ac65e-123">Supported</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ac65e-124">Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle [Shader Model 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mithilfe der 10,0-oder 10,1-Featureebene ([**D3D \_ Feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) auf Geräten, die Compute-Shader unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ac65e-124">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="ac65e-125">Weitere Informationen zur Unterstützung von Compute-Shadern bei downlevelhardware finden Sie unter Compute-Shader [auf downlevelhardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="ac65e-125">For more info about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="ac65e-126">ja</span><span class="sxs-lookup"><span data-stu-id="ac65e-126">yes</span></span>       |



 

<span data-ttu-id="ac65e-127">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ac65e-127">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ac65e-128">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="ac65e-128">Vertex</span></span> | <span data-ttu-id="ac65e-129">Hülle</span><span class="sxs-lookup"><span data-stu-id="ac65e-129">Hull</span></span> | <span data-ttu-id="ac65e-130">Domain</span><span class="sxs-lookup"><span data-stu-id="ac65e-130">Domain</span></span> | <span data-ttu-id="ac65e-131">Geometrie</span><span class="sxs-lookup"><span data-stu-id="ac65e-131">Geometry</span></span> | <span data-ttu-id="ac65e-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="ac65e-132">Pixel</span></span> | <span data-ttu-id="ac65e-133">Compute</span><span class="sxs-lookup"><span data-stu-id="ac65e-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac65e-134">x</span><span class="sxs-lookup"><span data-stu-id="ac65e-134">x</span></span>      | <span data-ttu-id="ac65e-135">x</span><span class="sxs-lookup"><span data-stu-id="ac65e-135">x</span></span>    | <span data-ttu-id="ac65e-136">x</span><span class="sxs-lookup"><span data-stu-id="ac65e-136">x</span></span>      | <span data-ttu-id="ac65e-137">x</span><span class="sxs-lookup"><span data-stu-id="ac65e-137">x</span></span>        | <span data-ttu-id="ac65e-138">x</span><span class="sxs-lookup"><span data-stu-id="ac65e-138">x</span></span>     | <span data-ttu-id="ac65e-139">x</span><span class="sxs-lookup"><span data-stu-id="ac65e-139">x</span></span>       |



 

<span data-ttu-id="ac65e-140">Weitere Informationen zu einem Byte Adress Puffer finden Sie unter der [Byte adressierbare Ressourcentyp](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span><span class="sxs-lookup"><span data-stu-id="ac65e-140">For more info about a byte address buffer, see the [byte addressable resource type](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).</span></span>

<span data-ttu-id="ac65e-141">Shader Model 5 implementiert auch einen [Lese-/Schreib-Byte-Adress Puffer](sm5-object-rwbyteaddressbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ac65e-141">Shader Model 5 also implements a [read-write byte address buffer](sm5-object-rwbyteaddressbuffer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ac65e-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ac65e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac65e-143">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="ac65e-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

