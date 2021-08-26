---
title: EN_IMECHANGE Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuerelements, dass sich der IME-Konvertierungsstatus geändert hat.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: e4974c4126606b8ed95ffa645778469b6fc897488533b81498347de1c1995e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047680"
---
# <a name="en_imechange-notification-code"></a>EN \_ IMECHANGE-Benachrichtigungscode

Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuerelements, dass sich der IME-Konvertierungsstatus geändert hat. Dieser Benachrichtigungscode ist *nur für* sprachasiatische Versionen des Betriebssystems verfügbar. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) gesendet.


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Bezeichner des Rich-Edit-Steuerelements. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Rich-Edit-Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungscode gibt 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Um EN \_ IMECHANGE-Benachrichtigungscodes zu erhalten, geben Sie [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht gesendet**](em-seteventmask.md) wird.

> [!Note]  
> Dieser Benachrichtigungscode wird nur in der asiatischen Version von Rich Edit 1.0 unterstützt. Sie wird in späteren Versionen nicht unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

