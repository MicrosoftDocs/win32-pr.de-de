---
title: WM_DDE_POKE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Poke-Nachricht an eine DDE-Serveranwendung.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE Nachrichten Datenaustausch
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
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743696"
---
# <a name="wm_dde_poke-message"></a>WM- \_ DDE- \_ Poke-Nachricht

Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Poke** -Nachricht an eine DDE-Serveranwendung. Ein Client verwendet diese Nachricht, um den Server aufzufordern, ein nicht angefordertes Datenelement zu akzeptieren. Der Server antwortet mit einer [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung, die angibt, ob das Datenelement akzeptiert wurde.

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client Fenster, das die Meldung bereitstellen soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort ist ein Handle für ein globales Speicher Objekt, das eine [**DDEPoke**](/windows/desktop/api/Dde/ns-dde-ddepoke) -Struktur mit den Daten und zusätzlichen Informationen enthält.

Das höchst wertige Wort enthält ein globales Atom, das das Datenelement identifiziert, für das die Daten oder Benachrichtigungen gesendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

### <a name="posting"></a>Veröffentlichen

Die Client Anwendung muss Speicher für das globale Speicher Objekt mithilfe der [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) -Funktion zuweisen. Die Client Anwendung muss das-Objekt löschen, wenn eine der folgenden Bedingungen zutrifft:

-   Die Serveranwendung antwortet mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung.
-   Der **frelease** -Member ist **false**, aber die Serveranwendung antwortet entweder mit einer positiven oder negativen [**WM- \_ DDE \_**](wm-dde-ack.md)-Bestätigung.

Die Client Anwendung muss das Atom mithilfe der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion erstellen.

Die Client Anwendung muss den **WM- \_ DDE \_ Poke** - *LPARAM* -Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.

### <a name="receiving"></a>Empfangen

Die Serveranwendung sollte die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht senden, um positiv oder negativ zu reagieren. Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann der Server entweder das Atom wieder verwenden oder es löschen und ein neues erstellen.

Der Server muss den " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *LPARAM* "-Parameter durch Aufrufen der [**packddelta param**](/windows/desktop/api/Dde/nf-dde-packddelparam) -Funktion oder der [**reuseddelta param**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) -Funktion erstellen oder wieder verwenden.

Um das globale Speicher Objekt freizugeben, sollte der Server die [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion aufruft. Wenn das Datenformat entweder [**CF \_ dspmetafilepict**](clipboard-formats.md) oder **CF \_ MetafilePict** ist, muss der Server außerdem [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) mit dem eingebetteten metadateihandle aufrufen. Diese beiden Formate haben eine zusätzliche Dereferenzierungsebene. Das heißt, eine Anwendung muss das Objekt Sperren, um einen Zeiger auf ein Handle zu erhalten, und dann das Handle sperren, um einen Zeiger auf eine [**MetafilePict**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) -Struktur zu erhalten, und schließlich **DeleteMetaFile** mit dem Handle aus dem **HMF** -Member der **MetafilePict** -Struktur aufrufen.

Um das Objekt freizugeben, sollte der Server die Funktion " [**freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam) " anrufen.

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

[**DDE Poke**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**Freeddelta param**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**Globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**MetafilePict**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
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

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

