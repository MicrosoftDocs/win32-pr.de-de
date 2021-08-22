---
title: CBN_SELENDCANCEL Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer ein Element auswählt, dann aber ein anderes Steuerelement auswählt oder das Dialogfeld schließt. Sie gibt an, dass die anfängliche Auswahl des Benutzers ignoriert werden soll. Das übergeordnete Fenster des Kombinationsfelds empfängt diesen Benachrichtigungscode über die WM \_ COMMAND-Meldung.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 869168bfb970df9afc6399e6b1ec40e02b9ccdeaa2f2fef93fcbd86c16e9c6d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314400"
---
# <a name="cbn_selendcancel-notification-code"></a>CBN \_ SELENDCANCEL-Benachrichtigungscode

Wird gesendet, wenn der Benutzer ein Element auswählt, dann aber ein anderes Steuerelement auswählt oder das Dialogfeld schließt. Sie gibt an, dass die anfängliche Auswahl des Benutzers ignoriert werden soll. Das übergeordnete Fenster des Kombinationsfelds empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelementbezeichner des Kombinationsfelds. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Kombinationsfeld.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In einem Kombinationsfeld mit dem [**CBS \_ SIMPLE-Format**](combo-box-styles.md) wird der CBN \_ SELENDCANCEL-Benachrichtigungscode nicht gesendet. Der [CBN \_ SELENDOK-Benachrichtigungscode](cbn-selendok.md) wird unmittelbar vor jedem [CBN SELCHANGE-Benachrichtigungscode \_ ](cbn-selchange.md) gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDOK](cbn-selendok.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

