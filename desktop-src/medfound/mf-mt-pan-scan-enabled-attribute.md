---
description: Gibt an, ob der Pan/Scan-Modus aktiviert ist.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528754"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a><span data-ttu-id="2b526-103">Das MF \_ MT \_ Pan Scan- \_ \_ aktiviertes Attribut</span><span class="sxs-lookup"><span data-stu-id="2b526-103">MF\_MT\_PAN\_SCAN\_ENABLED attribute</span></span>

<span data-ttu-id="2b526-104">Gibt an, ob der Pan/Scan-Modus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2b526-104">Specifies whether pan/scan mode is enabled.</span></span>

## <a name="data-type"></a><span data-ttu-id="2b526-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2b526-105">Data type</span></span>

<span data-ttu-id="2b526-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2b526-106">**UINT32**</span></span>

<span data-ttu-id="2b526-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="2b526-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b526-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b526-108">Remarks</span></span>

<span data-ttu-id="2b526-109">Wenn dieses Attribut den Wert **true** hat, sollte nur der Pan/Scan-Bereich des Videos angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2b526-109">If this attribute is **TRUE**, only the pan/scan region of the video should be displayed.</span></span> <span data-ttu-id="2b526-110">Der Pan/Scan-Bereich wird durch das [**MF \_ MT \_ Pan \_ Scan \_ Aperture**](mf-mt-pan-scan-aperture-attribute.md) -Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b526-110">The pan/scan region is specified by the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="2b526-111">Wenn dieses Attribut **false** ist oder nicht festgelegt ist, sollte die gesamte Anzeige Öffnung des Videos angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2b526-111">If this attribute is **FALSE** or not set, the entire display aperture of the video should be displayed.</span></span> <span data-ttu-id="2b526-112">Die Anzeige Öffnung wird durch das [**MF \_ MT- \_ minimale \_ Display \_ Aperture**](mf-mt-minimum-display-aperture-attribute.md) -Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b526-112">The display aperture is specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="2b526-113">Wenn Sie dieses Attribut auf " **true**" festlegen, legen Sie auch den Wert des [**MF \_ MT \_ Pan \_ Scan \_ Aperture**](mf-mt-pan-scan-aperture-attribute.md) -Attributs fest.</span><span class="sxs-lookup"><span data-stu-id="2b526-113">If you set this attribute to **TRUE**, also set the value of the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="2b526-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="2b526-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b526-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b526-115">Requirements</span></span>



| <span data-ttu-id="2b526-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b526-116">Requirement</span></span> | <span data-ttu-id="2b526-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2b526-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b526-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b526-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2b526-119">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2b526-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2b526-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b526-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2b526-121">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2b526-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2b526-122">Header</span><span class="sxs-lookup"><span data-stu-id="2b526-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b526-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b526-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b526-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b526-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b526-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2b526-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b526-126">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2b526-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2b526-127">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2b526-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2b526-128">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="2b526-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2b526-129">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="2b526-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b526-130">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="2b526-130">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




