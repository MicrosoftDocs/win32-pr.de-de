---
title: CBN_DROPDOWN Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn das Listenfeld eines Kombinationsfelds sichtbar gemacht wird. Das übergeordnete Fenster des Kombinationsfelds empfängt diesen Benachrichtigungscode über die WM \_ COMMAND-Meldung.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978ac01818f3e9ed7da9f3f1decc7398ab4af32df8f884041bec327640a8014d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438300"
---
# <a name="cbn_dropdown-notification-code"></a>\_CBN-DROPDOWN-Benachrichtigungscode

Wird gesendet, wenn das Listenfeld eines Kombinationsfelds sichtbar gemacht wird. Das übergeordnete Fenster des Kombinationsfelds empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Steuerelementbezeichner des Kombinationsfelds. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Kombinationsfeld.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird nur gesendet, wenn das Kombinationsfeld über das [**DROPDOWN- \_**](combo-box-styles.md) oder [**\_ CBS-DROPDOWNLIST-Format verfügt.**](combo-box-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[CBN \_ CLOSEUP](cbn-closeup.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

