---
title: WM_DDE_TERMINATE Meldung (DDE. h)
description: Eine dynamischer Datenaustausch (DDE)-Anwendung (Client oder Server) sendet eine WM-DDE-Beendigungs \_ \_ Nachricht, um eine Konversation zu beenden. Um diese Nachricht zu veröffentlichen, wenden Sie die PostMessage-Funktion mit den folgenden Parametern an.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103414"
---
# <a name="wm_dde_terminate-message"></a>WM- \_ DDE- \_ Nachricht beenden

Eine dynamischer Datenaustausch (DDE)-Anwendung (Client oder Server) sendet eine **WM-DDE-Beendigungs \_ \_** Nachricht, um eine Konversation zu beenden.

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client-oder Server Fenster, das die Meldung bereitstellen soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

### <a name="posting"></a>Veröffentlichen

Beim Warten auf die Bestätigung der Beendigung sollte die Posting-Anwendung keine weiteren Nachrichten an die empfangende Anwendung senden. Wenn die sendende Anwendung Nachrichten (mit Ausnahme von **WM \_ DDE \_ Beenden**) von der empfangenden Anwendung empfängt, sollten alle Atome oder gemeinsam genutzten Speicher Objekte, die den Nachrichten angehören, gelöscht werden, mit Ausnahme der globalen Speicher Objekte, die mit [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -oder [**WM \_ DDE- \_ Daten**](wm-dde-data.md) Nachrichten verknüpft sind, für die das **frelease** -Element

### <a name="receiving"></a>Empfangen

Die Client-oder Serveranwendung sollte Antworten, indem Sie eine Abbruch Meldung vom Typ " **WM \_ DDE \_** " veröffentlicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>DDE. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM- \_ DDE- \_ Daten**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ Poke**](wm-dde-poke.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

