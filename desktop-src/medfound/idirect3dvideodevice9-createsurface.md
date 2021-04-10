---
description: Erstellt eine komprimierte Oberfläche für die DirectX-Video Beschleunigung (DXVA)-Decodierung.
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9:: kreatesurface-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131328"
---
# <a name="idirect3dvideodevice9createsurface-method"></a><span data-ttu-id="19ddc-103">IDirect3DVideoDevice9:: kreatesurface-Methode</span><span class="sxs-lookup"><span data-stu-id="19ddc-103">IDirect3DVideoDevice9::CreateSurface method</span></span>

<span data-ttu-id="19ddc-104">Erstellt eine komprimierte Oberfläche für die DirectX-Video Beschleunigung (DXVA)-Decodierung.</span><span class="sxs-lookup"><span data-stu-id="19ddc-104">Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.</span></span>

<span data-ttu-id="19ddc-105">Um die Oberflächen Anforderungen zu ermitteln, müssen Sie [**IDirect3DVideoDevice9:: getdxvacompressedbufferinfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) aufrufen und die zurückgegebenen [**dxvacompbufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) -Strukturen untersuchen.</span><span class="sxs-lookup"><span data-stu-id="19ddc-105">To get the surface requirements, call [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) and examine the returned [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ddc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ddc-106">Syntax</span></span>


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a><span data-ttu-id="19ddc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ddc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ddc-108">*Width*</span><span class="sxs-lookup"><span data-stu-id="19ddc-108">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-109">Die Breite der Oberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="19ddc-109">The width of the surface, in pixels.</span></span> <span data-ttu-id="19ddc-110">Legen Sie diesen Parameter auf **dxvacompbufferinfo. widthtocreate** fest.</span><span class="sxs-lookup"><span data-stu-id="19ddc-110">Set this parameter equal to **DXVACompBufferInfo.WidthToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="19ddc-111">*Height*</span><span class="sxs-lookup"><span data-stu-id="19ddc-111">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-112">Die Höhe der Oberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="19ddc-112">The height of the surface, in pixels.</span></span> <span data-ttu-id="19ddc-113">Legen Sie diesen Parameter auf **dxvacompbufferinfo. heighttocreate** fest.</span><span class="sxs-lookup"><span data-stu-id="19ddc-113">Set this parameter equal to **DXVACompBufferInfo.HeightToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="19ddc-114">*BackBuffer*</span><span class="sxs-lookup"><span data-stu-id="19ddc-114">*BackBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-115">Die Anzahl der Back Puffer.</span><span class="sxs-lookup"><span data-stu-id="19ddc-115">The number of back buffers.</span></span> <span data-ttu-id="19ddc-116">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="19ddc-116">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="19ddc-117">*Format*</span><span class="sxs-lookup"><span data-stu-id="19ddc-117">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-118">Das als **D3DFORMAT** -Wert angegebene Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="19ddc-118">The pixel format, specified as a **D3DFORMAT** value.</span></span> <span data-ttu-id="19ddc-119">Legen Sie diesen Parameter auf **dxvacompbufferinfo. Format** fest.</span><span class="sxs-lookup"><span data-stu-id="19ddc-119">Set this parameter equal to **DXVACompBufferInfo.Format**.</span></span>

</dd> <dt>

<span data-ttu-id="19ddc-120">*Pool*</span><span class="sxs-lookup"><span data-stu-id="19ddc-120">*Pool*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-121">Der Speicherpool, in dem die-Oberfläche erstellt werden soll, angegeben als **D3DPOOL** -Wert.</span><span class="sxs-lookup"><span data-stu-id="19ddc-121">The memory pool in which to create the surface, specified as a **D3DPOOL** value.</span></span> <span data-ttu-id="19ddc-122">Legen Sie diesen Parameter auf **dxvacompbufferinfo. Pool** fest.</span><span class="sxs-lookup"><span data-stu-id="19ddc-122">Set this parameter equal to **DXVACompBufferInfo.Pool**.</span></span>

</dd> <dt>

<span data-ttu-id="19ddc-123">*Verwendung*</span><span class="sxs-lookup"><span data-stu-id="19ddc-123">*Usage*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-124">Ein bitweises **or** von mindestens einer **D3DUSAGE** -Konstante.</span><span class="sxs-lookup"><span data-stu-id="19ddc-124">A bitwise **OR** of one or more **D3DUSAGE** constants.</span></span> <span data-ttu-id="19ddc-125">Legen Sie diesen Parameter auf **dxvacompbufferinfo. Usage fest.**</span><span class="sxs-lookup"><span data-stu-id="19ddc-125">Set this parameter equal to **DXVACompBufferInfo.Usage**.</span></span>

</dd> <dt>

<span data-ttu-id="19ddc-126">*ppsurface*</span><span class="sxs-lookup"><span data-stu-id="19ddc-126">*ppSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-127">Empfängt einen Zeiger auf die **IDirect3DSurface9** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="19ddc-127">Receives a pointer to the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="19ddc-128">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="19ddc-128">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="19ddc-129">*psharedhandle*</span><span class="sxs-lookup"><span data-stu-id="19ddc-129">*pSharedHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="19ddc-130">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="19ddc-130">Reserved.</span></span> <span data-ttu-id="19ddc-131">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19ddc-131">Set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ddc-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19ddc-132">Return value</span></span>

<span data-ttu-id="19ddc-133">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="19ddc-133">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19ddc-134">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19ddc-134">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ddc-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19ddc-135">Requirements</span></span>



| <span data-ttu-id="19ddc-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19ddc-136">Requirement</span></span> | <span data-ttu-id="19ddc-137">Wert</span><span class="sxs-lookup"><span data-stu-id="19ddc-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="19ddc-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19ddc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="19ddc-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19ddc-139">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19ddc-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19ddc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="19ddc-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19ddc-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="19ddc-142">Header</span><span class="sxs-lookup"><span data-stu-id="19ddc-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ddc-143"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ddc-143"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ddc-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19ddc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ddc-145">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="19ddc-145">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




