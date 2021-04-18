---
title: CBN_SELENDOK Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer ein Listenelement auswählt oder ein Element auswählt und dann die Liste schließt. Gibt an, dass die Auswahl des Benutzers verarbeitet werden soll. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- Windows-Steuerelemente für CBN_SELENDOK Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337331"
---
# <a name="cbn_selendok-notification-code"></a>CBN- \_ selendok-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer ein Listenelement auswählt oder ein Element auswählt und dann die Liste schließt. Gibt an, dass die Auswahl des Benutzers verarbeitet werden soll. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
CBN_SELENDOK

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

In einem Kombinations Feld mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil wird der CBN- \_ selendok-Benachrichtigungs Code unmittelbar vor jedem [CBN- \_ selChange](cbn-selchange.md) -Benachrichtigungs Code gesendet.

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

[CBN \_ selendcancel](cbn-selendcancel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

