---
title: EN_LOWFIRTF Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Microsoft Rich Edit-Steuer Elements, dass ein nicht unterstütztes RTF-Schlüsselwort (Rich Text Format) empfangen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- Windows-Steuerelemente für EN_LOWFIRTF Benachrichtigungs
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
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518662"
---
# <a name="en_lowfirtf-notification-code"></a>EN \_ lowfirtf-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Microsoft Rich Edit-Steuer Elements, dass ein nicht unterstütztes RTF-Schlüsselwort (Rich Text Format) empfangen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Die Struktur von " [**umlowfirtf**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) ".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungs Code gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um eine en \_ lowfirtf-Benachrichtigung zu erhalten, geben Sie das ENM \_ lowfirtf-Flag in der mit der [**EM \_ SetEventMask**](em-seteventmask.md) -Nachricht gesendeten Maske an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**"Umlowfirtf"**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**WM- \_ Benachrichtigung**](wm-notify.md)
</dt> </dl>

 

 





