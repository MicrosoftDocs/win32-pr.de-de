---
description: Gibt an, ob es sich bei einer Video Erfassungs Quelle um ein Hardware Gerät oder ein Software Gerät handelt.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350548"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a><span data-ttu-id="ac2ba-103">MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ HW \_ Quell Attribut</span><span class="sxs-lookup"><span data-stu-id="ac2ba-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_HW\_SOURCE attribute</span></span>

<span data-ttu-id="ac2ba-104">Gibt an, ob es sich bei einer Video Erfassungs Quelle um ein Hardware Gerät oder ein Software Gerät handelt.</span><span class="sxs-lookup"><span data-stu-id="ac2ba-104">Specifies whether a video capture source is a hardware device or a software device.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac2ba-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ac2ba-105">Data type</span></span>

<span data-ttu-id="ac2ba-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ac2ba-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ac2ba-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="ac2ba-107">Get/set</span></span>

<span data-ttu-id="ac2ba-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ac2ba-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ac2ba-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ac2ba-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac2ba-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac2ba-110">Remarks</span></span>

<span data-ttu-id="ac2ba-111">Wenn der Wert **true** ist, ist die Erfassungs Quelle ein Hardware Gerät.</span><span class="sxs-lookup"><span data-stu-id="ac2ba-111">If the value is **TRUE**, the capture source is a hardware device.</span></span> <span data-ttu-id="ac2ba-112">Wenn der Wert **false** lautet, handelt es sich um ein Software Gerät.</span><span class="sxs-lookup"><span data-stu-id="ac2ba-112">If the value is **FALSE**, it is a software device.</span></span> <span data-ttu-id="ac2ba-113">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ac2ba-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="ac2ba-114">Dieses Attribut wird für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="ac2ba-114">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="ac2ba-115">**MF | atedevicesourceaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="ac2ba-115">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="ac2ba-116">**Mfenumschlag**</span><span class="sxs-lookup"><span data-stu-id="ac2ba-116">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="ac2ba-117">Das-Attribut gilt nur für Video Erfassungsgeräte.</span><span class="sxs-lookup"><span data-stu-id="ac2ba-117">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="ac2ba-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ac2ba-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2ba-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac2ba-119">Requirements</span></span>



| <span data-ttu-id="ac2ba-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac2ba-120">Requirement</span></span> | <span data-ttu-id="ac2ba-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ac2ba-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2ba-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac2ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac2ba-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac2ba-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac2ba-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac2ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac2ba-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac2ba-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ac2ba-126">Header</span><span class="sxs-lookup"><span data-stu-id="ac2ba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac2ba-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac2ba-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac2ba-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac2ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2ba-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ac2ba-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac2ba-130">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="ac2ba-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="ac2ba-131">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="ac2ba-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




