---
title: EN_STOPNOUNDO Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich Edit-Steuerelements, dass eine Aktion aufgetreten ist, für die das Steuerelement nicht genügend Arbeitsspeicher zuweisen kann, um den Rückgängigzustand beizubehalten. Ein Rich-Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer WM \_ NOTIFY-Nachricht.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2bd22161f215e9544db08f845eb144fe94ec083b8a887a3db6fc46220d822d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047390"
---
# <a name="en_stopnoundo-notification-code"></a>EN \_ STOPNOUNDO-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich Edit-Steuerelements, dass eine Aktion aufgetreten ist, für die das Steuerelement nicht genügend Arbeitsspeicher zuweisen kann, um den Rückgängigzustand beizubehalten. Ein Rich-Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer [**WM \_ NOTIFY-Nachricht.**](wm-notify.md)


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, um **den** Rückgängig-Vorgang fortzusetzen.

Gibt einen Wert ungleich 0 (null) zurück, um den **Rückgängig-Vorgang** zu beenden.

## <a name="remarks"></a>Hinweise

Das übergeordnete Fenster erhält immer eine [**WM \_ NOTIFY-Meldung**](wm-notify.md) für dieses Ereignis. Es ist keine Benachrichtigungsmaske erforderlich, die mit [**EM \_ SETEVENTMASK**](em-seteventmask.md)gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





