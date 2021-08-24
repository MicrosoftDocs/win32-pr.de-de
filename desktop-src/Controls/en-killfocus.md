---
title: EN_KILLFOCUS Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn ein Bearbeitungssteuer steuerelement den Tastaturfokus verliert. Das übergeordnete Fenster des Bearbeitungssteuer elements empfängt diesen Benachrichtigungscode über eine WM \_ COMMAND-Meldung.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_KILLFOCUS Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d49aaf72df70737ea9d9e61784918c6da1b6fa90d0b96c294570ae5b657e74ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697370"
---
# <a name="en_killfocus-notification-code"></a>EN \_ KILLFOCUS-Benachrichtigungscode

Wird gesendet, wenn ein Bearbeitungssteuer steuerelement den Tastaturfokus verliert. Das übergeordnete Fenster des Bearbeitungssteuer elements empfängt diesen Benachrichtigungscode über eine [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
EN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Bezeichner des Bearbeitungssteuerzeichens. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Bearbeitungssteuer steuerelement.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das übergeordnete Fenster empfängt immer eine [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) für dieses Ereignis. Es ist keine Benachrichtigungsmaske erforderlich, die mit [**EM \_ SETEVENTMASK gesendet wird.**](em-seteventmask.md)

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EN \_ SETFOCUS**](en-setfocus.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

