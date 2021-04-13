---
title: WM_DDE_UNADVISE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine "WM \_ DDE \_ unempfehlung"-Meldung, um eine DDE Server-Anwendung zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablage Format für das Element nicht mehr aktualisiert werden soll.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478306"
---
# <a name="wm_dde_unadvise-message"></a>WM \_ DDE- \_ Meldung "nicht Empfehlung"

Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine " **WM \_ DDE \_ unempfehlung** "-Meldung, um eine DDE Server-Anwendung zu informieren, dass das angegebene Element oder ein bestimmtes Zwischenablage Format für das Element nicht mehr aktualisiert werden soll. Dadurch wird der Daten Link warm oder Hot für das angegebene Element beendet.

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client Fenster, das die Nachricht sendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt das Zwischenablage Format des Elements an, für das die Aktualisierungs Anforderung zurückgezogen wird. Wenn dieser Wert **null** ist, werden alle aktiven [**WM- \_ DDE \_**](wm-dde-advise.md) -Konversationen für das Element beendet.

Das höchst wertige Wort enthält ein globales Atom, das das Element identifiziert, für das die Aktualisierungs Anforderung zurückgezogen wird. Wenn dieser Wert **null** ist, werden alle aktiven [**WM- \_ DDE \_**](wm-dde-advise.md) -Links, die der Konversation zugeordnet sind, beendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Client Anwendung ordnet das hochwertige Wort *LPARAM* zu, indem die [**globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) -Funktion aufgerufen wird.

Die Serveranwendung sendet die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht, um positiv oder negativ zu reagieren. Beim Veröffentlichen der **WM- \_ DDE \_**-Bestätigung kann der Server entweder das Atom wieder verwenden oder das Atom löschen und ein neues erstellen.

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

[**WM \_ DDE- \_ Empfehlung**](wm-dde-advise.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Informationen zu dynamischer Datenaustausch](about-dynamic-data-exchange.md)
</dt> </dl>

 

