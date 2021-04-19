---
description: GUID des Haupt Typs für einen Medientyp.
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: MF_MT_MAJOR_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348199"
---
# <a name="mf_mt_major_type-attribute"></a><span data-ttu-id="a4236-103">\_ \_ Haupt \_ Attribut von MF MT</span><span class="sxs-lookup"><span data-stu-id="a4236-103">MF\_MT\_MAJOR\_TYPE attribute</span></span>

<span data-ttu-id="a4236-104">GUID des Haupt Typs für einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="a4236-104">Major type GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4236-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a4236-105">Data type</span></span>

<span data-ttu-id="a4236-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a4236-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a4236-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4236-107">Remarks</span></span>

<span data-ttu-id="a4236-108">Der Haupttyp definiert die Gesamtkategorie der Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="a4236-108">The major type defines the overall category of the media data.</span></span> <span data-ttu-id="a4236-109">Zu den Haupttypen gehören Videos, Audiodateien, Skripts usw.</span><span class="sxs-lookup"><span data-stu-id="a4236-109">Major types include video, audio, script, and so forth.</span></span> <span data-ttu-id="a4236-110">Eine Liste möglicher Werte finden Sie unter [Hauptmedien Typen](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a4236-110">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="a4236-111">Eine alternative Möglichkeit zum Abrufen dieses Attributs ist das Aufrufen von [**imfmediatype:: getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="a4236-111">An alternate way to retrieve this attribute is to call [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span></span>

<span data-ttu-id="a4236-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a4236-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4236-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4236-113">Requirements</span></span>



| <span data-ttu-id="a4236-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4236-114">Requirement</span></span> | <span data-ttu-id="a4236-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a4236-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4236-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4236-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a4236-117">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a4236-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a4236-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4236-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a4236-119">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a4236-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a4236-120">Header</span><span class="sxs-lookup"><span data-stu-id="a4236-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4236-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4236-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4236-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4236-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4236-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a4236-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4236-124">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="a4236-124">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a4236-125">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="a4236-125">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a4236-126">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="a4236-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a4236-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="a4236-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




