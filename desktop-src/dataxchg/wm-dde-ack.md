---
title: WM_DDE_ACK Meldung (DDE. h)
description: Die "WM \_ DDE \_ ACK"-Meldung benachrichtigt eine dynamischer Datenaustausch (DDE)-Anwendung über die Bestätigung und Verarbeitung der folgenden Nachrichten WM \_ DDE \_ Poke, WM \_ DDE \_ Execute, WM \_ DDE \_ Data, WM \_ DDE- \_ Empfehlung, WM \_ DDE \_ unempfehlung, WM \_ DDE \_ initiieren oder WM \_ DDE \_ Request (in einigen Fällen). Um diese Nachricht zu veröffentlichen, wenden Sie die PostMessage-Funktion mit den folgenden Parametern an.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040528"
---
# <a name="wm_dde_ack-message"></a>WM-DDE-Bestätigungs \_ \_ Meldung

Die **"WM \_ DDE \_ ACK** "-Nachricht benachrichtigt eine dynamischer Datenaustausch (DDE)-Anwendung über die Bestätigung und Verarbeitung der folgenden Nachrichten: [**WM \_ DDE \_ Poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM DDE- \_ \_ Empfehlung**](wm-dde-advise.md), [**WM \_ DDE \_ unempfehlung**](wm-dde-unadvise.md), [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)oder [**WM DDE- \_ \_ Anforderung**](wm-dde-request.md) (in einigen Fällen).

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Bei der Reaktion auf " [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)" ist dieser Parameter ein Handle für das Server Fenster, das die Nachricht sendet.

Bei der Reaktion auf " [**WM \_ DDE \_ Execute**](wm-dde-execute.md)" ist dieser Parameter ein Handle für das Server Fenster, das die Meldung bereitstellt.

Beim Antworten auf alle anderen Nachrichten ist dieser Parameter ein Handle für das Client-oder Server Fenster, das die Meldung bereitstellt.

</dd> <dt>

*lParam* 
</dt> <dd>

Bei der Reaktion auf " [**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)" enthält das nieder wertige Wort ein Atom, das die antwortende Anwendung identifiziert. Das Haupt Wort enthält ein Atom, das das Thema identifiziert, für das eine Konversation eingerichtet wird.

Bei der Reaktion auf [**WM \_ DDE \_ Execute**](wm-dde-execute.md)gibt das nieder wertige Wort eine [**ddeack**](/windows/desktop/api/Dde/ns-dde-ddeack) -Struktur an, die eine Reihe von Flags enthält, die den Status der Antwort angeben. Das höchst wertige Wort ist ein Handle für ein globales Speicher Objekt, das die Befehls Zeichenfolge enthält, die in der **WM- \_ DDE- \_ Ausführungs** Nachricht empfangen wurde.

Beim Antworten auf alle anderen Nachrichten gibt das nieder wertige Wort eine [**ddeack**](/windows/desktop/api/Dde/ns-dde-ddeack) -Struktur an, die eine Reihe von Flags enthält, die den Status der Antwort angeben. Das höchst wertige Wort enthält ein globales Atom, das den Namen des Datenelements identifiziert, für das die Antwort gesendet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

### <a name="posting"></a>Veröffentlichen

Außer als Antwort auf die " [**WM DDE"- \_ \_ Initiierungs**](wm-dde-initiate.md) Nachricht stellt die Anwendung die " **WM \_ DDE \_ ACK** "-Nachricht durch Aufrufen der [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion und nicht durch Aufrufen der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion zur Anwendung. Bei der Reaktion auf " **WM \_ DDE \_ initiieren**" sendet die Anwendung die " **WM \_ DDE \_ ACK** "-Nachricht, indem **SendMessage** aufgerufen wird. In diesem Fall sollte weder der Anwendungsname Atom noch das Atom-Name-Atom den Wert **null** aufweisen (auch wenn die WM-DDE-Nachricht die Meldung **null** -Atome **\_ \_ initiiert** hat).

Beim Bestätigen einer Nachricht mit einem begleitenden Atom kann die Anwendung, die die WM-DDE-Bestätigung veröffentlicht, entweder das Atom wieder verwenden, das die ursprüngliche Nachricht begleitet hat, oder Sie kann Sie löschen und eine neue erstellen. **\_ \_**

Wenn Sie [**WM \_ DDE \_ Execute**](wm-dde-execute.md)bestätigen, sollte die Anwendung, die die " **WM \_ DDE \_ ACK** "-Bestätigung sendet, das in der ursprünglichen " **WM \_ \_**

Alle zurückgegebenen **WM- \_ DDE \_** -Bestätigungsnachrichten müssen den *LPARAM* -Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.

Wenn eine Anwendung die Beendigung einer Konversation initiiert hat, indem [**WM \_ DDE \_ beendet**](wm-dde-terminate.md) wird und eine Bestätigung erwartet wird, sollte die wartende Anwendung nachfolgende Nachrichten, die von der anderen Anwendung gesendet werden, nicht bestätigen (positiv oder negativ). Die wartende Anwendung sollte alle Atome oder gemeinsam genutzten Speicher Objekte löschen, die in diesen Beteiligten Nachrichten empfangen wurden. Arbeitsspeicher Objekte sollten nicht freigegeben werden, wenn das **frelease** -Flag in den Daten Meldungen [**WM \_ DDE \_ Poke**](wm-dde-poke.md) und [**WM \_ DDE \_**](wm-dde-data.md) auf **false** festgelegt ist.

### <a name="receiving"></a>Empfangen

Die Anwendung, die eine **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, sollte alle der Nachricht begleitenden Atome löschen. Wenn die Anwendung eine **WM- \_ DDE \_** -Bestätigung als Antwort auf eine Nachricht mit einem begleitenden globalen Speicher Objekt empfängt und das-Objekt mit der auf **false** festgelegten **freleaseflags** gesendet wurde, ist die Anwendung für das Löschen des Objekts verantwortlich.

Wenn die Anwendung eine negative **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, die als Antwort auf eine [**WM-DDE-Benachrichtigungs \_ \_**](wm-dde-advise.md) Meldung gepostet wurde, sollte die Anwendung das mit der ursprünglichen **WM \_ DDE \_** -Benachrichtigungs Meldung veröffentlichte globale Speicher Objekt löschen. Wenn die Anwendung eine negative **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, die als Antwort auf eine [**WM-DDE- \_ \_ Daten**](wm-dde-data.md), [**WM \_ DDE \_ Poke**](wm-dde-poke.md)oder [**WM \_ DDE \_ Execute**](wm-dde-execute.md) -Nachricht gepostet wurde, sollte die Anwendung das globale Speicher Objekt löschen, das mit der ursprünglichen **WM DDE- \_ \_ Daten**, **WM \_ DDE \_ Poke** oder **WM \_ DDE \_ Execute** ausgegeben wurde.

Die Anwendung, die eine gepostete **WM- \_ DDE \_** -Bestätigungsnachricht empfängt, muss den *LPARAM* -Parameter mithilfe der [**freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam) -Funktion freigeben.

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

[**DDE ACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**Freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md)
</dt> <dt>

[**WM- \_ DDE- \_ Daten**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ Ausführen**](wm-dde-execute.md)
</dt> <dt>

[**WM \_ DDE \_ initiieren**](wm-dde-initiate.md)
</dt> <dt>

[**WM \_ DDE \_ Poke**](wm-dde-poke.md)
</dt> <dt>

[**WM- \_ DDE- \_ Anforderung**](wm-dde-request.md)
</dt> <dt>

[**WM- \_ DDE \_ Beenden**](wm-dde-terminate.md)
</dt> <dt>

[**WM \_ DDE \_ nicht Empfehlung**](wm-dde-unadvise.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

