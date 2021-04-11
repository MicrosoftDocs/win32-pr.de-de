---
title: EN_STOPNOUNDO Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine Aktion aufgetreten ist, für die das-Steuerelement nicht genügend Arbeitsspeicher zuordnen kann Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- Windows-Steuerelemente für EN_STOPNOUNDO Benachrichtigungs
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
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105548"
---
# <a name="en_stopnoundo-notification-code"></a>EN \_ stopnoundo-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine Aktion aufgetreten ist, für die das-Steuerelement nicht genügend Arbeitsspeicher zuordnen kann Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

NULL zurückgeben, um **den** Rückgängigvorgang fortzusetzen

Gibt einen Wert ungleich 0 zurück, um  den Rückgängigvorgang zu verhindern

## <a name="remarks"></a>Bemerkungen

Das übergeordnete Fenster ruft immer eine [**WM \_**](wm-notify.md) -Benachrichtigungs Meldung für dieses Ereignis ab. es ist keine Benachrichtigungs Maske erforderlich, die mit der "em-Einstellungs [**\_ Maske**](em-seteventmask.md)" gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> </dl>

 

 





