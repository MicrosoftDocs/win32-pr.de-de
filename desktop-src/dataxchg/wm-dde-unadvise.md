---
title: WM_DDE_UNADVISE Meldung (Dde.h)
description: Eine dynamische Daten Exchange-Clientanwendung (DDE) sendet eine WM \_ DDE \_ UNADVISE-Nachricht, um eine DDE-Serveranwendung darüber zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablageformat für das Element nicht mehr aktualisiert werden soll.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE Nachricht Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bbd0ac8e056cc43be764e745f824b50fc90b3cb2f0c50c9061d111fb3bc178d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915104"
---
# <a name="wm_dde_unadvise-message"></a>WM \_ DDE \_ UNADVISE-Nachricht

Eine dynamische Daten Exchange-Clientanwendung (DDE) sendet eine **WM \_ DDE \_ UNADVISE-Nachricht,** um eine DDE-Serveranwendung darüber zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablageformat für das Element nicht mehr aktualisiert werden soll. Dadurch wird der Warm- oder Hot-Datenlink für das angegebene Element beendet.

Um diese Nachricht zu veröffentlichen, rufen Sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit den folgenden Parametern auf.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Clientfenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt das Zwischenablageformat des Elements an, für das die Updateanforderung zurückgesetzt wird. Wenn dies **NULL** ist, müssen alle aktiven [**WM \_ DDE \_ ADVISE-Konversationen**](wm-dde-advise.md) für das Element beendet werden.

Das Wort in hoher Reihenfolge enthält ein globales Atom, das das Element identifiziert, für das die Updateanforderung zurückgesetzt wird. Wenn dies **NULL** ist, müssen alle aktiven [**WM \_ DDE \_ ADVISE-Links,**](wm-dde-advise.md) die der Konversation zugeordnet sind, beendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Clientanwendung ordnet das Wort *lParam* in hoher Reihenfolge zu, indem die [**GlobalAddAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) aufgerufen wird.

Die Serveranwendung sendet die [**WM \_ \_ DDE-ACK-Nachricht,**](wm-dde-ack.md) um positiv oder negativ zu reagieren. Beim Posten von **WM \_ DDE \_ ACK** kann der Server entweder das Atom wiederverwenden oder das Atom löschen und ein neues erstellen.

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

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

