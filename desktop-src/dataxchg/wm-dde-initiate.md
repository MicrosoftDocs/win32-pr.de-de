---
title: WM_DDE_INITIATE (Dde.h)
description: Eine dynamischer Datenaustausch-Clientanwendung (DDE) sendet eine WM DDE INITIATE-Nachricht, um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs- \_ \_ und Themennamen antwortet.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE von Nachrichtendatenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf65e222c7711d429db44e391d4f03c35997e219
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386728"
---
# <a name="wm_dde_initiate-message"></a>WM \_ DDE \_ INITIATE-Nachricht

Eine dynamischer Datenaustausch-Clientanwendung (DDE) sendet eine **WM \_ DDE \_ INITIATE-Nachricht,** um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs- und Themennamen antwortet. Nach dem Empfang dieser Meldung wird von allen Serveranwendungen mit Namen, die der angegebenen Anwendung und dem angegebenen Thema unterstützen, erwartet, dass sie bestätigt werden. (Weitere Informationen finden Sie in der [**WM \_ DDE \_ ACK-Meldung.)**](wm-dde-ack.md)


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Clientfenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort der niedrigen Ordnung enthält ein Atom, das die Anwendung identifiziert, mit der eine Konversation angefordert wird. Der Anwendungsname darf keine Schrägstriche (/) oder schräge Schrägstriche () \\ enthalten. Diese Zeichen sind für Netzwerkimplementierungen reserviert. Wenn dieser Parameter **NULL ist,** wird eine Konversation mit allen Anwendungen angefordert.

Das obere Wort enthält ein Atom, das das Thema identifiziert, für das eine Konversation angefordert wird. Wenn das Thema NULL **ist,** werden Konversationen für alle verfügbaren Themen angefordert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn das niedrige Wort von *lParam* **NULL ist,** kann jede Serveranwendung antworten. Wenn das obere Wort *von lParam* **NULL ist,** ist jedes Thema gültig. Beim Empfang einer **WM \_ DDE \_ INITIATE-Anforderung,** bei der das obere Wort des *lParam-Parameters* auf **NULL** festgelegt ist, muss ein Server für jedes der unterstützten Themen eine [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) senden.

### <a name="sending"></a>Senden

Der Client überträgt die Nachricht an alle Fenster der obersten Ebene, indem der erste Parameter von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) auf **HWND \_ BROADCAST festgelegt wird.**

Wenn die Clientanwendung bereits das Fensterhand handle des gewünschten Servers abgerufen hat, kann sie **WM \_ DDE \_ INITIATE** direkt an das Serverfenster senden, indem sie das Fensterhand handle des Servers als ersten Parameter von [**SendMessage übergibt.**](/windows/desktop/api/winuser/nf-winuser-sendmessage)

Die Clientanwendung ordnet Atome zu, indem sie die [**GlobalAddAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) aufruft.

Wenn [**SendMessage zurückgegeben**](/windows/desktop/api/winuser/nf-winuser-sendmessage) wird, muss die Clientanwendung die Atome löschen.

### <a name="receiving"></a>Empfangen

Um die Initiierung einer Konversation abschließen zu können, muss die Serveranwendung mit mindestens einer [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) antworten, wobei jede Nachricht für ein separates Thema gilt. Beim Senden **der WM \_ DDE \_ ACK-Nachricht** sollte der Server neue Atome erstellen. Die mit WM DDE INITIATE gesendeten Atome sollten **nicht wiederverwendet \_ \_ werden.**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Dde.h (einschließlich Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

