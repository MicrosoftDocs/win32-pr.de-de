---
title: EN_DROPFILES Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer versucht, Dateien im Steuerelement abzulegen. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung, wenn er die WM- \_ dropfiles-Nachricht empfängt.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- Windows-Steuerelemente für EN_DROPFILES Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475393"
---
# <a name="en_dropfiles-notification-code"></a>EN \_ dropfiles-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer versucht, Dateien im Steuerelement abzulegen. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung, wenn er die [**WM- \_ dropfiles**](/windows/desktop/shell/wm-dropfiles) -Nachricht empfängt. [**\_**](wm-notify.md)


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**endropfiles**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) -Struktur, die gelöschte Dateiinformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um den Löschvorgang zuzulassen.

Gibt NULL zurück, um den Drop-Vorgang zu ignorieren.

## <a name="remarks"></a>Bemerkungen

Damit ein Rich-Edit-Steuerelement die [**WM- \_ dropfiles**](/windows/desktop/shell/wm-dropfiles) -Meldungen empfängt, muss das übergeordnete Fenster das Steuerelement als Ablage Ziel mithilfe der [**dragaccept-files**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) -Funktion registrieren. Das Steuerelement registriert sich nicht selbst.

Geben Sie zum Empfangen von en \_ dropfiles-Benachrichtigungs Codes [**ENM \_ dropfiles**](rich-edit-control-event-mask-flags.md) in der mit der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) gesendeten Maske an.

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

[**Endropfiles**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

