---
description: Legt die Direct3D-Device Manager für die DirectX-Video-accereration (DXVA) fest oder löscht sie.
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343808"
---
# <a name="mft_message_set_d3d_manager"></a><span data-ttu-id="eaefa-103">MFT- \_ Nachrichten \_ Satz \_ D3D \_ Manager</span><span class="sxs-lookup"><span data-stu-id="eaefa-103">MFT\_MESSAGE\_SET\_D3D\_MANAGER</span></span>

<span data-ttu-id="eaefa-104">Legt die Direct3D- [Device Manager](direct3d-device-manager.md) für die DirectX-Video-accereration (DXVA) fest oder löscht sie.</span><span class="sxs-lookup"><span data-stu-id="eaefa-104">Sets or clears the [Direct3D Device Manager](direct3d-device-manager.md) for DirectX Video Accereration (DXVA).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="eaefa-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="eaefa-105">Message Parameter</span></span>

<span data-ttu-id="eaefa-106">Wenn das Streaming beginnt, enthält der *ulparam* -Parameter einen **IUnknown** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="eaefa-106">When streaming begins, the *ulParam* parameter contains an **IUnknown** pointer.</span></span> <span data-ttu-id="eaefa-107">Der MFT fragt diesen Zeiger nach der [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle für Direct3D 9 und der [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle für Direct3D 11 ab.</span><span class="sxs-lookup"><span data-stu-id="eaefa-107">The MFT will query this pointer for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface for Direct3D 9 and the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface for Direct3D 11.</span></span> <span data-ttu-id="eaefa-108">Wenn das Streaming beendet wird, enthält der *ULParameter* den Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="eaefa-108">When streaming stops, the *ulParameter* contains the value **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaefa-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaefa-109">Remarks</span></span>

<span data-ttu-id="eaefa-110">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="eaefa-110">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="eaefa-111">Diese Meldung gilt nur für Video Transformationen.</span><span class="sxs-lookup"><span data-stu-id="eaefa-111">This message applies only to video transforms.</span></span> <span data-ttu-id="eaefa-112">Der Client sollte diese Nachricht nicht senden, es sei denn, der MFT gibt **true** für das [**MF \_ sa \_ D3D \_ Aware**](mf-sa-d3d-aware-attribute.md) -Attribut zurück ([MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) für Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="eaefa-112">The client should not send this message unless the MFT returns **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute ([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span>

<span data-ttu-id="eaefa-113">Senden Sie diese Nachricht nicht mit mehreren ouputs an einen MFT.</span><span class="sxs-lookup"><span data-stu-id="eaefa-113">Do not send this message to an MFT with multiple ouputs.</span></span>

### <a name="implementation"></a><span data-ttu-id="eaefa-114">Implementierung</span><span class="sxs-lookup"><span data-stu-id="eaefa-114">Implementation</span></span>

<span data-ttu-id="eaefa-115">Eine MFT sollte diese Nachricht nur unterstützen, wenn die MFT eine DirectX-Videobeschleunigung für die Videoverarbeitung oder Decodierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="eaefa-115">An MFT should support this message only if the MFT uses DirectX Video Acceleration for video processing or decoding.</span></span>

<span data-ttu-id="eaefa-116">Wenn eine MFT diese Nachricht unterstützt, sollte Sie auch die [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode implementieren und den Wert " **true** " für das Attribut " [**MF \_ sa \_ D3D \_ Aware**](mf-sa-d3d-aware-attribute.md) " ([MF \_ sa \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) für Direct3D 11) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eaefa-116">If an MFT supports this message, it should also implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method and return the value **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute (([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span> <span data-ttu-id="eaefa-117">Dieses Attribut informiert den Client darüber, dass der Client die **MFT \_ Message \_ Set \_ D3D \_ Manager** -Nachricht an die MFT senden soll, bevor das Streaming beginnt.</span><span class="sxs-lookup"><span data-stu-id="eaefa-117">This attribute informs the client that the client should send the **MFT\_MESSAGE\_SET\_D3D\_MANAGER** message to the MFT before streaming begins.</span></span>

<span data-ttu-id="eaefa-118">Wenn eine MFT diese Nachricht nicht unterstützt, sollte Sie **E \_ notimpl** von [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eaefa-118">If an MFT does not support this message, it should return **E\_NOTIMPL** from [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span> <span data-ttu-id="eaefa-119">Dies ist eine Ausnahme von der allgemeinen Regel, dass eine MFT von jeder ignoriernachricht aus **\_ OK** zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="eaefa-119">This is an exception to the general rule that an MFT can return **S\_OK** from any message it ignores.</span></span>

<span data-ttu-id="eaefa-120">Weitere Informationen finden Sie unter [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="eaefa-120">For more information, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaefa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaefa-121">Requirements</span></span>



| <span data-ttu-id="eaefa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaefa-122">Requirement</span></span> | <span data-ttu-id="eaefa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="eaefa-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaefa-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaefa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eaefa-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaefa-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eaefa-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaefa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eaefa-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaefa-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eaefa-128">Header</span><span class="sxs-lookup"><span data-stu-id="eaefa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaefa-129"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="eaefa-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaefa-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaefa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaefa-131">Direct3D-kompatible MFTs</span><span class="sxs-lookup"><span data-stu-id="eaefa-131">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="eaefa-132">Unterstützung von DXVA 2,0 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eaefa-132">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="eaefa-133">Unterstützung von Direct3D 11 Video Decodierung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eaefa-133">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="eaefa-134">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="eaefa-134">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




