---
title: EN_LOWFIRTF Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Microsoft Rich Edit-Steuerelements, dass ein nicht unterstütztes RTF-Schlüsselwort (Rich Text Format) empfangen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer WM \_ NOTIFY-Nachricht.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffafccf7fc52506ce72c6591ae9d4b5e3f5ee8855788267fbfae98497165e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576320"
---
# <a name="en_lowfirtf-notification-code"></a>EN \_ LOWFIRTF-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Microsoft Rich Edit-Steuerelements, dass ein nicht unterstütztes RTF-Schlüsselwort (Rich Text Format) empfangen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungscode in Form einer [**WM \_ NOTIFY-Nachricht.**](wm-notify.md)


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Die [**ENLOWFIRTF-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungscode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um eine EN \_ LOWFIRTF-Benachrichtigung zu erhalten, geben Sie das ENM \_ LOWFIRTF-Flag in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





