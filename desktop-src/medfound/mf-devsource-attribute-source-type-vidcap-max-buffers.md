---
description: Gibt die maximale Anzahl von Frames an, die von der Video Erfassungs Quelle gepuffert werden.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346986"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a><span data-ttu-id="de10a-103">MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ Maximales \_ Puffer Attribut</span><span class="sxs-lookup"><span data-stu-id="de10a-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_MAX\_BUFFERS attribute</span></span>

<span data-ttu-id="de10a-104">Gibt die maximale Anzahl von Frames an, die von der Video Erfassungs Quelle gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="de10a-104">Specifies the maximum number of frames that the video capture source will buffer.</span></span>

## <a name="data-type"></a><span data-ttu-id="de10a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="de10a-105">Data type</span></span>

<span data-ttu-id="de10a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="de10a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="de10a-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="de10a-107">Get/set</span></span>

<span data-ttu-id="de10a-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="de10a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="de10a-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="de10a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="de10a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de10a-110">Remarks</span></span>

<span data-ttu-id="de10a-111">Standardmäßig puffert die Video Erfassungs Quelle maximal einen Frame gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="de10a-111">By default, the video capture source buffers a maximum of one frame at a time.</span></span> <span data-ttu-id="de10a-112">Sie können das Puffer Limit erhöhen, indem Sie dieses Attribut festlegen.</span><span class="sxs-lookup"><span data-stu-id="de10a-112">You can increase the buffer limit by setting this attribute.</span></span>

<span data-ttu-id="de10a-113">Die richtige Methode zum Festlegen dieses Attributs hängt von der Funktion ab, die zum Erstellen der Medienquelle verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="de10a-113">The correct way to set this attribute depends on the function used to create the media source:</span></span>

-   <span data-ttu-id="de10a-114">[**MF | atedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Legen Sie das Attribut über den *pattributes* -Parameter der Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="de10a-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="de10a-115">[**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Legen Sie das Attribut über den *pattributes* -Parameter der Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="de10a-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="de10a-116">[**Mfenumdebug**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Legen Sie das-Attribut für den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger fest, der von der-Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="de10a-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Set the attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned by the function.</span></span> <span data-ttu-id="de10a-117">Legen Sie das-Attribut vor dem Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)fest.</span><span class="sxs-lookup"><span data-stu-id="de10a-117">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="de10a-118">Das-Attribut gilt nur für Video Erfassungsgeräte.</span><span class="sxs-lookup"><span data-stu-id="de10a-118">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="de10a-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="de10a-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="de10a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de10a-120">Requirements</span></span>



| <span data-ttu-id="de10a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de10a-121">Requirement</span></span> | <span data-ttu-id="de10a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="de10a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de10a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de10a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="de10a-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de10a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="de10a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de10a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="de10a-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de10a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="de10a-127">Header</span><span class="sxs-lookup"><span data-stu-id="de10a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="de10a-128"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de10a-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de10a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de10a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de10a-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="de10a-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de10a-131">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="de10a-131">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="de10a-132">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="de10a-132">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




