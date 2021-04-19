---
description: Gibt einen Gerätetyp an, z. b. Audioerfassung oder Video Erfassung.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359882"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a><span data-ttu-id="017a7-103">\_ \_ \_ Quelltyp Attribut des MF-devsource-Attributs \_</span><span class="sxs-lookup"><span data-stu-id="017a7-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE attribute</span></span>

<span data-ttu-id="017a7-104">Gibt den Typ eines Geräts an, z. b. Audioerfassung oder Video Erfassung.</span><span class="sxs-lookup"><span data-stu-id="017a7-104">Specifies a device's type, such as audio capture or video capture.</span></span>

## <a name="data-type"></a><span data-ttu-id="017a7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="017a7-105">Data type</span></span>

<span data-ttu-id="017a7-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="017a7-106">**GUID**</span></span>

<span data-ttu-id="017a7-107">Die folgenden Werte sind für dieses Attribut definiert:</span><span class="sxs-lookup"><span data-stu-id="017a7-107">The following values are defined for this attribute:</span></span>



| <span data-ttu-id="017a7-108">Wert</span><span class="sxs-lookup"><span data-stu-id="017a7-108">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="017a7-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="017a7-109">Meaning</span></span>                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <span data-ttu-id="017a7-110"><dt>**MF \_ devsource \_ - \_ Attribut \_ Quelltyp ( \_ audcap- \_ GUID)**</dt></span><span class="sxs-lookup"><span data-stu-id="017a7-110"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="017a7-111">Audioerfassungs Gerät.</span><span class="sxs-lookup"><span data-stu-id="017a7-111">Audio capture device.</span></span><br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <span data-ttu-id="017a7-112"><dt>**MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="017a7-112"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="017a7-113">Video Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="017a7-113">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="017a7-114">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="017a7-114">Get/set</span></span>

<span data-ttu-id="017a7-115">Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.</span><span class="sxs-lookup"><span data-stu-id="017a7-115">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="017a7-116">Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.</span><span class="sxs-lookup"><span data-stu-id="017a7-116">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="017a7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="017a7-117">Remarks</span></span>

<span data-ttu-id="017a7-118">Verwenden Sie dieses Attribut als Eingabe für die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="017a7-118">Use this attribute as input to the following functions:</span></span>

-   [<span data-ttu-id="017a7-119">**MF | atedevicesource**</span><span class="sxs-lookup"><span data-stu-id="017a7-119">**MFCreateDeviceSource**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [<span data-ttu-id="017a7-120">**MF | atedevicesourceaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="017a7-120">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="017a7-121">**Mfenumschlag**</span><span class="sxs-lookup"><span data-stu-id="017a7-121">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="017a7-122">Außerdem wird dieses Attribut für die Aktivierungs Objekte festgelegt, die von der [**mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="017a7-122">In addition, this attribute is set on the activation objects returned by the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span>

<span data-ttu-id="017a7-123">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="017a7-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="017a7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="017a7-124">Requirements</span></span>



| <span data-ttu-id="017a7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="017a7-125">Requirement</span></span> | <span data-ttu-id="017a7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="017a7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="017a7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="017a7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="017a7-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="017a7-128">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="017a7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="017a7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="017a7-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="017a7-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="017a7-131">Header</span><span class="sxs-lookup"><span data-stu-id="017a7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="017a7-132"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="017a7-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="017a7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="017a7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017a7-134">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="017a7-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="017a7-135">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="017a7-135">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="017a7-136">Geräte Attribute erfassen</span><span class="sxs-lookup"><span data-stu-id="017a7-136">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




