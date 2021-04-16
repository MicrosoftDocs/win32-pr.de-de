---
title: WM_RENDERALLFORMATS Meldung (Winuser. h)
description: Wird an den Besitzer der Zwischenablage gesendet, bevor er zerstört wird, wenn der Besitzer der Zwischenablage ein oder mehrere Zwischenablage Formate verzögert rendert.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd3ce1fabdea4cdcae93b5243b89c53def0afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518554"
---
# <a name="wm_renderallformats-message"></a>WM \_ renderallformats-Meldung

Wird an den Besitzer der Zwischenablage gesendet, bevor er zerstört wird, wenn der Besitzer der Zwischenablage ein oder mehrere Zwischenablage Formate verzögert rendert. Damit der Inhalt der Zwischenablage anderen Anwendungen zur Verfügung steht, muss der Besitzer der Zwischenablage Daten in allen Formaten Renderingformate renderingfähig sein und die Daten in der Zwischenablage platzieren, indem die [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) -Funktion aufgerufen wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Bei der Reaktion auf eine **WM- \_ renderallformats** -Nachricht muss die Anwendung die [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) -Funktion aufrufen und dann überprüfen, ob Sie noch der Besitzer der Zwischenablage ist, indem Sie die [**getclipboardowner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) -Funktion aufruft, bevor [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)aufgerufen wird.

Die Anwendung muss überprüfen, ob Sie nach dem Öffnen der Zwischenablage immer noch der Besitzer der Zwischenablage ist, da nach dem Empfang der **WM- \_ renderallformats** -Nachricht, aber vor dem Öffnen der Zwischenablage eine andere Anwendung den Besitz der Zwischenablage geöffnet und übernommen hat und die Daten dieser Anwendung nicht überschrieben werden sollen.

In den meisten Fällen sollte die Anwendung die [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) -Funktion vor dem Aufruf von [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)nicht aufrufen, da dadurch die Zwischenablage Formate gelöscht werden, die von der Anwendung bereits gerendert wurden.

Wenn die Anwendung zurückgegeben wird, entfernt das System alle nicht gerenderten Formate aus der Liste der verfügbaren Zwischenablage Formate. Weitere Informationen zum verzögerten Rendering finden Sie unter [Verzögertes Rendering](clipboard-operations.md#delayed-rendering).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM- \_ Renderformat**](wm-renderformat.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

