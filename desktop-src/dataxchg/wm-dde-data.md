---
title: WM_DDE_DATA (Dde.h)
description: Eine dynamische Daten Exchange-Serveranwendung (DDE) sendet eine WM DDE DATA-Nachricht an eine DDE-Clientanwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu \_ \_ benachrichtigen.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA der Exchange
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
ms.openlocfilehash: 0200737a9b25a123954498941ad117e5465f58f5313daa8caf90674751355ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736277"
---
# <a name="wm_dde_data-message"></a>WM \_ DDE \_ DATA-Nachricht

Eine dynamische Daten Exchange-Serveranwendung (DDE) sendet eine **WM \_ DDE \_ DATA-Nachricht** an eine DDE-Clientanwendung, um ein Datenelement an den Client zu übergeben oder den Client über die Verfügbarkeit eines Datenelements zu benachrichtigen.

Um diese Nachricht zu veröffentlichen, rufen Sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit den folgenden Parametern auf.


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Serverfenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort der niedrigen Ordnung ist ein Handle für ein globales Speicherobjekt, das eine [**DDEDATA-Struktur**](/windows/desktop/api/Dde/ns-dde-ddedata) mit den Daten und zusätzlichen Informationen enthält. Das Handle sollte auf **NULL** festgelegt werden, wenn der Server den Client benachrichtigt, dass sich der Datenelementwert während eines warmen Datenlinks geändert hat. Ein warmer Link wird vom Client hergestellt, der eine [**WM \_ DDE \_ ADVISE-Nachricht**](wm-dde-advise.md) mit dem **festgelegten fDeferUpd-Bit** sendet.

Das obere Wort enthält ein Atom, das das Datenelement identifiziert, für das die Daten oder Benachrichtigungen gesendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

### <a name="posting"></a>Entsendung

Die Serveranwendung ordnet das globale Speicherobjekt mithilfe der [**GlobalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zu. Sie ordnet das Atom mithilfe der [**GlobalAddAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) zu.

Der Server muss den **WM \_ DDE \_ DATA** *lParam-Parameter* erstellen oder wiederverwenden, indem er die [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) oder die [**ReuseDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) aufruft.

Wenn die empfangende (Client-)Anwendung mit einer negativen [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) antwortet, muss die Anwendung für die Veröffentlichung (Server) das globale Speicherobjekt löschen. Andernfalls muss der Client das Objekt nach dem Extrahieren seines Inhalts löschen, indem die [**UnpackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) aufruft.

Wenn die Serveranwendung den **fRelease-Member** der [**DDEDATA-Struktur**](/windows/desktop/api/Dde/ns-dde-ddedata) auf **FALSE** setzt, ist der Server für das Löschen des Objekts verantwortlich, wenn eine positive oder negative Bestätigung empfangen wird.

Die Serveranwendung sollte nicht sowohl den **fAckReq-** als auch **den fRelease-Member** der [**DDEDATA-Struktur**](/windows/desktop/api/Dde/ns-dde-ddedata) auf **FALSE festlegen.** Wenn beide Member auf **FALSE festgelegt** sind, kann der Server nicht bestimmen, wann das Objekt gelöscht werden soll.

### <a name="receiving"></a>Empfangen

Wenn **fAckReq** **true ist,** sollte die Clientanwendung die [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) veröffentlichen, um positiv oder negativ zu reagieren. Beim Veröffentlichen **von WM \_ DDE \_ ACK** kann der Client das Atom entweder wiederverwenden oder löschen und ein neues erstellen.

Der Client muss den [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam-Parameter* erstellen oder wiederverwenden, indem er die [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) oder die [**ReuseDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) aufruft.

Wenn **fAckReq** **false ist,** sollte die Clientanwendung das Atom löschen.

Wenn die Senden-Anwendung ein globales Speicherobjekt als **NULL** angibt, kann die empfangende Anwendung den Server zum Senden der Daten anfordern, indem sie eine [**WM \_ DDE \_ REQUEST-Nachricht**](wm-dde-request.md) sendet.

Nach der Verarbeitung einer **WM \_ DDE \_ DATA-Nachricht,** in der das globale Speicherobjekt nicht **NULL** ist, sollte der Client das Objekt freigibt, es sei denn, eine der folgenden Bedingungen trifft zu:

-   Der **fRelease-Member** ist **FALSE.**
-   Der **fRelease-Member** ist **TRUE,** aber die Clientanwendung antwortet mit einer negativen [**WM \_ DDE \_ ACK-Nachricht.**](wm-dde-ack.md)

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

[**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**WM \_ \_ DDE-ANFORDERUNG**](wm-dde-request.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

