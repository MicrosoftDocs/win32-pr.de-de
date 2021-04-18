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
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>DRM_LICENSE_STATE_CATEGORY-Enumeration (wmdrmsdk. h)

Der Enumerationstyp der **DRM- \_ Lizenz \_ Status \_ Kategorie** gibt den Typ der Lizenz Beschränkung an, der durch eine [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drmdrm-license-state-data.md) Struktur beschrieben wird.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM- \_ Lizenz \_ Status " \_ noright"**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, nicht zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Unlim**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, ohne Einschränkung zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Uhrzeiten.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ von**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, nach einem festgelegten Datum zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ bis**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, bis zum festgelegten Datum zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zwischen zwei festgelegten Datumsangaben zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_Anzahl von WM-DRM- \_ Lizenz Zuständen \_ \_ \_ aus**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Uhrzeitangaben nach einem festgelegten Datum.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**Anzahl der WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Uhrzeitangaben bis zum festgelegten Datum.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, zulässig ist, jedoch nur eine festgelegte Anzahl von Zeitpunkten zwischen zwei festgelegten Datumsangaben.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**Ablaufdatum des WM- \_ DRM- \_ Lizenz \_ Zustands \_ nach dem \_ \_ firdieren**
</dt> <dd>

Gibt an, dass die Aktion, für die die **DRM- \_ Lizenz \_ Zustands \_ Daten** empfangen wurden, für eine festgelegte Zeitspanne zulässig ist, beginnend mit der ersten Verwendung der Aktion.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





