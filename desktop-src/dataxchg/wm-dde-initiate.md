---
title: WM_DDE_INITIATE Meldung (DDE. h)
description: Eine dynamischer Datenaustausch (DDE)-Client Anwendung sendet eine \_ WM \_ -DDE-Initiierungs Nachricht, um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs-und Themen Namen antwortet.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE Nachrichten Datenaustausch
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
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391842"
---
# <a name="wm_dde_initiate-message"></a>WM- \_ DDE- \_ Initiierungs Meldung

Eine dynamischer Datenaustausch (DDE)-Client Anwendung sendet eine **WM- \_ DDE- \_ Initiierungs** Nachricht, um eine Konversation mit einer Serveranwendung zu initiieren, die auf die angegebenen Anwendungs-und Themen Namen antwortet. Wenn diese Nachricht empfangen wird, wird Sie von allen Server Anwendungen mit Namen, die der angegebenen Anwendung entsprechen und die das angegebene Thema unterstützen, erwartet. (Weitere Informationen finden Sie in der " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Meldung.)


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client Fenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort enthält ein Atom, das die Anwendung identifiziert, mit der eine Konversation angefordert wird. Der Anwendungsname darf keine Schrägstriche (/) oder umgekehrten Schrägstriche () enthalten \) . Diese Zeichen sind für Netzwerk Implementierungen reserviert. Wenn dieser Parameter **null** ist, wird eine Konversation mit allen Anwendungen angefordert.

Das höchst wertige Wort enthält ein Atom, das das Thema identifiziert, für das eine Konversation angefordert wird. Wenn das Thema **null** ist, werden Konversationen für alle verfügbaren Themen angefordert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn das nieder wertige Wort von *LPARAM* **null** ist, kann jede Serveranwendung Antworten. Wenn das hochwertige Wort *LPARAM* **null** ist, ist jedes Thema gültig. Beim Empfang einer **WM- \_ DDE- \_ Initiierungs** Anforderung, bei der das hochwertige Wort des *LPARAM* -Parameters auf **null** festgelegt ist, muss ein Server eine [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht für jedes der unterstützten Themen senden.

### <a name="sending"></a>Senden

Der Client sendet die Nachricht an alle Fenster der obersten Ebene, indem der erste Parameter von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) auf **HWND- \_ Broadcast** festgelegt wird.

Wenn die Client Anwendung bereits das Fenster Handle des gewünschten Servers abgerufen hat, kann Sie **WM \_ DDE \_ initiieren** direkt an das Server Fenster senden, indem Sie das Fenster Handle des Servers als ersten Parameter von [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)übergibt.

Die Client Anwendung ordnet Atome durch Aufrufen der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zu.

Wenn [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) zurückgibt, muss die Client Anwendung die Atome löschen.

### <a name="receiving"></a>Empfangen

Um die Initiierung einer Konversation abzuschließen, muss die Serveranwendung mit einer oder mehreren [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachrichten Antworten, wobei jede Nachricht für ein separates Thema gilt. Beim Senden der " **WM \_ DDE \_ ACK** "-Nachricht sollte der Server neue Atome erstellen, und die mit **WM \_ DDE \_ initiieren** gesendeten Atome sollten nicht wieder verwendet werden.

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

[**Globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM-DDE-Bestätigung \_ \_**](wm-dde-ack.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

