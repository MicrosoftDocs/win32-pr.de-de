---
title: EN_CLIPFORMAT Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass ein Einfügen mit einem bestimmten Zwischenablageformat erfolgt ist. Ein fensterloses Rich-Edit-Steuerelement sendet diese Benachrichtigung mithilfe der ITextHost-TxNotify-Methode.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4ad87f1c05ac9f5461da8a4ee1d26295be0ae1baafd8991801efc0d90197a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437040"
---
# <a name="en_clipformat-notification-code"></a>EN \_ CLIPFORMAT-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass ein Einfügen mit einem bestimmten Zwischenablageformat erfolgt ist. Ein fensterloses Rich Edit-Steuerelement sendet diese Benachrichtigung mithilfe der [**ITextHost::TxNotify-Methode.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Fenster-ID, die durch Aufrufen der [**GetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) mit dem GWL-ID-Wert \_ abgerufen wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**CLIPBOARDFORMAT-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) die Informationen zum Zwischenablageformat enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Um EN \_ CLIPFORMAT-Benachrichtigungscodes zu empfangen, geben Sie [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht gesendet**](em-seteventmask.md) wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

