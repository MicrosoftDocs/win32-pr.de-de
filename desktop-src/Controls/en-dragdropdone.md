---
title: EN_DRAGDROPDONE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Drag & Drop-Vorgang abgeschlossen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- Windows-Steuerelemente für EN_DRAGDROPDONE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949465"
---
# <a name="en_dragdropdone-notification-code"></a>EN \_ dragdropdone-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Drag & Drop-Vorgang abgeschlossen wurde. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungs Code gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um einen en \_ dragdropdone-Benachrichtigungs Code zu erhalten, geben Sie das [**ENM \_ dragdropdone**](rich-edit-control-event-mask-flags.md) -Flag in der mit der [**EM \_ SetEventMask**](em-seteventmask.md) -Nachricht gesendeten Maske an.

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

[**EM-- \_ einventmask**](em-seteventmask.md)
</dt> </dl>

 

 





