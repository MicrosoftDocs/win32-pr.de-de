---
title: DRM_LICENSE_STATE_CATEGORY -Enumeration (Wmdrmsdk.h)
description: Der DRM LICENSE STATE CATEGORY-Enumerationstyp gibt den Typ der Lizenzeinschränkung an, der von einer \_ \_ \_ DRM \_ LICENSE STATE \_ \_ DATA-Struktur beschrieben wird.
ms.assetid: 51258be9-2f4d-4f25-97f7-2cac6c155ade
keywords:
- DRM_LICENSE_STATE_CATEGORY enumeration windows Media Format
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
ms.openlocfilehash: 43b8724526142236b70faade68bf7d3ca358eb3f3810cae73f58adde17f25a0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591570"
---
# <a name="drm_license_state_category-enumeration-wmdrmsdkh"></a>DRM_LICENSE_STATE_CATEGORY -Enumeration (Wmdrmsdk.h)

Der **DRM \_ LICENSE STATE \_ CATEGORY-Enumerationstyp \_** gibt den Typ der Lizenzeinschränkung an, der von einer [**DRM LICENSE STATE \_ \_ \_ DATA-Struktur beschrieben**](drmdrm-license-state-data.md) wird.

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

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ NORIGHT**
</dt> <dd>

Gibt an, dass die Aktion, für die **die \_ DRM-LIZENZZUSTANDSDATEN \_ \_** empfangen wurden, nicht zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ UNLIM**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE DRM \_ LICENSE STATE \_ \_ DATA** empfangen wurde, ohne Einschränkung zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ COUNT**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE DRM \_ LICENSE STATE \_ \_ DATA** empfangen wurde, zulässig ist, jedoch nur eine bestimmte Anzahl von Malen.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ FROM**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE \_ DRM-LIZENZZUSTANDSDATEN \_ \_** empfangen wurden, nach einem festgelegten Datum zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM \_ \_ DRM-LIZENZSTATUS \_ \_ BIS**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE \_ DRM-LIZENZZUSTANDSDATEN \_ \_** empfangen wurden, bis zu einem festgelegten Datum zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM \_ \_ DRM-LIZENZSTATUS \_ \_ VON \_ BIS**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE \_ DRM-LIZENZZUSTANDSDATEN \_ \_** empfangen wurden, zwischen zwei festgelegten Datumsangaben zulässig ist.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ COUNT \_ FROM**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE \_ DRM-LIZENZZUSTANDSDATEN \_ \_** empfangen wurden, zulässig ist, aber nur eine bestimmte Anzahl von Malen nach einem festgelegten Datum.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**WM \_ \_ DRM-LIZENZSTATUSANZAHL \_ \_ \_ BIS**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE DRM \_ LICENSE STATE \_ \_ DATA** empfangen wurde, zulässig ist, jedoch nur eine bestimmte Anzahl von Malen bis zu einem festgelegten Datum.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM \_ \_ DRM-LIZENZSTATUSANZAHL \_ \_ VON \_ \_ BIS**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE \_ DRM-LIZENZZUSTANDSDATEN \_ \_** empfangen wurden, zulässig ist, aber nur eine bestimmte Anzahl von Malen zwischen zwei festgelegten Datumsangaben.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**WM \_ \_ DRM-LIZENZSTATUSABLAUF \_ \_ NACH \_ \_ FIRSTUSE**
</dt> <dd>

Gibt an, dass die Aktion, für die **DIE \_ DRM-LIZENZZUSTANDSDATEN \_ \_** empfangen wurden, ab der ersten Verwendung der Aktion für einen festgelegten Zeitraum zulässig ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





