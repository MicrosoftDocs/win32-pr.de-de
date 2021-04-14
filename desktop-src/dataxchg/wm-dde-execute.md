---
title: WM_DDE_EXECUTE Meldung (DDE. h)
description: Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine WM- \_ DDE- \_ Ausführungs Nachricht an eine DDE-Serveranwendung, um eine Zeichenfolge an den Server zu senden, die als eine Reihe von Befehlen verarbeitet werden soll.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- WM_DDE_EXECUTE Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391975"
---
# <a name="wm_dde_execute-message"></a>WM- \_ DDE- \_ Ausführungs Meldung

Eine DDE-Client Anwendung (dynamischer Datenaustausch) sendet eine **WM- \_ DDE- \_ Ausführungs** Nachricht an eine DDE-Serveranwendung, um eine Zeichenfolge an den Server zu senden, die als eine Reihe von Befehlen verarbeitet werden soll. Die Serveranwendung sendet eine [**WM- \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht als Antwort.

Um diese Nachricht zu veröffentlichen, wenden Sie die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion mit den folgenden Parametern an.


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Client Fenster, das die Meldung bereitstellen soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält ein globales Speicher Objekt, das auf eine ANSI-oder Unicode-Befehls Zeichenfolge verweist, abhängig von den in der Konversation beteiligten Windows-Typen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Befehls Zeichenfolge ist eine auf NULL endenden Zeichenfolge, die aus einer oder mehreren in Klammern eingeschlossenen Opcode-Zeichen folgen besteht \[ \] . Jede Opcode-Zeichenfolge weist die folgende Syntax auf, wobei die *Parameter* Liste optional ist:

*Opcode-Parameter*

Der *Opcode* ist ein beliebiges von der Anwendung definiertes einzelnes Token. Es darf keine Leerzeichen, Kommas, Klammern, eckige Klammern oder Anführungszeichen enthalten.

Die *Parameter* Liste kann beliebige Anwendungs definierte Werte oder Werte enthalten. Mehrere Parameter werden durch Kommas getrennt, und die gesamte Parameterliste wird in Klammern eingeschlossen. Parameter dürfen keine Kommas oder Klammern enthalten, außer innerhalb einer Zeichenfolge in Anführungszeichen. Wenn eine eckige Klammer oder ein Klammer Zeichen in einer Zeichenfolge in Anführungszeichen eingeschlossen werden soll, muss Sie nicht verdoppelt werden, wie es bei den alten Regeln der Fall war.

Folgende Befehls Zeichenfolgen sind gültig:


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



Beachten Sie, dass unter den alten Regeln Klammern und eckige Klammern wie folgt verdoppelt werden mussten:


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



Server sollten in der Lage sein, Befehle in beiden Form zu analysieren.

Unicode-Execute-Zeichen folgen sollten nur verwendet werden, wenn sowohl die Client-als auch die Server Fenster Handles bewirken, dass die [**iswindowunicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) -Funktion **true** zurückgibt

### <a name="posting"></a>Veröffentlichen

Die Client Anwendung ordnet das globale Speicher Objekt zu, indem Sie [](/windows/desktop/api/winbase/nf-winbase-globalalloc) die globalbelegungsfunktion aufrufen.

Bei der Verarbeitung der [**WM \_ DDE \_**](wm-dde-ack.md) -Bestätigungsnachricht, die der Server in Antwort auf eine **WM-DDE- \_ \_ Execute** -Nachricht sendet, muss die Client Anwendung das von der **WM \_ DDE \_ ACK** -Nachricht zurückgegebene Objekt löschen.

### <a name="receiving"></a>Empfangen

Die Serveranwendung sendet die " [**WM \_ DDE \_ ACK**](wm-dde-ack.md) "-Nachricht, um positiv oder negativ zu reagieren. Der Server sollte das globale Speicher Objekt wieder verwenden.

Sofern nicht anders durch ein unter Protokoll angegeben, sollte der Server erst dann die [**WM \_ DDE \_ ACK**](wm-dde-ack.md) -Nachricht veröffentlichen, wenn alle durch die Execute-Befehls Zeichenfolge angegebenen Aktionen abgeschlossen sind. Die einzige Ausnahme von dieser Regel ist, wenn die Zeichenfolge bewirkt, dass der Server die Konversation beendet.

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

[**Iswindowunicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
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

 

