---
title: WM_DDE_DATA Meldung (DDE. h)
description: Eine DDE-Serveranwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Daten Nachricht an eine DDE-Client Anwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu benachrichtigen.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338535"
---
# <a name="wm_dde_data-message"></a>WM \_ DDE- \_ Daten Meldung

Eine DDE-Serveranwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Daten** Nachricht an eine DDE-Client Anwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu benachrichtigen.

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Server Fenster, das die Meldung bereitstellen soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort ist ein Handle für ein globales Speicher Objekt, das eine [**ddedata**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur mit den Daten und zusätzlichen Informationen enthält. Das Handle sollte auf **null** festgelegt werden, wenn der Server den Client darüber benachrichtigt, dass sich der Datenelement Wert während eines warm Daten Links geändert hat. Ein warmer Link wird vom Client erstellt, der eine [**WM- \_ DDE \_**](wm-dde-advise.md) -Benachrichtigungs Meldung mit dem festgelegten " **f"-** Bit sendet.

Das höchst wertige Wort enthält ein Atom, das das Datenelement identifiziert, für das die Daten oder Benachrichtigungen gesendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

### <a name="posting"></a>Veröffentlichen

Die Serveranwendung ordnet das globale Speicher Objekt mithilfe der [**globalbelegungsfunktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zu. Das Atom wird mithilfe der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zugewiesen.

Der Server muss den *LPARAM* -Parameter der **WM-DDE- \_ \_ Daten** durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.

Wenn die empfangende (Client-) Anwendung mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung antwortet, muss die Posting (Server)-Anwendung das globale Speicher Objekt löschen. andernfalls muss der Client das Objekt löschen, nachdem der Inhalt durch Aufrufen der [**unpackddelta param**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) -Funktion extrahiert wurde.

Wenn die Serveranwendung den **frelease** -Member der [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur auf **false** festlegt, ist der Server dafür verantwortlich, das Objekt zu löschen, wenn eine positive oder negative Bestätigung empfangen wird.

Die Serveranwendung sollte nicht sowohl die **fakkreq** -als auch die **frelease** -Member der [**DDE Data**](/windows/desktop/api/Dde/ns-dde-ddedata) -Struktur auf **false** festlegen. Wenn beide Member auf **false** festgelegt sind, kann der Server nicht bestimmen, wann das Objekt gelöscht werden soll.

### <a name="receiving"></a>Empfangen

Wenn " **fakkreq** " den Wert " **true**" hat, sollte die Client Anwendung die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht bereitstellen, um positiv oder negativ Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann der Client entweder das Atom wieder verwenden oder es löschen und ein neues erstellen.

Der Client muss den Parameter " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *LPARAM* " durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.

Wenn " **fakkreq** " den Wert " **false**" hat, sollte die Client Anwendung das Atom löschen.

Wenn die Bereitstellung des globalen Speicher Objekts durch die Anwendungs Bereitstellung als **null** festgelegt wurde, kann die empfangende Anwendung den Server zum Senden der Daten anfordern, indem eine [**WM-DDE- \_ \_ Anforderungs**](wm-dde-request.md) Nachricht

Nachdem eine **WM- \_ DDE- \_ Daten** Nachricht verarbeitet wurde, in der das globale Speicher Objekt nicht **null** ist, muss der Client das Objekt freigeben, es sei denn, eine der folgenden Bedingungen ist erfüllt:

-   Der **frelease** -Member ist **false**.
-   Der **frelease** -Member ist **true**, aber die Client Anwendung antwortet mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht.

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

[**DDE-Daten**](/windows/desktop/api/Dde/ns-dde-ddedata)
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

[**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE \_ Poke**](wm-dde-poke.md)
</dt> <dt>

[**WM- \_ DDE- \_ Anforderung**](wm-dde-request.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

