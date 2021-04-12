---
title: WM_DDE_ADVISE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet die "WM DDE"- \_ \_ Empfehlung an eine DDE-Serveranwendung, um den Server aufzufordern, ein Update für ein Datenelement anzufordern, wenn das Element geändert wird.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE Nachrichten Datenaustausch
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
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103518"
---
# <a name="wm_dde_advise-message"></a>WM-DDE-Benachrichtigungs \_ \_ Meldung

Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet die " **WM DDE"- \_ \_ Empfehlung** an eine DDE-Serveranwendung, um den Server aufzufordern, ein Update für ein Datenelement anzufordern, wenn das Element geändert wird.

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client Fenster, das die Meldung bereitstellen soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort ist ein Handle für ein globales Speicher Objekt, das eine [**DDE-Empfehlung**](/windows/desktop/api/Dde/ns-dde-ddeadvise) -Struktur enthält, die angibt, wie die Daten gesendet werden sollen.

Das hochwertige Wort enthält ein Atom, das das angeforderte Datenelement identifiziert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn eine Client Anwendung mehr als ein Zwischenablage Format für ein einzelnes Thema und Element unterstützt, kann Sie mehrere **WM-DDE-Anmeldungs \_ \_** Nachrichten für das Thema und das Element bereitstellen und für jede Nachricht ein anderes Zwischenablage Format angeben. Beachten Sie, dass ein Server mehrere Formate nur für heiße Daten Verknüpfungen unterstützen kann, nicht für warm Daten Links.

### <a name="posting"></a>Veröffentlichen

Die Client Anwendung sendet die **Empfehlung "WM \_ DDE- \_ Empfehlung** " durch Aufrufen der [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion und nicht der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion.

Die Client Anwendung ordnet das globale Speicher Objekt mithilfe der [**globalbelegungsfunktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zu. Das Atom wird mithilfe der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zugewiesen.

Die Client Anwendung muss den *LPARAM* -Parameter " **WM \_ DDE- \_ Empfehlung** " durch Aufrufen der Funktion " [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) " oder der Funktion " [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) " erstellen oder wieder verwenden.

Wenn die empfangende Anwendung (Server) mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung antwortet, muss das Objekt von der Posting-Anwendung gelöscht werden.

Das **frelease** -Flag wird nicht in **WM- \_ DDE \_** -Anmeldungs Nachrichten verwendet, aber das Datenfreigabe Verhalten ähnelt dem der [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) und [**WM \_ DDE \_ Poke**](wm-dde-poke.md) -Nachrichten, bei denen **frelease** **true** ist.

### <a name="receiving"></a>Empfangen

Die Serveranwendung sendet die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht, um positiv oder negativ zu reagieren. Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann die Anwendung das Atom wieder verwenden oder löschen und ein neues erstellen. Wenn die **WM- \_ DDE \_** -Bestätigungsnachricht positiv ist, sollte die Anwendung das globale Speicher Objekt löschen, andernfalls sollte die Anwendung das Objekt nicht löschen.

Der Server muss den " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *LPARAM* "-Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.

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

[**DDE-Empfehlung**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[**Freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**Globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**Packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**Reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**Unpackddelta param**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM-DDE-Bestätigung \_ \_**](wm-dde-ack.md)
</dt> <dt>

[**WM- \_ DDE- \_ Daten**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ Poke**](wm-dde-poke.md)
</dt> <dt>

[**WM- \_ DDE- \_ Anforderung**](wm-dde-request.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

