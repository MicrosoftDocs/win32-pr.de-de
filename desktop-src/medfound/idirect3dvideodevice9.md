---
description: Ermöglicht die hardwarebeschleunigte Decodierung von einem Direct3D 9-Gerät mithilfe von DirectX Video Acceleration (DXVA) Version 1,0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: IDirect3DVideoDevice9-Schnittstelle (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 89afef6f39b3aa196d8b1013e3d8873e329ce6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130340"
---
# <a name="idirect3dvideodevice9-interface"></a><span data-ttu-id="d49ef-103">IDirect3DVideoDevice9-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d49ef-103">IDirect3DVideoDevice9 interface</span></span>

<span data-ttu-id="d49ef-104">Ermöglicht die hardwarebeschleunigte Decodierung von einem Direct3D 9-Gerät mithilfe von DirectX Video Acceleration (DXVA) Version 1,0.</span><span class="sxs-lookup"><span data-stu-id="d49ef-104">Enables hardware-accelerated decoding from a Direct3D 9 device, using DirectX Video Acceleration (DXVA) version 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d49ef-105">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d49ef-105">When to use</span></span>

<span data-ttu-id="d49ef-106">Diese Schnittstelle ist nicht für die allgemeine Anwendungs Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="d49ef-106">This interface is not intended for general application use.</span></span> <span data-ttu-id="d49ef-107">DirectShow-Decoderfilter sollten die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -Schnittstelle verwenden, nicht **IDirect3DVideoDevice9**.</span><span class="sxs-lookup"><span data-stu-id="d49ef-107">DirectShow decoder filters should use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, not **IDirect3DVideoDevice9**.</span></span> <span data-ttu-id="d49ef-108">Die Eingabe Pins des Filters für den Video Mischungs-Renderer (VMR) und der Überlagerungs-Mixer-Filter machen **iamvideoaccelerator** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d49ef-108">The input pins of the Video Mixing Renderer (VMR) filter and the Overlay Mixer filter expose **IAMVideoAccelerator**.</span></span>

## <a name="members"></a><span data-ttu-id="d49ef-109">Member</span><span class="sxs-lookup"><span data-stu-id="d49ef-109">Members</span></span>

<span data-ttu-id="d49ef-110">Die **IDirect3DVideoDevice9** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d49ef-110">The **IDirect3DVideoDevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d49ef-111">**IDirect3DVideoDevice9** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d49ef-111">**IDirect3DVideoDevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="d49ef-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="d49ef-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d49ef-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="d49ef-113">Methods</span></span>

<span data-ttu-id="d49ef-114">Die **IDirect3DVideoDevice9** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d49ef-114">The **IDirect3DVideoDevice9** interface has these methods.</span></span>



| <span data-ttu-id="d49ef-115">Methode</span><span class="sxs-lookup"><span data-stu-id="d49ef-115">Method</span></span>                                                                                   | <span data-ttu-id="d49ef-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d49ef-116">Description</span></span>                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d49ef-117">**"Kreatedxvadevice"**</span><span class="sxs-lookup"><span data-stu-id="d49ef-117">**CreateDXVADevice**</span></span>](idirect3dvideodevice9-createdxvadevice.md)                       | <span data-ttu-id="d49ef-118">Erstellt ein DXVA-Decodergerät.</span><span class="sxs-lookup"><span data-stu-id="d49ef-118">Creates a DXVA decoder device.</span></span><br/>                                                                                         |
| [<span data-ttu-id="d49ef-119">**"Kreatesurface"**</span><span class="sxs-lookup"><span data-stu-id="d49ef-119">**CreateSurface**</span></span>](idirect3dvideodevice9-createsurface.md)                             | <span data-ttu-id="d49ef-120">Erstellt eine komprimierte Oberfläche für die DXVA-Decodierung.</span><span class="sxs-lookup"><span data-stu-id="d49ef-120">Creates a compressed surface for DXVA decoding.</span></span><br/>                                                                        |
| [<span data-ttu-id="d49ef-121">**Getdxvacompressedbufferinfo**</span><span class="sxs-lookup"><span data-stu-id="d49ef-121">**GetDXVACompressedBufferInfo**</span></span>](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | <span data-ttu-id="d49ef-122">Ruft Informationen zu den für die Hardware beschleunigten Decodierung benötigten komprimierten Puffern ab.</span><span class="sxs-lookup"><span data-stu-id="d49ef-122">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span><br/>                                |
| [<span data-ttu-id="d49ef-123">**Getdxvage IDs**</span><span class="sxs-lookup"><span data-stu-id="d49ef-123">**GetDXVAGuids**</span></span>](idirect3dvideodevice9-getdxvaguids.md)                               | <span data-ttu-id="d49ef-124">Ruft eine Liste der DXVA-Profile ab, die vom Anzeigetreiber unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d49ef-124">Gets a list of the DXVA profiles that are supported by the display driver.</span></span><br/>                                             |
| [<span data-ttu-id="d49ef-125">**Getdxvainternalinfo**</span><span class="sxs-lookup"><span data-stu-id="d49ef-125">**GetDXVAInternalInfo**</span></span>](idirect3dvideodevice9-getdxvainternalinfo.md)                 | <span data-ttu-id="d49ef-126">Fragt den von der Hardware Abstraktionsschicht (HAL) für die private Verwendung zugewiesenen Speicherplatz ab.</span><span class="sxs-lookup"><span data-stu-id="d49ef-126">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span> <br/> |
| [<span data-ttu-id="d49ef-127">**Getuncompresseddxvaformats**</span><span class="sxs-lookup"><span data-stu-id="d49ef-127">**GetUncompressedDXVAFormats**</span></span>](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | <span data-ttu-id="d49ef-128">Ruft eine Liste nicht komprimierter Pixel Formate ab, die mithilfe eines angegebenen DXVA-Profils gerendert werden können.</span><span class="sxs-lookup"><span data-stu-id="d49ef-128">Gets a list of uncompressed pixel formats that can be rendered using a specified DXVA profile.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="d49ef-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d49ef-129">Remarks</span></span>

<span data-ttu-id="d49ef-130">Um einen Zeiger auf diese Schnittstelle abzurufen, nennen Sie **QueryInterface** für einen [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -oder [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="d49ef-130">To get a pointer to this interface, call **QueryInterface** on an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) or [**IDirect3DDevice9Ex**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex) pointer.</span></span>

<span data-ttu-id="d49ef-131">Diese Schnittstelle unterstützt nur DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="d49ef-131">This interface supports DXVA 1.0 only.</span></span> <span data-ttu-id="d49ef-132">DXVA 2,0 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d49ef-132">It does not support DXVA 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="d49ef-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d49ef-133">Requirements</span></span>



| <span data-ttu-id="d49ef-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d49ef-134">Requirement</span></span> | <span data-ttu-id="d49ef-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d49ef-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d49ef-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d49ef-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d49ef-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d49ef-137">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d49ef-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d49ef-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d49ef-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d49ef-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d49ef-140">Header</span><span class="sxs-lookup"><span data-stu-id="d49ef-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d49ef-141"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d49ef-141"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d49ef-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d49ef-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49ef-143">Direct3D-Video Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d49ef-143">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d49ef-144">DirectX-Video Beschleunigung 2,0</span><span class="sxs-lookup"><span data-stu-id="d49ef-144">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="d49ef-145">DXVA 1,0-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="d49ef-145">DXVA 1.0 specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
