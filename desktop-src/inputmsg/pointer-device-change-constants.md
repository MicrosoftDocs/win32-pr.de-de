---
title: Zeiger Geräte Änderung
description: Werte, die im wParam-Parameter der WM_POINTERDEVICECHANGE Nachricht übergeben werden können.
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5e4b85c17adcd2db7c0f2f672e27ca467b346b0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956838"
---
# <a name="pointer-device-change"></a><span data-ttu-id="05389-103">Zeiger Geräte Änderung</span><span class="sxs-lookup"><span data-stu-id="05389-103">Pointer Device Change</span></span>

<span data-ttu-id="05389-104">Werte, die im *wParam* -Parameter der [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) Nachricht übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="05389-104">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="05389-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="05389-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-106">0x001</span><span class="sxs-lookup"><span data-stu-id="05389-106">0x001</span></span>
</dt> <dt>



<span data-ttu-id="05389-107">Ein neues Gerät wird angefügt.</span><span class="sxs-lookup"><span data-stu-id="05389-107">A new device is attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span><span class="sxs-lookup"><span data-stu-id="05389-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-109">0x002</span><span class="sxs-lookup"><span data-stu-id="05389-109">0x002</span></span>
</dt> <dt>



<span data-ttu-id="05389-110">Ein Gerät wurde getrennt.</span><span class="sxs-lookup"><span data-stu-id="05389-110">A device has been detached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span><span class="sxs-lookup"><span data-stu-id="05389-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-112">0x004</span><span class="sxs-lookup"><span data-stu-id="05389-112">0x004</span></span>
</dt> <dt>



<span data-ttu-id="05389-113">Die Ausrichtung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="05389-113">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span><span class="sxs-lookup"><span data-stu-id="05389-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-115">0x008</span><span class="sxs-lookup"><span data-stu-id="05389-115">0x008</span></span>
</dt> <dt>



<span data-ttu-id="05389-116">Die Ausrichtung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="05389-116">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span><span class="sxs-lookup"><span data-stu-id="05389-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-118">0x010</span><span class="sxs-lookup"><span data-stu-id="05389-118">0x010</span></span>
</dt> <dt>



<span data-ttu-id="05389-119">Die Ausrichtung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="05389-119">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span><span class="sxs-lookup"><span data-stu-id="05389-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-121">0x020</span><span class="sxs-lookup"><span data-stu-id="05389-121">0x020</span></span>
</dt> <dt>



<span data-ttu-id="05389-122">Die Ausrichtung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="05389-122">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="05389-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-124">0x040</span><span class="sxs-lookup"><span data-stu-id="05389-124">0x040</span></span>
</dt> <dt>



<span data-ttu-id="05389-125">Der Standard Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="05389-125">The default display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span><span class="sxs-lookup"><span data-stu-id="05389-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-127">0x080</span><span class="sxs-lookup"><span data-stu-id="05389-127">0x080</span></span>
</dt> <dt>



<span data-ttu-id="05389-128">Zentrierter Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="05389-128">Centered display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="05389-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-130">0x100</span><span class="sxs-lookup"><span data-stu-id="05389-130">0x100</span></span>
</dt> <dt>



<span data-ttu-id="05389-131">Die Änderung in der Anzeige der Digitalisierungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="05389-131">The change in display to digitizer mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span><span class="sxs-lookup"><span data-stu-id="05389-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-133">0x200</span><span class="sxs-lookup"><span data-stu-id="05389-133">0x200</span></span>
</dt> <dt>



<span data-ttu-id="05389-134">Anzeige Auflösung.</span><span class="sxs-lookup"><span data-stu-id="05389-134">Display resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span><span class="sxs-lookup"><span data-stu-id="05389-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-136">0x400</span><span class="sxs-lookup"><span data-stu-id="05389-136">0x400</span></span>
</dt> <dt>



<span data-ttu-id="05389-137">Der Ursprung der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="05389-137">The display origin.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05389-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="05389-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05389-139">0x800</span><span class="sxs-lookup"><span data-stu-id="05389-139">0x800</span></span>
</dt> <dt>



<span data-ttu-id="05389-140">Das Seitenverhältnis der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="05389-140">The display aspect ratio.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05389-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05389-141">Requirements</span></span>



| <span data-ttu-id="05389-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05389-142">Requirement</span></span> | <span data-ttu-id="05389-143">Wert</span><span class="sxs-lookup"><span data-stu-id="05389-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05389-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05389-144">Minimum supported client</span></span><br/> | <span data-ttu-id="05389-145">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05389-145">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="05389-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05389-146">Minimum supported server</span></span><br/> | <span data-ttu-id="05389-147">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05389-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="05389-148">Header</span><span class="sxs-lookup"><span data-stu-id="05389-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="05389-149"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="05389-149"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05389-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05389-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05389-151">Konstanten</span><span class="sxs-lookup"><span data-stu-id="05389-151">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="05389-152">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="05389-152">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





