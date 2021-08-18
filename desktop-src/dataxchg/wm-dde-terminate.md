---
title: WM_DDE_TERMINATE (Dde.h)
description: Eine dynamische Daten Exchange (DDE)-Anwendung (Client oder Server) sendet eine WM \_ DDE TERMINATE-Nachricht, um eine Konversation zu \_ beenden. Um diese Nachricht zu veröffentlichen, rufen Sie die PostMessage-Funktion mit den folgenden Parametern auf.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE der Exchange
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
ms.openlocfilehash: a98d9b4bf2120cb6daa08b6088a8dd39f8a17b8e28c37a3917936a9c49230487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736267"
---
# <a name="wm_dde_terminate-message"></a>WM \_ DDE \_ TERMINATE-Nachricht

Eine dynamische Daten Exchange (DDE)-Anwendung (Client oder Server) sendet eine **WM \_ DDE \_ TERMINATE-Nachricht,** um eine Konversation zu beenden.

Um diese Nachricht zu veröffentlichen, rufen Sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit den folgenden Parametern auf.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client- oder Serverfenster, in dem die Nachricht angezeigt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

### <a name="posting"></a>Entsendung

Während auf die Bestätigung der Beendigung gewartet wird, sollte die Veröffentlichungsanwendung keine anderen Nachrichten an die empfangende Anwendung senden. Wenn die sendende Anwendung Nachrichten (mit Ausnahme von **WM \_ DDE \_ TERMINATE)** von der empfangenden Anwendung empfängt, sollte sie alle Atome oder freigegebenen Speicherobjekte löschen, die den Nachrichten zugeordnet sind, mit Ausnahme von globalen Speicherobjekten, die [**WM \_ DDE \_ POKE-**](wm-dde-poke.md) oder [**WM \_ DDE \_ DATA-Nachrichten**](wm-dde-data.md) zugeordnet sind, die nicht über den **fRelease-Membersatz** verfügen.

### <a name="receiving"></a>Empfangen

Die Client- oder Serveranwendung sollte antworten, indem sie eine **WM \_ DDE \_ TERMINATE-Nachricht** sendet.

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

