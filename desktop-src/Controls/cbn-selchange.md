---
title: CBN_SELCHANGE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer die aktuelle Auswahl im Listenfeld eines Kombinations Felds ändert.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- Windows-Steuerelemente für CBN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957190"
---
# <a name="cbn_selchange-notification-code"></a>CBN- \_ selChange-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer die aktuelle Auswahl im Listenfeld eines Kombinations Felds ändert. Der Benutzer kann die Auswahl ändern, indem er im Listenfeld oder mithilfe der Pfeiltasten klickt. Das übergeordnete Fenster des Kombinations Felds empfängt diesen Benachrichtigungs Code in Form einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
CBN_SELCHANGE

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

Um den Index der aktuellen Auswahl zu erhalten, senden Sie die [**CB \_ getcurrsel**](cb-getcursel.md) -Nachricht an das-Steuerelement.

Der CBN \_ selChange-Benachrichtigungs Code wird nicht gesendet, wenn die aktuelle Auswahl mithilfe der [**CB- \_ setcurrsel**](cb-setcursel.md) -Nachricht festgelegt wird.

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

[CBN- \_ Schließung](cbn-closeup.md)
</dt> <dt>

[CBN- \_ dblclk](cbn-dblclk.md)
</dt> <dt>

[**CB \_ getcurrsel**](cb-getcursel.md)
</dt> <dt>

[**CB \_ setcurrsel**](cb-setcursel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

