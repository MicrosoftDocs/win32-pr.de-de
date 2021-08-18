---
title: WM_DDE_ACK (Dde.h)
description: Die WM DDE ACK-Nachricht benachrichtigt eine dynamische Daten Exchange-Anwendung (DDE) über den Empfang und die Verarbeitung der folgenden Nachrichten \_ \_ WM \_ DDE \_ POKE, WM \_ DDE \_ EXECUTE, WM \_ DDE \_ DATA, WM \_ DDE \_ ADVISE, WM \_ DDE \_ UNADVISE, WM DDE INITIATE oder \_ WM \_ \_ DDE REQUEST (in \_ einigen Fällen). Um diese Nachricht zu veröffentlichen, rufen Sie die PostMessage-Funktion mit den folgenden Parametern auf.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK-Nachricht Data Exchange
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
ms.openlocfilehash: cf1aad39115e1bdb68208a9ccbb0d83eea934ef2ff8c6521a0602e081c7ed811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636240"
---
# <a name="wm_dde_ack-message"></a>WM \_ DDE \_ ACK-Meldung

Die **WM \_ DDE \_ ACK-Nachricht** benachrichtigt eine dynamische Daten Exchange-Anwendung (DDE) über den Empfang und die Verarbeitung der folgenden Nachrichten: [**WM \_ DDE \_ POKE,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) [**WM \_ DDE \_ DATA,**](wm-dde-data.md) [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE,**](wm-dde-unadvise.md) [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)oder [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) (in einigen Fällen).

Um diese Nachricht zu veröffentlichen, rufen Sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit den folgenden Parametern auf.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Bei der Reaktion auf [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)ist dieser Parameter ein Handle für das Serverfenster, das die Nachricht sendet.

Wenn auf [**WM \_ DDE \_ EXECUTE reagiert**](wm-dde-execute.md)wird, ist dieser Parameter ein Handle für das Serverfenster, das die Nachricht sendet.

Bei der Antwort auf alle anderen Nachrichten ist dieser Parameter ein Handle für das Client- oder Serverfenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn auf [**WM \_ DDE \_ INITIATE reagiert**](wm-dde-initiate.md)wird, enthält das Wort der niedrigen Ordnung ein Atom, das die antwortende Anwendung identifiziert. Das obere Wort enthält ein Atom, das das Thema identifiziert, für das eine Konversation hergestellt wird.

Wenn auf [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)reagiert wird, gibt das Wort in niedriger Reihenfolge eine [**DDEACK-Struktur**](/windows/desktop/api/Dde/ns-dde-ddeack) an, die eine Reihe von Flags enthält, die den Status der Antwort angeben. Das obere Wort ist ein Handle für ein globales Speicherobjekt, das die Befehlszeichenfolge enthält, die in der **WM \_ DDE \_ EXECUTE-Nachricht empfangen** wurde.

Beim Antworten auf alle anderen Nachrichten gibt das Wort in niedriger Reihenfolge eine [**DDEACK-Struktur**](/windows/desktop/api/Dde/ns-dde-ddeack) an, die eine Reihe von Flags enthält, die den Status der Antwort angeben. Das obere Wort enthält ein globales Atom, das den Namen des Datenelements identifiziert, für das die Antwort gesendet wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

### <a name="posting"></a>Entsendung

Mit Ausnahme der Antwort auf die [**WM \_ DDE \_ INITIATE-Nachricht**](wm-dde-initiate.md) sendet die Anwendung die **WM \_ DDE \_ ACK-Nachricht** durch Aufrufen der [**PostMessage-Funktion,**](/windows/desktop/api/winuser/nf-winuser-postmessagea) nicht durch Aufrufen der [**SendMessage-Funktion.**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Wenn auf **WM \_ DDE \_ INITIATE reagiert** wird, sendet die Anwendung die WM **\_ DDE \_ ACK-Nachricht,** indem sie **SendMessage aufruft.** In diesem Fall sollte weder das Atom für den Anwendungsnamen noch das Atom des Themennamens **NULL** sein (auch wenn in der **WM \_ DDE \_ INITIATE-Nachricht** **NULL-Atome** angegeben wurden).

Wenn sie eine Nachricht mit einem zugehörigen Atom bestätigen, kann die Anwendung, die **WM \_ DDE \_ ACK** posten, entweder das Atom wiederverwenden, das die ursprüngliche Nachricht begleitet hat, oder sie kann es löschen und ein neues erstellen.

Bei der Bestätigung von [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)sollte die Anwendung, die **WM \_ DDE \_ ACK** veröffentlicht, das globale Speicherobjekt wiederverwenden, das in der ursprünglichen **WM \_ DDE \_ EXECUTE-Nachricht identifiziert** wurde.

Alle veröffentlichten **WM \_ DDE \_ ACK-Nachrichten** müssen den *lParam-Parameter* erstellen oder wiederverwenden, indem sie die [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) oder die [**ReuseDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) aufrufen.

Wenn eine Anwendung die Beendigung einer Konversation durch Veröffentlichen von [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) initiiert hat und auf eine Bestätigung wartet, sollte die wartende Anwendung alle nachfolgenden Nachrichten, die von der anderen Anwendung gesendet werden, nicht bestätigen (positiv oder negativ). Die wartende Anwendung sollte alle Atome oder Shared Memory-Objekte löschen, die in diesen intervenenden Nachrichten empfangen werden. Speicherobjekte sollten nicht frei werden, wenn das **fRelease-Flag** in [**WM \_ DDE \_ POKE-**](wm-dde-poke.md) und [**WM \_ DDE \_ DATA-Meldungen**](wm-dde-data.md) auf **FALSE** festgelegt ist.

### <a name="receiving"></a>Empfangen

Die Anwendung, die eine **WM \_ DDE \_ ACK-Nachricht** empfängt, sollte alle Atome löschen, die die Nachricht begleiten. Wenn die Anwendung eine **WM \_ DDE \_ ACK** als Antwort auf eine Nachricht mit einem zugehörigen globalen Speicherobjekt empfängt und das Objekt mit den **fRelease-Flags** auf **FALSE** festgelegt wurde, ist die Anwendung für das Löschen des Objekts verantwortlich.

Wenn die Anwendung eine negative **WM \_ DDE \_ ACK-Nachricht** empfängt, die als Antwort auf eine [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) gepostet wird, sollte die Anwendung das globale Speicherobjekt löschen, das mit der ursprünglichen **WM \_ DDE \_ ADVISE-Nachricht** gepostet wurde. Wenn die Anwendung eine negative **WM \_ DDE \_ ACK-Nachricht** empfängt, die als Antwort auf eine [**WM \_ DDE \_ DATA-,**](wm-dde-data.md) [**WM \_ DDE \_ POKE-**](wm-dde-poke.md)oder [**WM \_ DDE \_ EXECUTE-Nachricht**](wm-dde-execute.md) gepostet wird, sollte die Anwendung das globale Speicherobjekt löschen, das mit der ursprünglichen **WM \_ DDE \_ DATA-,** **WM \_ DDE \_ POKE-** oder **WM \_ DDE \_ EXECUTE-Nachricht** gepostet wurde.

Die Anwendung, die eine gepostete **WM \_ DDE \_ ACK-Nachricht** empfängt, muss den *lParam-Parameter* mithilfe der [**FreeDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-freeddelparam) frei geben.

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

[**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)
</dt> <dt>

[**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**WM \_ \_ DDE-ANFORDERUNG**](wm-dde-request.md)
</dt> <dt>

[**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md)
</dt> <dt>

[**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

