---
description: Gibt den nominalen Bereich der Farbinformationen in einem Video Medientyp an.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: MF_MT_VIDEO_NOMINAL_RANGE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355419"
---
# <a name="mf_mt_video_nominal_range-attribute"></a><span data-ttu-id="f8829-103">\_Attribut des \_ \_ \_ Attributs "MF MT-Video"</span><span class="sxs-lookup"><span data-stu-id="f8829-103">MF\_MT\_VIDEO\_NOMINAL\_RANGE attribute</span></span>

<span data-ttu-id="f8829-104">Gibt den nominalen Bereich der Farbinformationen in einem Video Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="f8829-104">Specifies the nominal range of the color information in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="f8829-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f8829-105">Data type</span></span>

<span data-ttu-id="f8829-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f8829-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f8829-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8829-107">Remarks</span></span>

<span data-ttu-id="f8829-108">Der Wert dieses Attributs ist ein Member der [**mfnominalrange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="f8829-108">The value of this attribute is a member of the [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) enumeration.</span></span>

<span data-ttu-id="f8829-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="f8829-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

<span data-ttu-id="f8829-110">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="f8829-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="f8829-111">Für den Ausgabe Medientyp kann der \_ \_ \_ nominale Bereich des MF MT-Videos \_ mit **MF nominalrange \_ 0 \_ 255** und **MF nominalrange \_ 16 \_ 235** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f8829-111">On the output media type, MF\_MT\_VIDEO\_NOMINAL\_RANGE can be set with **MFNominalRange\_0\_255** and **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="f8829-112">Der H. 264/AVC-Encoder muss " **MF nominalrange \_ Unknown** " als " **MF nominalrange \_ 16 \_ 235**" behandeln.</span><span class="sxs-lookup"><span data-stu-id="f8829-112">H.264/AVC encoder shall treat **MFNominalRange\_Unknown** as **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="f8829-113">Der H. 264/AVC-Encoder muss einen Ausgabe Medientyp ablehnen, wenn der \_ nominale Bereich des MF MT- \_ Videos \_ \_ auf **mfnominalrange \_ 48 \_ 208**, **mfnominalrange \_ 64 \_ 127** oder andere Werte, die nicht für [**mfnominalrange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange)definiert sind, festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f8829-113">H.264/AVC encoder shall reject a output media type when MF\_MT\_VIDEO\_NOMINAL\_RANGE is set to **MFNominalRange\_48\_208**, **MFNominalRange\_64\_127**, or any other values not defined on [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8829-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8829-114">Requirements</span></span>



| <span data-ttu-id="f8829-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8829-115">Requirement</span></span> | <span data-ttu-id="f8829-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f8829-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8829-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8829-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8829-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f8829-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f8829-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8829-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8829-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f8829-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f8829-121">Header</span><span class="sxs-lookup"><span data-stu-id="f8829-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8829-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8829-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8829-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8829-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8829-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f8829-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f8829-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f8829-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f8829-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f8829-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f8829-127">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="f8829-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f8829-128">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="f8829-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="f8829-129">Erweiterte Farbinformationen</span><span class="sxs-lookup"><span data-stu-id="f8829-129">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




