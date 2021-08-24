---
title: WM_NEXTDLGCTL (Winuser.h)
description: Wird an eine Dialogfeldprozedur gesendet, um den Tastaturfokus auf ein anderes Steuerelement im Dialogfeld zu setzen.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL-Dialogfelder
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a14de889e614aaba28757716326bcd1cf843aed64fe2dc58ca86430d65db628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606220"
---
# <a name="wm_nextdlgctl-message"></a>WM \_ NEXTDLGCTL-Meldung

Wird an eine Dialogfeldprozedur gesendet, um den Tastaturfokus auf ein anderes Steuerelement im Dialogfeld zu setzen.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wenn *lParam* **true ist,** identifiziert dieser Parameter das Steuerelement, das den Fokus erhält. Wenn *lParam* **FALSE ist, gibt** dieser Parameter an, ob das nächste oder vorherige Steuerelement mit dem **WS \_ TABSTOP-Stil** den Fokus erhält. Wenn *wParam* 0 (null) ist, erhält das nächste Steuerelement den Fokus. Andernfalls erhält das vorherige Steuerelement mit **dem WS \_ TABSTOP-Format** den Fokus.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt an, wie das System *wParam verwendet.* Wenn das niedrig geordnete Wort **TRUE ist,** *ist wParam* ein Handle, das dem Steuerelement zugeordnet ist, das den Fokus erhält. *andernfalls ist wParam* ein Flag, das angibt, ob das nächste oder vorherige Steuerelement mit dem **WS \_ TABSTOP-Stil** den Fokus erhält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Diese Meldung führt zusätzliche Dialogfeldverwaltungsvorgänge aus, die über die von der [**SetFocus-Funktion**](/windows/desktop/api/winuser/nf-winuser-setfocus) **WM \_ NEXTDLGCTL** ausgeführten Vorgänge hinausgehen, aktualisiert den Standard-Pushbuttonrahmen, legt den Standardsteuersteuerzeichner fest und wählt automatisch den Text eines Bearbeitungssteuerfelds aus (wenn das Zielfenster ein Bearbeitungssteuerfeld ist).

Verwenden Sie die [**SendMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-sendmessage) nicht, um eine **WM \_ NEXTDLGCTL-Nachricht** zu senden, wenn Ihre Anwendung gleichzeitig andere Nachrichten verarbeiten wird, die den Fokus festlegen. Verwenden Sie [**stattdessen die PostMessage-Funktion.**](/windows/desktop/api/winuser/nf-winuser-postmessagea)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> </dl>

 

