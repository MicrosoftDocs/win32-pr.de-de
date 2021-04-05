---
description: Enthält einen vom Aufrufer definierten Wert für ein metransformmarker-Ereignis.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: MF_EVENT_MFT_CONTEXT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041958"
---
# <a name="mf_event_mft_context-attribute"></a><span data-ttu-id="78998-103">\_ \_ MFT- \_ Kontext Attribut für das MF-Ereignis</span><span class="sxs-lookup"><span data-stu-id="78998-103">MF\_EVENT\_MFT\_CONTEXT attribute</span></span>

<span data-ttu-id="78998-104">Enthält einen vom Aufrufer definierten Wert für ein [metransformmarker](metransformmarker.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="78998-104">Contains a caller-defined value for an [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="data-type"></a><span data-ttu-id="78998-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="78998-105">Data type</span></span>

<span data-ttu-id="78998-106">**Ulong \_** Als **UINT64** gespeicherter PTR</span><span class="sxs-lookup"><span data-stu-id="78998-106">**ULONG\_PTR** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="78998-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="78998-107">Get/set</span></span>

<span data-ttu-id="78998-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="78998-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="78998-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="78998-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="78998-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="78998-110">Applies to</span></span>

[<span data-ttu-id="78998-111">**IMF Media Event**</span><span class="sxs-lookup"><span data-stu-id="78998-111">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="78998-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78998-112">Remarks</span></span>

<span data-ttu-id="78998-113">Dieses Attribut wird mit dem [metransformmarker](metransformmarker.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="78998-113">This attribute is used with the [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="78998-114">Der Wert des-Attributs wird aus dem *ulparam* -Parameter der [**IMF Transform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) -Methode entnommen.</span><span class="sxs-lookup"><span data-stu-id="78998-114">The value of the attribute is taken from the *ulParam* parameter of the [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) method.</span></span>

<span data-ttu-id="78998-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="78998-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="78998-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78998-116">Requirements</span></span>



| <span data-ttu-id="78998-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78998-117">Requirement</span></span> | <span data-ttu-id="78998-118">Wert</span><span class="sxs-lookup"><span data-stu-id="78998-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78998-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78998-119">Minimum supported client</span></span><br/> | <span data-ttu-id="78998-120">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="78998-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="78998-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78998-121">Minimum supported server</span></span><br/> | <span data-ttu-id="78998-122">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="78998-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="78998-123">Header</span><span class="sxs-lookup"><span data-stu-id="78998-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="78998-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78998-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78998-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78998-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78998-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="78998-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="78998-127">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="78998-127">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="78998-128">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="78998-128">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




