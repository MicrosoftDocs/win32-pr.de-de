---
description: Gibt an, ob ein ASF-Bildstream ein abbaubarer JPEG-Typ ist.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862747"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a><span data-ttu-id="66efd-103">Das MF \_ MT- \_ Image \_ Verlust \_ tolerantes Attribut</span><span class="sxs-lookup"><span data-stu-id="66efd-103">MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute</span></span>

<span data-ttu-id="66efd-104">Gibt an, ob ein ASF-Bildstream ein abbaubarer JPEG-Typ ist.</span><span class="sxs-lookup"><span data-stu-id="66efd-104">Specifies whether an ASF image stream is a degradable JPEG type.</span></span>

## <a name="data-type"></a><span data-ttu-id="66efd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="66efd-105">Data type</span></span>

<span data-ttu-id="66efd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66efd-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="66efd-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="66efd-107">Get/set</span></span>

<span data-ttu-id="66efd-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="66efd-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="66efd-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="66efd-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="66efd-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="66efd-110">Applies to</span></span>

[<span data-ttu-id="66efd-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="66efd-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="66efd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66efd-112">Remarks</span></span>

<span data-ttu-id="66efd-113">Dieses Attribut gilt für den Medientyp für bildstreams in ASF.</span><span class="sxs-lookup"><span data-stu-id="66efd-113">This attribute applies to the media type for image streams in ASF.</span></span> <span data-ttu-id="66efd-114">Wenn der Wert **true** ist, ist der Datenstrom ein abbaubarer JPEG-Bildtyp.</span><span class="sxs-lookup"><span data-stu-id="66efd-114">If the value is **TRUE**, the stream is a degradable JPEG image type.</span></span> <span data-ttu-id="66efd-115">Andernfalls ist der Stream ein jff-Bildtyp.</span><span class="sxs-lookup"><span data-stu-id="66efd-115">Otherwise, the stream is a JFIF image type.</span></span> <span data-ttu-id="66efd-116">Weitere Informationen zu diesen Streamtypen finden Sie in der ASF-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="66efd-116">For more information about these stream types, see the ASF specification.</span></span>

<span data-ttu-id="66efd-117">Zusätzlich zum Attribut "MF \_ MT \_ Image \_ Loss \_ tolerante" enthält der Medientyp für einen ASF-Bildstream die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="66efd-117">In addition to the MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute, the media type for an ASF image stream contains the following attributes:</span></span>



| <span data-ttu-id="66efd-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="66efd-118">Attribute</span></span>                                                 | <span data-ttu-id="66efd-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66efd-119">Description</span></span>                                |
|-----------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="66efd-120">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="66efd-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="66efd-121">Enthält den Wert des **MF MediaType- \_ Bilds**.</span><span class="sxs-lookup"><span data-stu-id="66efd-121">Contains the value **MFMediaType\_Image**.</span></span> |
| [<span data-ttu-id="66efd-122">**MF- \_ MT- \_ Frame \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="66efd-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md) | <span data-ttu-id="66efd-123">Gibt die Bildgröße in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="66efd-123">Gives the image size in pixels.</span></span>            |



 

<span data-ttu-id="66efd-124">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="66efd-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66efd-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66efd-125">Requirements</span></span>



| <span data-ttu-id="66efd-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66efd-126">Requirement</span></span> | <span data-ttu-id="66efd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="66efd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66efd-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66efd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66efd-129">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="66efd-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="66efd-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66efd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66efd-131">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="66efd-131">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="66efd-132">Header</span><span class="sxs-lookup"><span data-stu-id="66efd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="66efd-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="66efd-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66efd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66efd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66efd-135">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="66efd-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66efd-136">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="66efd-136">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




