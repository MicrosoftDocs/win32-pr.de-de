---
description: Pixel Seitenverhältnis für einen Video Medientyp.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526600"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a><span data-ttu-id="e22d5-103">Attribut für das MF- \_ \_ Pixel- \_ Seiten \_ Verhältnis</span><span class="sxs-lookup"><span data-stu-id="e22d5-103">MF\_MT\_PIXEL\_ASPECT\_RATIO attribute</span></span>

<span data-ttu-id="e22d5-104">Pixel Seitenverhältnis für einen Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="e22d5-104">Pixel aspect ratio for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e22d5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e22d5-105">Data type</span></span>

<span data-ttu-id="e22d5-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e22d5-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="e22d5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e22d5-107">Remarks</span></span>

<span data-ttu-id="e22d5-108">Die oberen 32 Bits enthalten den Zähler des Pixel Seitenverhältnisses und die unteren 32 Bits enthalten den Nenner.</span><span class="sxs-lookup"><span data-stu-id="e22d5-108">The upper 32 bits contain the numerator of the pixel aspect ratio and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="e22d5-109">Der Zähler ist die horizontale Komponente des Seitenverhältnisses. der Nenner ist die vertikale Komponente.</span><span class="sxs-lookup"><span data-stu-id="e22d5-109">The numerator is the horizontal component of the aspect ratio; the denominator is the vertical component.</span></span>

<span data-ttu-id="e22d5-110">Um dieses Attribut festzulegen, verwenden Sie die [**mfsetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e22d5-110">To set this attribute, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="e22d5-111">Um dieses Attribut zu erhalten, verwenden Sie die [**mfgetattributeratio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e22d5-111">To get this attribute, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="e22d5-112">Das Pixel Seitenverhältnis beschreibt die Form der Pixel im angezeigten Videobild.</span><span class="sxs-lookup"><span data-stu-id="e22d5-112">The pixel aspect ratio describes the shape of the pixels in the displayed video image.</span></span> <span data-ttu-id="e22d5-113">Legen Sie dieses Attribut fest, wenn das Bild nicht eckige Pixel enthält.</span><span class="sxs-lookup"><span data-stu-id="e22d5-113">Set this attribute if the image has non-square pixels.</span></span> <span data-ttu-id="e22d5-114">Damit das Bild auf einem Anzeigegerät mit quadratischen Pixeln ordnungsgemäß angezeigt werden kann, muss es mit der Umkehrung des Pixel Seitenverhältnisses des Bilds skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="e22d5-114">To display correctly on a display device with square pixels, the image must be scaled by the inverse of the image's pixel aspect ratio.</span></span>

<span data-ttu-id="e22d5-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e22d5-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e22d5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e22d5-116">Requirements</span></span>



| <span data-ttu-id="e22d5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e22d5-117">Requirement</span></span> | <span data-ttu-id="e22d5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e22d5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e22d5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e22d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e22d5-120">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e22d5-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e22d5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e22d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e22d5-122">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e22d5-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e22d5-123">Header</span><span class="sxs-lookup"><span data-stu-id="e22d5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e22d5-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e22d5-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22d5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e22d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22d5-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e22d5-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e22d5-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="e22d5-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="e22d5-128">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e22d5-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e22d5-129">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="e22d5-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




