---
description: Gibt die Gerätekategorie für ein Video Erfassungsgerät an.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129785"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a><span data-ttu-id="80b9f-103">MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ Category-Attribut</span><span class="sxs-lookup"><span data-stu-id="80b9f-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_CATEGORY attribute</span></span>

<span data-ttu-id="80b9f-104">Gibt die Gerätekategorie für ein Video Erfassungsgerät an.</span><span class="sxs-lookup"><span data-stu-id="80b9f-104">Specifies the device category for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="80b9f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="80b9f-105">Data type</span></span>

<span data-ttu-id="80b9f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="80b9f-106">**GUID**</span></span>

<span data-ttu-id="80b9f-107">Der folgende Wert ist definiert.</span><span class="sxs-lookup"><span data-stu-id="80b9f-107">The following value is defined.</span></span>



| <span data-ttu-id="80b9f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="80b9f-108">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="80b9f-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="80b9f-109">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <span data-ttu-id="80b9f-110"><dt>**CLSID \_ videoinputentvicecategory**</dt></span><span class="sxs-lookup"><span data-stu-id="80b9f-110"><dt>**CLSID\_VideoInputDeviceCategory**</dt></span></span> </dl> | <span data-ttu-id="80b9f-111">Video Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="80b9f-111">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="80b9f-112">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="80b9f-112">Get/set</span></span>

<span data-ttu-id="80b9f-113">Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.</span><span class="sxs-lookup"><span data-stu-id="80b9f-113">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="80b9f-114">Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.</span><span class="sxs-lookup"><span data-stu-id="80b9f-114">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="80b9f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80b9f-115">Remarks</span></span>

<span data-ttu-id="80b9f-116">Verwenden Sie dieses Attribut als Eingabe für die [**mfenumtvicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion, wenn Sie Video Erfassungsgeräte aufzählen.</span><span class="sxs-lookup"><span data-stu-id="80b9f-116">Use this attribute as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function when enumerating video capture devices.</span></span>

<span data-ttu-id="80b9f-117">Außerdem wird dieses Attribut für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="80b9f-117">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="80b9f-118">**MF | atedevicesourceaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="80b9f-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="80b9f-119">**Mfenumschlag**</span><span class="sxs-lookup"><span data-stu-id="80b9f-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="80b9f-120">Das-Attribut gilt nur für Video Erfassungsgeräte.</span><span class="sxs-lookup"><span data-stu-id="80b9f-120">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="80b9f-121">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="80b9f-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b9f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80b9f-122">Requirements</span></span>



| <span data-ttu-id="80b9f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80b9f-123">Requirement</span></span> | <span data-ttu-id="80b9f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="80b9f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80b9f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80b9f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="80b9f-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80b9f-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="80b9f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80b9f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="80b9f-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80b9f-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="80b9f-129">Header</span><span class="sxs-lookup"><span data-stu-id="80b9f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b9f-130"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b9f-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b9f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80b9f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b9f-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="80b9f-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80b9f-133">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="80b9f-133">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="80b9f-134">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="80b9f-134">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




