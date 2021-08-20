---
title: WM_DDE_REQUEST Nachricht (Dde.h)
description: Eine dynamische Daten Exchange-Clientanwendung (DDE) sendet eine WM \_ DDE \_ REQUEST-Nachricht an eine DDE-Serveranwendung, um den Wert eines Datenelements anzufordern. Um diese Nachricht zu veröffentlichen, rufen Sie die PostMessage-Funktion mit den folgenden Parametern auf.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST Exchange der Nachricht
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c58877b15f39d2de907688972905e98007658981bcc57df62655634bafe8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811350"
---
# <a name="wm_dde_request-message"></a>WM \_ DDE \_ REQUEST-Nachricht

Eine dynamische Daten Exchange-Clientanwendung (DDE) sendet eine **WM \_ DDE \_ REQUEST-Nachricht** an eine DDE-Serveranwendung, um den Wert eines Datenelements anzufordern.

Um diese Nachricht zu veröffentlichen, rufen Sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit den folgenden Parametern auf.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Clientfenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Standardformat oder ein registriertes Zwischenablageformat an.

Das Wort mit hoher Ordnung enthält ein Atom, das das vom Server angeforderte Datenelement identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

### <a name="posting"></a>Entsendung

Die Clientanwendung ordnet das Atom zu, indem die [**GlobalAddAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) aufgerufen wird.

### <a name="receiving"></a>Empfangen

Wenn die empfangende (Server-)Anwendung die Anforderung erfüllen kann, antwortet sie mit einer [**WM \_ DDE \_ DATA-Nachricht,**](wm-dde-data.md) die die angeforderten Daten enthält. Andernfalls antwortet er mit einer negativen [**WM \_ \_ DDE-ACK-Nachricht.**](wm-dde-ack.md)

Wenn sie entweder mit einer [**WM \_ DDE \_ DATA-**](wm-dde-data.md) oder [**WM \_ \_ DDE-ACK-Nachricht**](wm-dde-ack.md) antwortet, kann die Serveranwendung entweder das Atom wiederverwenden oder das Atom löschen und eine neue erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Dde.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

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

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

