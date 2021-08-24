---
title: WM_DDE_ADVISE (Dde.h)
description: Eine dynamische Daten Exchange-Clientanwendung (DDE) sendet die WM DDE ADVISE-Nachricht an eine DDE-Serveranwendung, um den Server auf die Bereitstellung eines Updates für ein Datenelement zu bitten, wenn sich das Element \_ \_ ändert.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE der Exchange
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c651144b4f09cf53f07c0f1860625cab8277e5c8a9532ee864b9ec1b1c927323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636220"
---
# <a name="wm_dde_advise-message"></a>WM \_ DDE \_ ADVISE-Meldung

Eine dynamische Daten Exchange-Clientanwendung (DDE) sendet die **WM \_ DDE \_ ADVISE-Nachricht** an eine DDE-Serveranwendung, um den Server auf die Bereitstellung eines Updates für ein Datenelement zu bitten, wenn sich das Element ändert.

Um diese Nachricht zu veröffentlichen, rufen Sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit den folgenden Parametern auf.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Clientfenster, in dem die Nachricht angezeigt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge ist ein Handle für ein globales Speicherobjekt, das eine [**DDEADVISE-Struktur**](/windows/desktop/api/Dde/ns-dde-ddeadvise) enthält, die angibt, wie die Daten gesendet werden sollen.

Das obere Wort enthält ein Atom, das das angeforderte Datenelement identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn eine Clientanwendung mehr als ein Zwischenablageformat für ein einzelnes Thema und Element unterstützt, kann sie mehrere **WM \_ DDE \_ ADVISE-Nachrichten** für das Thema und Element veröffentlichen und dabei bei jeder Nachricht ein anderes Zwischenablageformat angeben. Beachten Sie, dass ein Server mehrere Formate nur für hot-Datenlinks unterstützen kann, nicht für warme Datenlinks.

### <a name="posting"></a>Entsendung

Die Clientanwendung sendet die **WM \_ DDE \_ ADVISE-Nachricht,** indem sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) aufruft, nicht die [**SendMessage-Funktion.**](/windows/desktop/api/winuser/nf-winuser-sendmessage)

Die Clientanwendung ordnet das globale Speicherobjekt mithilfe der [**GlobalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zu. Sie ordnet das Atom mithilfe der [**GlobalAddAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) zu.

Die Clientanwendung muss den **WM \_ DDE \_ ADVISE** *lParam-Parameter* durch Aufrufen der [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) oder der [**ReuseDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) erstellen oder wiederverwenden.

Wenn die empfangende Anwendung (Serveranwendung) mit einer negativen [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) antwortet, muss die Stellenausschreibungsanwendung das Objekt löschen.

Das **fRelease-Flag** wird nicht in **WM \_ DDE \_ ADVISE-Nachrichten** verwendet, aber das Verhalten der Datenfreiung ähnelt dem Verhalten von [**WM \_ DDE \_ DATA-**](wm-dde-data.md) und [**WM \_ DDE \_ POKE-Nachrichten,**](wm-dde-poke.md) bei denen **fRelease** **TRUE** ist.

### <a name="receiving"></a>Empfangen

Die Serveranwendung sendet die [**WM \_ DDE \_ ACK-Nachricht,**](wm-dde-ack.md) um positiv oder negativ zu reagieren. Bei der **Veröffentlichung von WM \_ DDE \_ ACK** kann die Anwendung das Atom wiederverwenden oder löschen und ein neues erstellen. Wenn die **WM \_ DDE \_ ACK-Meldung** positiv ist, sollte die Anwendung das globale Speicherobjekt löschen. Andernfalls sollte die Anwendung das Objekt nicht löschen.

Der Server muss den [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam-Parameter* erstellen oder wiederverwenden, indem er die [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) oder die [**ReuseDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Dde.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**WM \_ \_ DDE-ANFORDERUNG**](wm-dde-request.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

