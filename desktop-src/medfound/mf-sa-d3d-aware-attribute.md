---
description: Gibt an, ob eine Media Foundation Transformation (MFT) die DirectX-Video Beschleunigung (DXVA) unterstützt. Dieses Attribut gilt nur für Video-MFTs.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: MF_SA_D3D_AWARE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368861"
---
# <a name="mf_sa_d3d_aware-attribute"></a><span data-ttu-id="14e44-104">MF \_ sa \_ D3D \_ Aware-Attribut</span><span class="sxs-lookup"><span data-stu-id="14e44-104">MF\_SA\_D3D\_AWARE attribute</span></span>

<span data-ttu-id="14e44-105">Gibt an, ob eine Media Foundation Transformation (MFT) die DirectX-Video Beschleunigung (DXVA) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14e44-105">Specifies whether a Media Foundation transform (MFT) supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="14e44-106">Dieses Attribut gilt nur für Video-MFTs.</span><span class="sxs-lookup"><span data-stu-id="14e44-106">This attribute applies only to video MFTs.</span></span>

## <a name="data-type"></a><span data-ttu-id="14e44-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="14e44-107">Data type</span></span>

<span data-ttu-id="14e44-108">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14e44-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="14e44-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14e44-109">Remarks</span></span>

<span data-ttu-id="14e44-110">Um dieses Attribut abzufragen, müssen Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den globalen Attribut Speicher des MFT abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14e44-110">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="14e44-111">Wenn **GetAttributes** erfolgreich ist, können Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14e44-111">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="14e44-112">Dieses Attribut teilt dem Client mit, ob der MFT Direct3D 9-Video verwenden kann:</span><span class="sxs-lookup"><span data-stu-id="14e44-112">This attribute tells the client whether the MFT can use Direct3D 9 video:</span></span>

-   <span data-ttu-id="14e44-113">Wenn das Attribut ungleich NULL ist, kann der Client dem MFT einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle übergeben, bevor das Streaming gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="14e44-113">If the attribute is nonzero, the client can give the MFT a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface before streaming starts.</span></span> <span data-ttu-id="14e44-114">Hierzu sendet der Client die [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht an die MFT.</span><span class="sxs-lookup"><span data-stu-id="14e44-114">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="14e44-115">Der Client muss diese Nachricht nicht senden.</span><span class="sxs-lookup"><span data-stu-id="14e44-115">The client is not required to send this message.</span></span>
-   <span data-ttu-id="14e44-116">Wenn dieses Attribut NULL (**false**) ist, wird das Direct3D 9-Video vom MFT nicht unterstützt, und der Client sollte die [**MFT- \_ Nachricht \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) nicht an die MFT senden.</span><span class="sxs-lookup"><span data-stu-id="14e44-116">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 9 video, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="14e44-117">Der Standardwert dieses Attributs ist **false**.</span><span class="sxs-lookup"><span data-stu-id="14e44-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="14e44-118">Behandeln Sie dieses Attribut als schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="14e44-118">Treat this attribute as read-only.</span></span> <span data-ttu-id="14e44-119">Ändern Sie den Wert nicht. die MFT ignoriert alle Änderungen am Wert.</span><span class="sxs-lookup"><span data-stu-id="14e44-119">Do not change the value; the MFT will ignore any changes to the value.</span></span>

<span data-ttu-id="14e44-120">Weitere Informationen zum Implementieren dieses Attributs in einem benutzerdefinierten MFT finden Sie unter [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="14e44-120">For more information about implementing this attribute in a custom MFT, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

<span data-ttu-id="14e44-121">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="14e44-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="14e44-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14e44-122">Examples</span></span>

<span data-ttu-id="14e44-123">Der folgende Code testet, ob eine MFT DXVA unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14e44-123">The following code tests whether an MFT supports DXVA.</span></span>


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a><span data-ttu-id="14e44-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14e44-124">Requirements</span></span>



| <span data-ttu-id="14e44-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14e44-125">Requirement</span></span> | <span data-ttu-id="14e44-126">Wert</span><span class="sxs-lookup"><span data-stu-id="14e44-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14e44-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14e44-127">Minimum supported client</span></span><br/> | <span data-ttu-id="14e44-128">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="14e44-128">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="14e44-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14e44-129">Minimum supported server</span></span><br/> | <span data-ttu-id="14e44-130">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="14e44-130">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="14e44-131">Header</span><span class="sxs-lookup"><span data-stu-id="14e44-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="14e44-132"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="14e44-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e44-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14e44-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e44-134">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="14e44-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="14e44-135">Direct3D-kompatible MFTs</span><span class="sxs-lookup"><span data-stu-id="14e44-135">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="14e44-136">Unterstützung von DXVA 2,0 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14e44-136">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="14e44-137">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="14e44-137">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="14e44-138">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="14e44-138">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="14e44-139">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="14e44-139">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="14e44-140">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="14e44-140">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="14e44-141">\_ \_ DXVA-Modus für MF-Topologie \_</span><span class="sxs-lookup"><span data-stu-id="14e44-141">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




