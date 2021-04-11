---
title: EN_CLIPFORMAT Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass ein einfügen mit einem bestimmten Zwischenablage Format stattgefunden hat. Diese Benachrichtigung wird von einem fensterlosen Bearbeitungs Steuerelement mithilfe der itexthost txnotify-Methode gesendet.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- Windows-Steuerelemente für EN_CLIPFORMAT Benachrichtigungs
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
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949704"
---
# <a name="en_clipformat-notification-code"></a>\_Benachrichtigungs Code für en clipFormat

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass ein einfügen mit einem bestimmten Zwischenablage Format stattgefunden hat. Diese Benachrichtigung wird von einem fensterlosen Bearbeitungs Steuerelement mithilfe der [**itexthost:: txnotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) -Methode gesendet.


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Fenster-ID, die durch Aufrufen der [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) -Funktion mit dem GWL-ID-Wert abgerufen wird \_ .

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**ClipboardFormat**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) -Struktur, die Informationen über das Zwischenablage Format enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Um \_ die Benachrichtigungs Codes von "de clipFormat" zu erhalten, geben Sie " [**ENM \_ clipFormat**](rich-edit-control-event-mask-flags.md) " in der Maske an, die mit der Nachricht " [**EM \_**](em-seteventmask.md) -Nachricht

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ClipboardFormat**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

