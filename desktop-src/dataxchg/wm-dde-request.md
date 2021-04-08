---
title: WM_DDE_REQUEST Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Anforderungs Nachricht an eine DDE-Serveranwendung, um den Wert eines Datenelements anzufordern. Um diese Nachricht zu veröffentlichen, wenden Sie die PostMessage-Funktion mit den folgenden Parametern an.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST Nachrichten Datenaustausch
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
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741088"
---
# <a name="wm_dde_request-message"></a>WM- \_ DDE- \_ Anforderungs Nachricht

Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Anforderungs** Nachricht an eine DDE-Serveranwendung, um den Wert eines Datenelements anzufordern.

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client Fenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt ein Standardmäßiges oder registriertes Zwischenablage Format an.

Das höchst wertige Wort enthält ein Atom, das das vom Server angeforderte Datenelement identifiziert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

### <a name="posting"></a>Veröffentlichen

Die Client Anwendung ordnet das Atom durch Aufrufen der [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion zu.

### <a name="receiving"></a>Empfangen

Wenn die empfangende Anwendung (Server) die Anforderung erfüllen kann, antwortet sie mit einer [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) Nachricht, die die angeforderten Daten enthält. Andernfalls antwortet er mit einer negativen [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung.

Bei der Reaktion entweder der [**WM- \_ DDE- \_ Daten**](wm-dde-data.md) oder der [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsmeldung kann die Serveranwendung entweder das Atom wieder verwenden oder das Atom löschen und ein neues erstellen.

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

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

