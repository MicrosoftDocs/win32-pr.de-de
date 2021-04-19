---
title: WM_DRAWCLIPBOARD Meldung (Winuser. h)
description: Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn der Inhalt der Zwischenablage geändert wird. Dies ermöglicht es einem Fenster der Zwischenablage Anzeige, den neuen Inhalt der Zwischenablage anzuzeigen. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345289"
---
# <a name="wm_drawclipboard-message"></a>WM- \_ drawclipboard-Nachricht

Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn der Inhalt der Zwischenablage geändert wird. Dies ermöglicht es einem Fenster der Zwischenablage Anzeige, den neuen Inhalt der Zwischenablage anzuzeigen.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_DRAWCLIPBOARD                0x0308
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

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nur Zwischenablage-Viewer-Fenstern empfangen. Dies sind Fenster, die mithilfe der [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) -Funktion der Zwischenablage-Viewer-Kette hinzugefügt wurden.

Jedes Fenster, das die " **WM \_ drawclipboard** "-Nachricht empfängt, muss die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion anrufen, um die Nachricht an das nächste Fenster in der Zwischenablage-Viewer-Kette zu übergeben. Das Handle für das nächste Fenster in der Kette wird von [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)zurückgegeben und kann sich als Reaktion auf eine [**WM- \_ CHANGECBCHAIN**](wm-changecbchain.md) -Nachricht ändern.

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**Setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ CHANGECBCHAIN**](wm-changecbchain.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

