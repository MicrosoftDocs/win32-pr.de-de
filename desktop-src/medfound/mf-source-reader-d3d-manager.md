---
description: Enthält einen Zeiger auf den Microsoft Direct3D-Device Manager für den Quell Reader.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: MF_SOURCE_READER_D3D_MANAGER-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865579"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a><span data-ttu-id="884c2-103">MF- \_ Quell \_ Leser \_ D3D Manager- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="884c2-103">MF\_SOURCE\_READER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="884c2-104">Enthält einen Zeiger auf den Microsoft [Direct3D-Device Manager](direct3d-device-manager.md) für den [Quell Reader](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="884c2-104">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md) for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="884c2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="884c2-105">Data type</span></span>

<span data-ttu-id="884c2-106">**IDirect3DDeviceManager9 \* oder IMF dxgidebug Manager \*** gespeichert als \**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="884c2-106">**IDirect3DDeviceManager9\* or IMFDXGIDeviceManager\*** stored as \**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="884c2-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="884c2-107">Get/set</span></span>

<span data-ttu-id="884c2-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="884c2-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="884c2-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="884c2-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="884c2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="884c2-110">Remarks</span></span>

<span data-ttu-id="884c2-111">Der Wert dieses Attributs kann ein Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle oder ein [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)sein.</span><span class="sxs-lookup"><span data-stu-id="884c2-111">The value of this attribute can be a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface or a [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span></span>

<span data-ttu-id="884c2-112">Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Video-Decoder bereitzustellen, die vom Quell Leser geladen werden.</span><span class="sxs-lookup"><span data-stu-id="884c2-112">Use this attribute to provide a Direct3D device for any video decoders loaded by the source reader.</span></span> <span data-ttu-id="884c2-113">Wenn Sie dieses Attribut festlegen und der Decoder Microsoft DirectX Video Acceleration (DXVA) unterstützt, verwendet der Quell Leser das Direct3D-Gerät zum Zuordnen von Video Puffern.</span><span class="sxs-lookup"><span data-stu-id="884c2-113">If you set this attribute and the decoder supports Microsoft DirectX Video Acceleration (DXVA), the source reader uses the Direct3D device to allocate video buffers.</span></span> <span data-ttu-id="884c2-114">Diese Puffer sind kompatibel mit dem DXVA 2-Videoprozessor.</span><span class="sxs-lookup"><span data-stu-id="884c2-114">These buffers are compatible with the DXVA 2 video processor.</span></span> <span data-ttu-id="884c2-115">(Siehe [DXVA-Video Verarbeitung](dxva-video-processing.md).)</span><span class="sxs-lookup"><span data-stu-id="884c2-115">(See [DXVA Video Processing](dxva-video-processing.md).)</span></span>

<span data-ttu-id="884c2-116">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="884c2-116">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="884c2-117">**MF | atesourcereaderfromb-testream**</span><span class="sxs-lookup"><span data-stu-id="884c2-117">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="884c2-118">**Mfkreatesourcereaderfrommediasource**</span><span class="sxs-lookup"><span data-stu-id="884c2-118">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="884c2-119">**MF | atesourcereaderfromurl**</span><span class="sxs-lookup"><span data-stu-id="884c2-119">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="884c2-120">In der Regel legen Sie dieses Attribut fest, wenn Sie den Quell Reader verwenden, um decodierte Video Frames zu erhalten und die Frames mithilfe von Direct3D anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="884c2-120">Typically you would set this attribute if you are using the source reader to get decoded video frames and using Direct3D to display the frames.</span></span> <span data-ttu-id="884c2-121">Durch Festlegen dieses Attributs kann der Decoder DXVA verwenden.</span><span class="sxs-lookup"><span data-stu-id="884c2-121">Setting this attribute enables the decoder to use DXVA.</span></span>

<span data-ttu-id="884c2-122">Sie würden dieses Attribut nicht festlegen, wenn Folgendes:</span><span class="sxs-lookup"><span data-stu-id="884c2-122">You would not set this attribute if:</span></span>

-   <span data-ttu-id="884c2-123">Sie verwenden den Quell Reader, um nur Audioinhalte und keine Videos zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="884c2-123">You are using the source reader to process audio only and not video.</span></span>
-   <span data-ttu-id="884c2-124">Sie erhalten komprimierte Videos vom Quell-Reader.</span><span class="sxs-lookup"><span data-stu-id="884c2-124">You are getting compressed video from the source reader.</span></span> <span data-ttu-id="884c2-125">In diesem Fall erstellt der Quell Leser keinen Decoder.</span><span class="sxs-lookup"><span data-stu-id="884c2-125">In that case, the source reader does not create a decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="884c2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="884c2-126">Requirements</span></span>



| <span data-ttu-id="884c2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="884c2-127">Requirement</span></span> | <span data-ttu-id="884c2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="884c2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="884c2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="884c2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="884c2-130">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="884c2-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="884c2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="884c2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="884c2-132">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="884c2-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="884c2-133">Header</span><span class="sxs-lookup"><span data-stu-id="884c2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="884c2-134"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="884c2-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884c2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="884c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884c2-136">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="884c2-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="884c2-137">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="884c2-137">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="884c2-138">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="884c2-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




