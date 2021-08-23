---
title: EN_DRAGDROPDONE Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass der Drag & Drop-Vorgang abgeschlossen wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: fb498361de04184823ab0d0652cc32adc9cbb1978bd6f303b7b215417f99f552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436870"
---
# <a name="en_dragdropdone-notification-code"></a>EN \_ DRAGDROPDONE-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass der Drag & Drop-Vorgang abgeschlossen wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungscode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um einen EN DRAGDROPDONE-Benachrichtigungscode zu erhalten, geben Sie \_ das [**ENM \_ DRAGDROPDONE-Flag**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht gesendet**](em-seteventmask.md) wird.

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> </dl>

 

 





