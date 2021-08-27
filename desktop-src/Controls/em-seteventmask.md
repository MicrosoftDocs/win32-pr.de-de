---
title: EM_SETEVENTMASK (Richedit.h)
description: Legt die Ereignismaske für ein rich edit-Steuerelement fest. Die Ereignismaske gibt an, welche Benachrichtigungscodes das Steuerelement an das übergeordnete Fenster sendet.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244274d969473531bae7c1d124af24a88d6b98d9db8bdbe073d054a3a9e36ac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048500"
---
# <a name="em_seteventmask-message"></a>EM \_ SETEVENTMASK-Meldung

Legt die Ereignismaske für ein rich edit-Steuerelement fest. Die Ereignismaske gibt an, welche Benachrichtigungscodes das Steuerelement an das übergeordnete Fenster sendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue Ereignismaske für das Rich-Edit-Steuerelement. Eine Liste der Ereignismasken finden Sie unter [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die vorherige Ereignismaske zurück.

## <a name="remarks"></a>Hinweise

Die Standardereignismaske (bevor eine festgelegt wird) ist ENM \_ NONE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Rich Edit Control-Ereignismaskenflags**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





