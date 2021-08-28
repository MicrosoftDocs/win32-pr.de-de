---
title: CBN_SELCHANGE Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer die aktuelle Auswahl im Listenfeld eines Kombinationsfelds ändert.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE Benachrichtigungscode Windows Controls
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
ms.openlocfilehash: f808438f8592acfdede592fab352bbeb0dd7123b5dc41db86eadb6749ae8b4ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968620"
---
# <a name="cbn_selchange-notification-code"></a>CBN \_ SELCHANGE-Benachrichtigungscode

Wird gesendet, wenn der Benutzer die aktuelle Auswahl im Listenfeld eines Kombinationsfelds ändert. Der Benutzer kann die Auswahl ändern, indem er auf das Listenfeld klickt oder die Pfeiltasten verwendet. Das übergeordnete Fenster des Kombinationsfelds empfängt diesen Benachrichtigungscode in Form einer [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
CBN_SELCHANGE

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

Um den Index der aktuellen Auswahl abzurufen, senden Sie die [**CB \_ GETCURSEL-Nachricht**](cb-getcursel.md) an das Steuerelement.

Der CBN \_ SELCHANGE-Benachrichtigungscode wird nicht gesendet, wenn die aktuelle Auswahl mithilfe der [**CB \_ SETCURSEL-Nachricht**](cb-setcursel.md) festgelegt wird.

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

[CBN \_ CLOSEUP](cbn-closeup.md)
</dt> <dt>

[CBN \_ DBLCLK](cbn-dblclk.md)
</dt> <dt>

[**CB \_ GETCURSEL**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

