---
title: EN_IMECHANGE Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass der IME-Konvertierungs Status geändert wurde.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- Windows-Steuerelemente für EN_IMECHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040641"
---
# <a name="en_imechange-notification-code"></a>EN \_ ImeChange-Benachrichtigungs Code

Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuer Elements, dass der IME-Konvertierungs Status geändert wurde. Dieser Benachrichtigungs Code ist *nur* für Versionen des Betriebssystems in der asiatischen Sprache verfügbar. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Rich Edit-Steuer Elements. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Rich Edit-Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungs Code gibt NULL zurück.

## <a name="remarks"></a>Bemerkungen

Um \_ ImeChange-Benachrichtigungs Codes zu erhalten, geben Sie [**ENM \_ ImeChange**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.

> [!Note]  
> Dieser Benachrichtigungs Code wird nur in der asiatischen Version von Rich Edit 1,0 unterstützt. Sie wird in späteren Versionen nicht unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

