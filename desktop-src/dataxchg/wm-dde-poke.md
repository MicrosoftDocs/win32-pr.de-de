---
title: WM_DDE_POKE (Dde.h)
description: Eine dynamische Daten Exchange-Clientanwendung (DDE) sendet eine WM \_ DDE \_ POKE-Nachricht an eine DDE-Serveranwendung.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE der Exchange
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1329c6667698a0b633deb2726c47469b515e8fcd78d735a3949e7c8e19a4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736287"
---
# <a name="wm_dde_poke-message"></a>WM \_ DDE \_ POKE-Nachricht

Eine dynamische Daten Exchange -Clientanwendung (DDE) sendet eine **WM \_ DDE \_ POKE-Nachricht** an eine DDE-Serveranwendung. Ein Client verwendet diese Meldung, um den Server anfordert, ein nicht angefordertes Datenelement zu akzeptieren. Es wird erwartet, dass der Server mit einer [**WM \_ DDE \_ ACK-Meldung**](wm-dde-ack.md) antwortet, die angibt, ob er das Datenelement akzeptiert hat.

Um diese Nachricht zu veröffentlichen, rufen Sie die [**PostMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit den folgenden Parametern auf.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Clientfenster, in dem die Nachricht angezeigt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge ist ein Handle für ein globales Speicherobjekt, das eine [**DDEPOKE-Struktur**](/windows/desktop/api/Dde/ns-dde-ddepoke) mit den Daten und zusätzlichen Informationen enthält.

Das obere Wort enthält ein globales Atom, das das Datenelement identifiziert, für das die Daten oder Benachrichtigungen gesendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

### <a name="posting"></a>Entsendung

Die Clientanwendung muss mithilfe der [**GlobalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) Arbeitsspeicher für das globale Speicherobjekt zuordnen. Die Clientanwendung muss das Objekt löschen, wenn eine der folgenden Bedingungen zutrifft:

-   Die Serveranwendung antwortet mit einer negativen [**WM \_ DDE \_ ACK-Meldung.**](wm-dde-ack.md)
-   Der **fRelease-Member** ist **FALSE,** aber die Serveranwendung antwortet entweder mit einer positiven oder negativen [**WM \_ DDE \_ ACK**](wm-dde-ack.md).

Die Clientanwendung muss das Atom mithilfe der [**GlobalAddAtom-Funktion**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) erstellen.

Die Clientanwendung muss den **WM \_ DDE \_ POKE** *lParam-Parameter* durch Aufrufen der [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) oder der [**ReuseDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) erstellen oder wiederverwenden.

### <a name="receiving"></a>Empfangen

Die Serveranwendung sollte die [**WM \_ DDE \_ ACK-Nachricht**](wm-dde-ack.md) veröffentlichen, um positiv oder negativ zu reagieren. Beim Veröffentlichen **von WM \_ DDE \_ ACK** kann der Server entweder das Atom wiederverwenden oder es löschen und ein neues erstellen.

Der Server muss den [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam-Parameter* erstellen oder wiederverwenden, indem er die [**PackDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-packddelparam) oder die [**ReuseDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) aufruft.

Um das globale Speicherobjekt frei zu geben, sollte der Server die [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) aufrufen. Wenn das Datenformat entweder [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) oder **CF \_ METAFILEPICT** ist, muss der Server außerdem [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) mit dem eingebetteten Metadateihand handle aufrufen. Diese beiden Formate verfügen über eine zusätzliche Deskriptionsebene. Das heißt, eine Anwendung muss das -Objekt sperren, um einen Zeiger auf ein Handle zu erhalten, dann dieses Handle sperren, um einen Zeiger auf eine [**METAFILEPICT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) zu erhalten, und schließlich **DeleteMetaFile** mit dem Handle aus dem **hMF-Member** der **METAFILEPICT-Struktur** aufrufen.

Um das Objekt frei zu geben, sollte der Server die [**FreeDDElParam-Funktion**](/windows/desktop/api/Dde/nf-dde-freeddelparam) aufrufen.

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

[**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
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

**Konzeptionellen**
</dt> <dt>

[Informationen dynamische Daten Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

