---
title: EN_CORRECTTEXT Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine ordnungsgemäße Syv- \_ Geste aufgetreten ist, sodass das übergeordnete Fenster die Korrektur des Texts abbrechen kann. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- Windows-Steuerelemente für EN_CORRECTTEXT Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102982"
---
# <a name="en_correcttext-notification-code"></a>De \_ correcttext-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass eine ordnungsgemäße Syv- \_ Geste aufgetreten ist, sodass das übergeordnete Fenster die Korrektur des Texts abbrechen kann. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**encorrecttext**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) -Struktur, die die zu korrigierende Auswahl angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, um die Aktion zu ignorieren.

Gibt einen Wert ungleich 0 zurück, um die Aktion zu verarbeiten.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird nur gesendet, wenn die Stift Funktionen verfügbar sind.

Geben Sie zum Empfangen von en- \_ korrettext-Benachrichtigungs Codes [**ENM \_ correcttext**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht gesendet wird.

> [!Note]  
> Der en \_ correcttext-Benachrichtigungs Code wird nur in der Rich Edit-Version 1,0 unterstützt. Sie wird in späteren Versionen der Rich-Edit-Version nicht unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

 

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

[**"Tcorrecttext"**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





