---
title: DRM_LICENSE_STATE_CATEGORY-Enumeration (Drmexternals.h)
description: Der DRM \_ LICENSE \_ STATE \_ CATEGORY-Enumerationstyp definiert die Kategorien für DRM-Lizenzzeichenfolgen, die dem Benutzer angezeigt werden.
ms.assetid: f5c5aa78-84f9-4ee4-b551-05bf864243ab
keywords:
- DRM_LICENSE_STATE_CATEGORY Enumerationsfenster Medienformat
- Enumerationsfenster Medienformat
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
ms.openlocfilehash: 2bbfd6c566d6c58314416c787110ea77da25416ed73d80ec87fd2d66602d820b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931000"
---
# <a name="drm_license_state_category-enumeration-drmexternalsh"></a>DRM_LICENSE_STATE_CATEGORY-Enumeration (Drmexternals.h)

Der **DRM \_ LICENSE STATE \_ CATEGORY-Enumerationstyp \_** definiert die Kategorien für DRM-Lizenzzeichenfolgen, die dem Benutzer angezeigt werden. [](wmformat-glossary.md)

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

<span id="WM_DRM_LICENSE_STATE_NORIGHT"></span><span id="wm_drm_license_state_noright"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ NORIGHT**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Wiedergabe nicht zulässig" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNLIM"></span><span id="wm_drm_license_state_unlim"></span>**WM \_ DRM \_ LICENSE \_ STATE \_ UNLIM**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Playback unlimited" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT"></span><span id="wm_drm_license_state_count"></span>**ANZAHL DER \_ WM-DRM-LIZENZSTATUS \_ \_ \_**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "5-mal gültig wiedergeben" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM"></span><span id="wm_drm_license_state_from"></span>**WM \_ \_ DRM-LIZENZSTATUS \_ \_ VON**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Playback valid from 7/12/00" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_UNTIL"></span><span id="wm_drm_license_state_until"></span>**WM \_ \_ DRM-LIZENZSTATUS \_ \_ BIS**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Playback valid until 7/12/00" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_FROM_UNTIL"></span><span id="wm_drm_license_state_from_until"></span>**WM \_ \_ DRM-LIZENZSTATUS \_ \_ VON \_ BIS**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Playback valid from 5/12 to 9/12" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM"></span><span id="wm_drm_license_state_count_from"></span>**ANZAHL DER \_ WM-DRM-LIZENZSTATUS \_ \_ \_ \_ VON**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "5 Mal vom 12.05.bis zum 12.9.2012 gültig wiedergeben" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_UNTIL"></span><span id="wm_drm_license_state_count_until"></span>**ANZAHL DER WM \_ \_ DRM-LIZENZSTATUS \_ \_ \_ BIS**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "5 mal bis zum 00.07.2012 gültig wiedergeben" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_COUNT_FROM_UNTIL"></span><span id="wm_drm_license_state_count_from_until"></span>**ANZAHL \_ DER WM-DRM-LIZENZSTATUS \_ VON \_ \_ \_ \_ BIS**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "5 Mal vom 12.05.bis zum 12.9.2012 gültig wiedergeben" hat.

</dd> <dt>

<span id="WM_DRM_LICENSE_STATE_EXPIRATION_AFTER_FIRSTUSE"></span><span id="wm_drm_license_state_expiration_after_firstuse"></span>**ABLAUF DES \_ WM-DRM-LIZENZSTATUS \_ \_ NACH \_ \_ \_ FIRSTUSE**
</dt> <dd>

Gibt an, dass die Zeichenfolge das Format "Wiedergabe gültig für 24 Stunden ab der ersten Verwendung" hat.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Enumeration gibt die Kategorie für jede mögliche Ausgabezeichenfolge an, die angezeigt werden soll. Es ist ein Member der [**DRM \_ LICENSE STATE \_ \_ DATA-Struktur.**](drm-license-state-data.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK oder höhere Versionen des SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





