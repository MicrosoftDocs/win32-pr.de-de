---
title: DRM_LICENSE_STATE_CATEGORY-Enumeration (drmexternals. h)
description: Der \_ \_ Enumerationstyp der DRM-Lizenzstatus \_ Kategorie definiert die Kategorien für DRM-Lizenz Zeichenfolgen, die dem Benutzer angezeigt werden.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- DRM_LICENSE_STATE_CATEGORY-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40763ec7f610073784e3bd1516d4c955abcd65b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477943"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a><span data-ttu-id="2c3ca-105">DRM_LICENSE_STATE_CATEGORY-Enumeration (drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="2c3ca-105">DRM_LICENSE_STATE_CATEGORY enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="2c3ca-106">Der Enumerationstyp der **DRM- \_ Lizenz \_ Status \_ Kategorie** definiert die Kategorien für DRM- [*Lizenz*](wmformat-glossary.md) Zeichenfolgen, die dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-106">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type defines the categories for DRM [*license*](wmformat-glossary.md) strings that are displayed to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c3ca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c3ca-107">Syntax</span></span>


```C++
typedef enum DRM_LICENSE_STATE_CATEGORY { 
  WM_DRM_LICENSE_STATE_NORIGHT                    = 0,
  WM_DRM_LICENSE_STATE_UNLIM,
  WM_DRM_LICENSE_STATE_COUNT,
  WM_DRM_LICENSE_STATE_FROM,
  WM_DRM_LICENSE_STATE_UNTIL,
  WM_DRM_LICENSE_STATE_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM,
  WM_DRM_LICENSE_STATE_COUNT_UNTIL,
  WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL,
  WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE
} ;
```



## <a name="constants"></a><span data-ttu-id="2c3ca-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2c3ca-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2c3ca-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM- \_ Lizenz \_ Status " \_ noright"**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-109"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-110">Gibt an, dass die Zeichenfolge die Form "Wiedergabe nicht zulässig" hat.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-110">Indicates the string will take the form "Playback not permitted."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Unlim**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-111"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-112">Gibt an, dass die Zeichenfolge in der Form "Wiedergabe unbegrenzt" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-112">Indicates the string will take the form "Playback unlimited."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-113"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-114">Gibt an, dass die Zeichenfolge das Format "Wiedergabe gültig fünfmal" annimmt.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-114">Indicates the string will take the form "Playback valid 5 times."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ von**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-115"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-116">Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig aus 7/12/00" hat.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-116">Indicates the string will take the form "Playback valid from 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ bis**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-117"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-118">Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig bis 7/12/00" hat.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-118">Indicates the string will take the form "Playback valid until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-119"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-120">Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig von 5/12 bis 9/12" hat.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-120">Indicates the string will take the form "Playback valid from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_Anzahl von WM-DRM- \_ Lizenz Zuständen \_ \_ \_ aus**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-121"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-122">Gibt an, dass die Zeichenfolge das Format "Wiedergabe gültig 5-Mal von 5/12 bis 9/12" annimmt.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-122">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**Anzahl der WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-123"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-124">Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig 5 Mal bis 7/12/00" hat.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-124">Indicates the string will take the form "Playback valid 5 times until 7/12/00."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-125"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-126">Gibt an, dass die Zeichenfolge das Format "Wiedergabe gültig 5-Mal von 5/12 bis 9/12" annimmt.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-126">Indicates the string will take the form "Playback valid 5 times from 5/12 to 9/12."</span></span>

</dd> <dt>

<span data-ttu-id="2c3ca-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**Ablaufdatum des WM- \_ DRM- \_ Lizenz \_ Zustands \_ nach dem \_ \_ firdieren**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-127"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="2c3ca-128">Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig für 24 Stunden nach der ersten Verwendung" hat.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-128">Indicates the string will take the form "Playback valid for 24 hours from first use."</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c3ca-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c3ca-129">Remarks</span></span>

<span data-ttu-id="2c3ca-130">Diese Enumeration gibt die Kategorie für jede mögliche Ausgabe Zeichenfolge an, die angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-130">This enumeration indicates the category for each possible output string to be displayed.</span></span> <span data-ttu-id="2c3ca-131">Es ist ein Mitglied der [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drm-license-state-data.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="2c3ca-131">It is a member of the [**DRM\_LICENSE\_STATE\_DATA**](drm-license-state-data.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c3ca-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c3ca-132">Requirements</span></span>



| <span data-ttu-id="2c3ca-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c3ca-133">Requirement</span></span> | <span data-ttu-id="2c3ca-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2c3ca-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3ca-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c3ca-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2c3ca-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c3ca-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2c3ca-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c3ca-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2c3ca-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c3ca-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2c3ca-139">Version</span><span class="sxs-lookup"><span data-stu-id="2c3ca-139">Version</span></span><br/>                  | <span data-ttu-id="2c3ca-140">SDK für Windows Media-Format 7 oder höhere Versionen des SDKs</span><span class="sxs-lookup"><span data-stu-id="2c3ca-140">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="2c3ca-141">Header</span><span class="sxs-lookup"><span data-stu-id="2c3ca-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c3ca-142"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c3ca-142"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c3ca-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c3ca-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c3ca-144">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="2c3ca-144">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





