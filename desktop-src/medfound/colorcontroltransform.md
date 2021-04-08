---
description: Passt die Farbmerkmale eines Videostreams an.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Color Control Transform DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749345"
---
# <a name="color-control-transform-dsp"></a><span data-ttu-id="f1dec-103">Farb Steuerungs Transformation (DSP)</span><span class="sxs-lookup"><span data-stu-id="f1dec-103">Color Control Transform DSP</span></span>

<span data-ttu-id="f1dec-104">Passt die Farbmerkmale eines Videostreams an.</span><span class="sxs-lookup"><span data-stu-id="f1dec-104">Adjusts the color characteristics of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="f1dec-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="f1dec-105">CLSID</span></span>

<span data-ttu-id="f1dec-106">CLSID \_ ccolorcontroldmo</span><span class="sxs-lookup"><span data-stu-id="f1dec-106">CLSID\_CColorControlDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="f1dec-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f1dec-107">Interfaces</span></span>

-   <span data-ttu-id="f1dec-108">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="f1dec-108">**IMediaObject**</span></span>
-   <span data-ttu-id="f1dec-109">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="f1dec-109">**IMFTransform**</span></span>
-   <span data-ttu-id="f1dec-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="f1dec-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="f1dec-111">Formate</span><span class="sxs-lookup"><span data-stu-id="f1dec-111">Formats</span></span>

-   <span data-ttu-id="f1dec-112">RGB 24</span><span class="sxs-lookup"><span data-stu-id="f1dec-112">RGB 24</span></span>
-   <span data-ttu-id="f1dec-113">RGB 32</span><span class="sxs-lookup"><span data-stu-id="f1dec-113">RGB 32</span></span>
-   <span data-ttu-id="f1dec-114">RGB 555</span><span class="sxs-lookup"><span data-stu-id="f1dec-114">RGB 555</span></span>
-   <span data-ttu-id="f1dec-115">RGB 565</span><span class="sxs-lookup"><span data-stu-id="f1dec-115">RGB 565</span></span>
-   <span data-ttu-id="f1dec-116">Ayuv</span><span class="sxs-lookup"><span data-stu-id="f1dec-116">AYUV</span></span>
-   <span data-ttu-id="f1dec-117">UYVY</span><span class="sxs-lookup"><span data-stu-id="f1dec-117">UYVY</span></span>
-   <span data-ttu-id="f1dec-118">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="f1dec-118">YUY2</span></span>
-   <span data-ttu-id="f1dec-119">YV12</span><span class="sxs-lookup"><span data-stu-id="f1dec-119">YV12</span></span>

## <a name="properties"></a><span data-ttu-id="f1dec-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1dec-120">Properties</span></span>

-   [<span data-ttu-id="f1dec-121">mfpkey- \_ Farb \_ Helligkeit</span><span class="sxs-lookup"><span data-stu-id="f1dec-121">MFPKEY\_COLOR\_BRIGHTNESS</span></span>](mfpkey-color-brightness.md)
-   [<span data-ttu-id="f1dec-122">Kontrast zwischen mfpkey- \_ Farbe \_</span><span class="sxs-lookup"><span data-stu-id="f1dec-122">MFPKEY\_COLOR\_CONTRAST</span></span>](mfpkey-color-contrast.md)
-   [<span data-ttu-id="f1dec-123">mfpkey \_ - \_ farbfarbton</span><span class="sxs-lookup"><span data-stu-id="f1dec-123">MFPKEY\_COLOR\_HUE</span></span>](mfpkey-color-hue.md)
-   [<span data-ttu-id="f1dec-124">\_Farbsättigung für mfpkey \_</span><span class="sxs-lookup"><span data-stu-id="f1dec-124">MFPKEY\_COLOR\_SATURATION</span></span>](mfpkey-color-saturation.md)

## <a name="remarks"></a><span data-ttu-id="f1dec-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1dec-125">Remarks</span></span>

<span data-ttu-id="f1dec-126">Dieser DSP ändert den Inhalt des Videodaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="f1dec-126">This DSP modifies the contents of the video stream.</span></span> <span data-ttu-id="f1dec-127">Bei der Wiedergabe können Sie mit der **imfvideoprocessor** -Schnittstelle, die die Videoverarbeitung auf der Grafikkarte steuert, eine effizientere Wirkung erzielen.</span><span class="sxs-lookup"><span data-stu-id="f1dec-127">For playback, you might be able to achieve similar effects more efficiently by using the **IMFVideoProcessor** interface, which controls video processing in the graphics card.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1dec-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1dec-128">Requirements</span></span>



| <span data-ttu-id="f1dec-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1dec-129">Requirement</span></span> | <span data-ttu-id="f1dec-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f1dec-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dec-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1dec-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f1dec-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1dec-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f1dec-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1dec-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f1dec-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1dec-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1dec-135">Header</span><span class="sxs-lookup"><span data-stu-id="f1dec-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1dec-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1dec-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="f1dec-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f1dec-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1dec-138"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1dec-138"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f1dec-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1dec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1dec-140">Digitale Signal Prozessoren</span><span class="sxs-lookup"><span data-stu-id="f1dec-140">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




