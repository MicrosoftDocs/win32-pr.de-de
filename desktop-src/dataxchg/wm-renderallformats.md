---
title: WM_RENDERALLFORMATS Meldung (Winuser.h)
description: Wird an den Besitzer der Zwischenablage gesendet, bevor er zerstört wird, wenn der Besitzer der Zwischenablage das Rendern eines oder mehrerer Zwischenablageformate verzögert hat.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS Nachricht Data Exchange
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
ms.openlocfilehash: 77dae9b44cb379ed62c99c601d308fdec500440a9ebad0ffeaffad16ec780dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636060"
---
# <a name="wm_renderallformats-message"></a>WM \_ RENDERALLFORMATS-Meldung

Wird an den Besitzer der Zwischenablage gesendet, bevor er zerstört wird, wenn der Besitzer der Zwischenablage das Rendern eines oder mehrerer Zwischenablageformate verzögert hat. Damit der Inhalt der Zwischenablage für andere Anwendungen verfügbar bleibt, muss der Besitzer der Zwischenablage Daten in allen Formaten rendern, die er generieren kann, und die Daten in der Zwischenablage platzieren, indem er die [**SetClipboardData-Funktion**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) aufruft.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn sie auf eine **WM \_ RENDERALLFORMATS-Nachricht** antwortet, muss die Anwendung die [**OpenClipboard-Funktion**](/windows/win32/api/winuser/nf-winuser-openclipboard) aufrufen und dann überprüfen, ob sie weiterhin der Besitzer der Zwischenablage ist, indem sie die [**GetClipboardOwner-Funktion**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) aufruft, bevor [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)aufgerufen wird.

Die Anwendung muss überprüfen, ob sie nach dem Öffnen der Zwischenablage weiterhin der Besitzer der Zwischenablage ist, da nach dem Empfang der **WM \_ RENDERALLFORMATS-Nachricht,** aber vor dem Öffnen der Zwischenablage möglicherweise eine andere Anwendung geöffnet und den Besitz der Zwischenablage übernommen hat, und die Daten dieser Anwendung sollten nicht überschrieben werden.

In den meisten Fällen sollte die Anwendung die [**EmptyClipboard-Funktion**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) nicht aufrufen, bevor [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)aufgerufen wird, da dadurch die Zwischenablageformate gelöscht werden, die die Anwendung bereits gerendert hat.

Wenn die Anwendung zurückgibt, entfernt das System alle nicht formatierten Formate aus der Liste der verfügbaren Zwischenablageformate. Informationen zum verzögerten Rendering finden Sie unter [Verzögertes Rendering.](clipboard-operations.md#delayed-rendering)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERFORMAT**](wm-renderformat.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

