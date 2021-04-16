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
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>DRM_LICENSE_STATE_CATEGORY-Enumeration (drmexternals. h)

Der Enumerationstyp der **DRM- \_ Lizenz \_ Status \_ Kategorie** definiert die Kategorien für DRM- [*Lizenz*](wmformat-glossary.md) Zeichenfolgen, die dem Benutzer angezeigt werden.

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
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM- \_ Lizenz \_ Status " \_ noright"**
</dt> <dd>

Gibt an, dass die Zeichenfolge die Form "Wiedergabe nicht zulässig" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Unlim**
</dt> <dd>

Gibt an, dass die Zeichenfolge in der Form "Wiedergabe unbegrenzt" verwendet wird.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Wiedergabe gültig fünfmal" annimmt.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ von**
</dt> <dd>

Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig aus 7/12/00" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ bis**
</dt> <dd>

Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig bis 7/12/00" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**
</dt> <dd>

Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig von 5/12 bis 9/12" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**\_Anzahl von WM-DRM- \_ Lizenz Zuständen \_ \_ \_ aus**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Wiedergabe gültig 5-Mal von 5/12 bis 9/12" annimmt.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**Anzahl der WM- \_ DRM- \_ Lizenz \_ Status \_ \_ bis**
</dt> <dd>

Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig 5 Mal bis 7/12/00" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Wiedergabe gültig 5-Mal von 5/12 bis 9/12" annimmt.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**Ablaufdatum des WM- \_ DRM- \_ Lizenz \_ Zustands \_ nach dem \_ \_ firdieren**
</dt> <dd>

Gibt an, dass die Zeichenfolge die Form "Wiedergabe gültig für 24 Stunden nach der ersten Verwendung" hat.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration gibt die Kategorie für jede mögliche Ausgabe Zeichenfolge an, die angezeigt werden soll. Es ist ein Mitglied der [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drm-license-state-data.md) Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | SDK für Windows Media-Format 7 oder höhere Versionen des SDKs<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





