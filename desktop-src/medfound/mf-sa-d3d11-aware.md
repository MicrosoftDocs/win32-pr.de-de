---
description: Gibt an, ob eine Media Foundation Transformation (MFT) Microsoft Direct3D 11 unterstützt.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344178"
---
# <a name="mf_sa_d3d11_aware-attribute"></a><span data-ttu-id="24661-103">MF \_ sa \_ D3D11 \_ Aware-Attribut</span><span class="sxs-lookup"><span data-stu-id="24661-103">MF\_SA\_D3D11\_AWARE attribute</span></span>

<span data-ttu-id="24661-104">Gibt an, ob eine Media Foundation Transformation (MFT) Microsoft Direct3D 11 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24661-104">Specifies whether a Media Foundation transform (MFT) supports Microsoft Direct3D 11.</span></span>

## <a name="data-type"></a><span data-ttu-id="24661-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="24661-105">Data type</span></span>

<span data-ttu-id="24661-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24661-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="24661-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24661-107">Remarks</span></span>

<span data-ttu-id="24661-108">Dieses Attribut gilt nur für Video-MFTs.</span><span class="sxs-lookup"><span data-stu-id="24661-108">This attribute applies only to video MFTs.</span></span> <span data-ttu-id="24661-109">Um dieses Attribut abzufragen, müssen Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den MFT-Attribut Speicher zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="24661-109">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT attribute store.</span></span> <span data-ttu-id="24661-110">Wenn **GetAttributes** erfolgreich ist, können Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="24661-110">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

-   <span data-ttu-id="24661-111">Wenn das-Attribut ungleich NULL ist, kann der Client dem MFT einen Zeiger auf die [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle übergeben, bevor das Streaming gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="24661-111">If the attribute is nonzero, the client can give the MFT a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface before streaming starts.</span></span> <span data-ttu-id="24661-112">Hierzu sendet der Client die [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht an die MFT.</span><span class="sxs-lookup"><span data-stu-id="24661-112">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="24661-113">Der Client muss diese Nachricht nicht senden.</span><span class="sxs-lookup"><span data-stu-id="24661-113">The client is not required to send this message.</span></span>
-   <span data-ttu-id="24661-114">Wenn dieses Attribut NULL (**false**) ist, wird Direct3D 11 von der MFT nicht unterstützt, und der Client sollte die [**MFT- \_ Nachricht \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) nicht an die MFT senden.</span><span class="sxs-lookup"><span data-stu-id="24661-114">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 11, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="24661-115">Der Standardwert dieses Attributs ist **false**.</span><span class="sxs-lookup"><span data-stu-id="24661-115">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="24661-116">Behandeln Sie dieses Attribut als schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="24661-116">Treat this attribute as read-only.</span></span> <span data-ttu-id="24661-117">Ändern Sie den Wert nicht. die MFT ignoriert alle Änderungen am Wert.</span><span class="sxs-lookup"><span data-stu-id="24661-117">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24661-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24661-118">Requirements</span></span>



| <span data-ttu-id="24661-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24661-119">Requirement</span></span> | <span data-ttu-id="24661-120">Wert</span><span class="sxs-lookup"><span data-stu-id="24661-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="24661-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24661-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24661-122">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="24661-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="24661-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24661-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24661-124">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="24661-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="24661-125">Header</span><span class="sxs-lookup"><span data-stu-id="24661-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24661-126"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="24661-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24661-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24661-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24661-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="24661-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="24661-129">Unterstützung von Direct3D 11 Video Decodierung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24661-129">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




