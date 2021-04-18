---
title: DRM_LICENSE_STATE_CATEGORY-Enumeration (wmdrmsdk. h)
description: Der \_ \_ Enumerationstyp der DRM-Lizenzstatus \_ Kategorie gibt den Typ der Lizenz Beschränkung an, der durch eine DRM- \_ Lizenz \_ Zustands \_ Datenstruktur beschrieben wird.
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- DRM_LICENSE_STATE_CATEGORY-Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_CATEGORY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e928a95a71d9636f88bc3c79ac36168072527040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354699"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a><span data-ttu-id="a6927-104">DRM_LICENSE_STATE_CATEGORY-Enumeration (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="a6927-104">DRM_LICENSE_STATE_CATEGORY enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="a6927-105">Der Enumerationstyp der **DRM- \_ Lizenz \_ Status \_ Kategorie** gibt den Typ der Lizenz Beschränkung an, der durch eine [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drmdrm-license-state-data.md) Struktur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a6927-105">The **DRM\_LICENSE\_STATE\_CATEGORY** enumeration type specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6927-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6927-106">Syntax</span></span>


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
} DRM_LICENSE_STATE_CATEGORY;
```



## <a name="constants"></a><span data-ttu-id="a6927-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a6927-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a6927-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM- \_ Lizenz \_ Status " \_ noright"**</span><span class="sxs-lookup"><span data-stu-id="a6927-108"><span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM\_DRM\_LICENSE\_STATE\_NORIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-109">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a6927-109">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Unlim**</span><span class="sxs-lookup"><span data-stu-id="a6927-110"><span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM\_DRM\_LICENSE\_STATE\_UNLIM**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-111">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, ohne Einschränkung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a6927-111">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="a6927-112"><span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-113">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Uhrzeiten.</span><span class="sxs-lookup"><span data-stu-id="a6927-113">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ von**</span><span class="sxs-lookup"><span data-stu-id="a6927-114"><span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM\_DRM\_LICENSE\_STATE\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-115">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, nach einem festgelegten Datum zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a6927-115">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ bis**</span><span class="sxs-lookup"><span data-stu-id="a6927-116"><span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM\_DRM\_LICENSE\_STATE\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-117">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, bis zum festgelegten Datum zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a6927-117">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**</span><span class="sxs-lookup"><span data-stu-id="a6927-118"><span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-119">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zwischen zwei festgelegten Datumsangaben zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a6927-119">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_Anzahl von WM-DRM- \_ Lizenz Zuständen \_ \_ \_ aus**</span><span class="sxs-lookup"><span data-stu-id="a6927-120"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-121">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Uhrzeitangaben nach einem festgelegten Datum.</span><span class="sxs-lookup"><span data-stu-id="a6927-121">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times after a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**Anzahl der WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**</span><span class="sxs-lookup"><span data-stu-id="a6927-122"><span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-123">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Uhrzeitangaben bis zum festgelegten Datum.</span><span class="sxs-lookup"><span data-stu-id="a6927-123">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times until a set date.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis**</span><span class="sxs-lookup"><span data-stu-id="a6927-124"><span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-125">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Zeitpunkten zwischen zwei festgelegten Datumsangaben.</span><span class="sxs-lookup"><span data-stu-id="a6927-125">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed, but only a set number of times between two set dates.</span></span>

</dd> <dt>

<span data-ttu-id="a6927-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**Ablaufdatum des WM- \_ DRM- \_ Lizenz \_ Zustands \_ nach dem \_ \_ firdieren**</span><span class="sxs-lookup"><span data-stu-id="a6927-126"><span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM\_DRM\_LICENSE\_STATE\_EXPIRATION\_AFTER\_FIRSTUSE**</span></span>
</dt> <dd>

<span data-ttu-id="a6927-127">Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, für eine festgelegte Zeitspanne zulässig ist, beginnend mit der ersten Verwendung der Aktion.</span><span class="sxs-lookup"><span data-stu-id="a6927-127">Specifies that the action for which the **DRM\_LICENSE\_STATE\_DATA** was received is allowed for a set amount of time beginning with the first use of the action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6927-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6927-128">Remarks</span></span>

<span data-ttu-id="a6927-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6927-129">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6927-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6927-130">Requirements</span></span>



| <span data-ttu-id="a6927-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6927-131">Requirement</span></span> | <span data-ttu-id="a6927-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a6927-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6927-133">Header</span><span class="sxs-lookup"><span data-stu-id="a6927-133">Header</span></span><br/> | <dl> <span data-ttu-id="a6927-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6927-134"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6927-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6927-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6927-136">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="a6927-136">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





