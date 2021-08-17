---
title: EN_OLEOPFAILED Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass eine Benutzeraktion für ein Component Object Model-Objekt (COM) fehlgeschlagen ist. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0391bfc61ff9350758ac81ff6f54fb1cff61d0dd1ebbcb2b8ef02ada9fe3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436680"
---
# <a name="en_oleopfailed-notification-code"></a>EN \_ OLEOPFAILED-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass eine Benutzeraktion für ein Component Object Model-Objekt (COM) fehlgeschlagen ist. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**ENOLEOPFAILED-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) die Informationen zum Fehler enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungscode gibt 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Das übergeordnete Fenster wird immer eine [**WM \_ NOTIFY-Nachricht**](wm-notify.md) für dieses Ereignis erhalten, es ist keine Benachrichtigungsmaske erforderlich, die mit [**EM \_ SETEVENTMASK gesendet wird.**](em-seteventmask.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





