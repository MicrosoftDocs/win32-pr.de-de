---
title: LBN_SELCHANGE Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass sich die Auswahl in einem Listenfeld aufgrund von Benutzereingaben geändert hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- Windows-Steuerelemente für LBN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741569"
---
# <a name="lbn_selchange-notification-code"></a>LBN \_ selChange-Benachrichtigungs Code

Benachrichtigt die Anwendung, dass sich die Auswahl in einem Listenfeld aufgrund von Benutzereingaben geändert hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird nur von einem Listenfeld gesendet, das über den [**lbs- \_ Benachrichtigungs**](list-box-styles.md) Stil verfügt.

Dieser Benachrichtigungs Code wird nicht gesendet, wenn die Auswahl durch die Nachricht [**lb \_ SetSel**](lb-setsel.md), [**lb \_ setcurrsel**](lb-setcursel.md), [**lb \_ SelectString**](lb-selectstring.md), [**lb \_ selitemrange**](lb-selitemrange.md) oder [**lb \_ selitemrangeex**](lb-selitemrangeex.md) geändert wird.

Bei einem Listenfeld mit Mehrfachauswahl wird der LBN \_ selChange-Benachrichtigungs Code immer dann gesendet, wenn der Benutzer eine Pfeiltaste drückt, auch wenn sich die Auswahl nicht ändert.

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

[**LB- \_ setcurrsel**](lb-setcursel.md)
</dt> <dt>

[LBN- \_ dblclk](lbn-dblclk.md)
</dt> <dt>

[LBN \_ selcancel](lbn-selcancel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

