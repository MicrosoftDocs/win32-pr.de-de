---
title: CBN_SELENDCANCEL Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer ein Element auswählt, aber ein anderes Steuerelement auswählt oder das Dialogfeld schließt. Gibt an, dass die anfängliche Auswahl des Benutzers ignoriert werden soll. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- Windows-Steuerelemente für CBN_SELENDCANCEL Benachrichtigungs
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
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743048"
---
# <a name="cbn_selendcancel-notification-code"></a>CBN \_ selendcancel-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer ein Element auswählt, aber ein anderes Steuerelement auswählt oder das Dialogfeld schließt. Gibt an, dass die anfängliche Auswahl des Benutzers ignoriert werden soll. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner des Kombinations Felds. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Kombinations Feld.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In einem Kombinations Feld mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil wird der CBN- \_ Benachrichtigungs Code "selendcancel" nicht gesendet. Der [CBN- \_ selendok](cbn-selendok.md) -Benachrichtigungs Code wird unmittelbar vor jedem [CBN- \_ selChange](cbn-selchange.md) -Benachrichtigungs Code gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[CBN \_ selChange](cbn-selchange.md)
</dt> <dt>

[CBN- \_ selendok](cbn-selendok.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

