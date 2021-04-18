---
description: Tragbare Windows-Geräte unterstützen die folgenden Abbild Eigenschaften.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Bildeigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371562"
---
# <a name="image-properties"></a><span data-ttu-id="a9ba6-103">Bildeigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9ba6-103">Image Properties</span></span>

<span data-ttu-id="a9ba6-104">Tragbare Windows-Geräte unterstützen die folgenden Abbild Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-104">Windows Portable Devices supports the following image properties.</span></span>



| <span data-ttu-id="a9ba6-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a9ba6-105">Property</span></span>                                                                                                                                       | <span data-ttu-id="a9ba6-106">VarType</span><span class="sxs-lookup"><span data-stu-id="a9ba6-106">VarType</span></span>     | <span data-ttu-id="a9ba6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9ba6-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ba6-108">**Bittiefe des WPD- \_ Bilds \_**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-108">**WPD\_IMAGE\_BITDEPTH**</span></span>                                                                                                                       | <span data-ttu-id="a9ba6-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-109">**VT\_UI4**</span></span> | <span data-ttu-id="a9ba6-110">Die Bittiefe des Bilds.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-110">The bit depth of the image.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a9ba6-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**Status der \_ \_ \_ korrigierten WPD-Bild Farbe \_**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS**</span></span> | <span data-ttu-id="a9ba6-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-112">**VT\_UI4**</span></span> | <span data-ttu-id="a9ba6-113">Eine mit der [**WPD- \_ Farbe \_ korrigierte \_ \_ statusvalues**](wpd-color-corrected-status-values.md) -Enumeration, die angibt, ob die Datei farblich korrigiert wurde. Dadurch wird verhindert, dass mehrere Geräte bei der Nachbearbeitung automatisch eine Farbkorrektur des Bilds vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-113">A [**WPD\_COLOR\_CORRECTED\_STATUS\_VALUES**](wpd-color-corrected-status-values.md) enumeration that specifies whether the file has been color-corrected.This prevents multiple devices from automatically color-correcting the image during post-processing.</span></span><br/>                                                                       |
| <span data-ttu-id="a9ba6-114">**ausgeschnittener WPD- \_ Image \_ \_ Status**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-114">**WPD\_IMAGE\_CROPPED\_STATUS**</span></span>                                                                                                                | <span data-ttu-id="a9ba6-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-115">**VT\_UI4**</span></span> | <span data-ttu-id="a9ba6-116">Eine von [**WPD ausgeschnittene \_ \_ statuswertenenumeration \_**](wpd-cropped-status-values.md) , die angibt, ob die Datei abgeschnitten wurde. Dadurch wird verhindert, dass mehrere Geräte das Image während der Nachbearbeitung automatisch zuschneiden.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-116">A [**WPD\_CROPPED\_STATUS\_VALUES**](wpd-cropped-status-values.md) enumeration that specifies whether the file has been cropped.This prevents multiple devices from automatically cropping the image during post-processing.</span></span><br/>                                                                                                        |
| <span data-ttu-id="a9ba6-117">**Index für WPD- \_ Image verfügbar \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-117">**WPD\_IMAGE\_EXPOSURE\_INDEX**</span></span>                                                                                                                | <span data-ttu-id="a9ba6-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-118">**VT\_UI4**</span></span> | <span data-ttu-id="a9ba6-119">Ein-Wert, der die Einstellungen der Folien Geschwindigkeit identifiziert, wenn dieses Bild aufgezeichnet wurde. Die Einstellungen entsprechen den ISO-Bezeichnungen von ASA/DIN.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-119">A value that identifies the film speed settings when this image was captured.The settings correspond to the ISO designations of ASA/DIN.</span></span><br/> <span data-ttu-id="a9ba6-120">In der Regel unterstützt ein Gerät diskrete Enumerationswerte, aber eine kontinuierliche Kontrolle über einen Bereich ist möglich.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-120">Typically, a device supports discrete enumerated values, but continuous control over a range is possible.</span></span><br/> <span data-ttu-id="a9ba6-121">Der Wert 0xFFFFFFFF entspricht der automatischen ISO-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-121">A value of 0xFFFFFFFF corresponds to automatic ISO setting.</span></span><br/> |
| <span data-ttu-id="a9ba6-122">**Anzeigezeit für WPD- \_ Image \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-122">**WPD\_IMAGE\_EXPOSURE\_TIME**</span></span>                                                                                                                 | <span data-ttu-id="a9ba6-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-123">**VT\_UI4**</span></span> | <span data-ttu-id="a9ba6-124">Gibt die Auslösegeschwindigkeit des Geräts an, als das Abbild erfasst wurde. Einheiten werden in Sekunden von 10000 skaliert.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-124">Identifies the shutter speed of the device when this image was captured.Units are in seconds scaled by 10000.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="a9ba6-125">**WPD- \_ Image- \_ Nummer**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-125">**WPD\_IMAGE\_FNUMBER**</span></span>                                                                                                                        | <span data-ttu-id="a9ba6-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-126">**VT\_UI4**</span></span> | <span data-ttu-id="a9ba6-127">Gibt die Einstellung für die Öffnung des Bilds an, wenn dieses Bild aufgezeichnet wurde. Einheiten sind gleich der durch 100 skalierten f-Nummer.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-127">Identifies the aperture setting of the lens when this image was captured.Units are equal to the f-number scaled by 100.</span></span><br/>                                                                                                                                                                                                              |
| <span data-ttu-id="a9ba6-128">**horizontale Auflösung des WPD- \_ Bilds \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-128">**WPD\_IMAGE\_HORIZONTAL\_RESOLUTION**</span></span>                                                                                                         | <span data-ttu-id="a9ba6-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-129">**VT\_R8**</span></span>  | <span data-ttu-id="a9ba6-130">Gibt die horizontale Auflösung eines Bilds in dpi (dots per inch) an.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-130">Indicates the horizontal resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a9ba6-131">**vertikale Auflösung des WPD- \_ Bilds \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-131">**WPD\_IMAGE\_VERTICAL\_RESOLUTION**</span></span>                                                                                                           | <span data-ttu-id="a9ba6-132">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-132">**VT\_R8**</span></span>  | <span data-ttu-id="a9ba6-133">Gibt die vertikale Auflösung eines Bilds in dpi (dots per inch) an.</span><span class="sxs-lookup"><span data-stu-id="a9ba6-133">Indicates the vertical resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a9ba6-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9ba6-134">Requirements</span></span>



| <span data-ttu-id="a9ba6-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9ba6-135">Requirement</span></span> | <span data-ttu-id="a9ba6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a9ba6-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ba6-137">Header</span><span class="sxs-lookup"><span data-stu-id="a9ba6-137">Header</span></span><br/> | <dl> <span data-ttu-id="a9ba6-138"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ba6-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9ba6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9ba6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ba6-140">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="a9ba6-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




