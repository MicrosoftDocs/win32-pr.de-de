---
title: EN_CHANGE (Rich Edit)-Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt das Host Fenster eines fensterlosen Bearbeitungs Steuer Elements, dass eine Änderung aufgetreten ist. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- EN_CHANGE (Rich Edit)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949707"
---
# <a name="en_change-rich-edit-notification-code"></a>EN- \_ Änderungs Benachrichtigungs Code (Rich Edit)

Benachrichtigt das Host Fenster eines fensterlosen Bearbeitungs Steuer Elements, dass eine Änderung aufgetreten ist. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**changenotify**](/windows/desktop/api/Textserv/ns-textserv-changenotify) -Struktur, die die vorgenommene Änderung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungs Code gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um \_ Änderungs Benachrichtigungs Codes von en zu erhalten, geben Sie [**ENM- \_ Änderung**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Txnotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





