---
title: Stiftmaske
description: Werte, die im penMask-Feld der -Struktur POINTER_PEN_INFO werden können.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f8b44787dd1039bd3ffd3fa9afef76a527e2143cfe52bdcfa7676c15efa51342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666115"
---
# <a name="pen-mask"></a>Stiftmaske

Werte, die im **penMask-Feld** der -Struktur POINTER_PEN_INFO [**werden**](/previous-versions/windows/desktop/api) können.

<dl> <dt>

<span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Standard. Keines der optionalen Felder ist gültig.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



**Der** Druck der [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) ist gültig.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



**Die** Drehung [**der POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) ist gültig.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X** 
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



**ist ein** [**gültiger POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) der -Struktur.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



**der -Struktur** [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) gültig.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Konstanten](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





