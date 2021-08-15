---
title: CBN_EDITUPDATE Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Bearbeitungssteuerteil eines Kombinationsfelds geänderten Text anzeigen soll.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- CBN_EDITUPDATE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeaf787fd241d9dd87457273bd76c07eebe12fa99f2635643b4a4eaa8eaf4952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314730"
---
# <a name="cbn_editupdate-notification-code"></a>CBN \_ EDITUPDATE-Benachrichtigungscode

Wird gesendet, wenn der Bearbeitungssteuerteil eines Kombinationsfelds geänderten Text anzeigen soll. Dieser Benachrichtigungscode wird gesendet, nachdem das Steuerelement den Text formatiert hat, aber bevor der Text angezeigt wird. Das übergeordnete Fenster des Kombinationsfelds empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
CBN_EDITUPDATE

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

Wenn das Kombinationsfeld das [**FORMAT CBS \_ DROPDOWNLIST auflistet,**](combo-box-styles.md) wird dieser Benachrichtigungscode nicht gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[CBN \_ EDITCHANGE](cbn-editchange.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

