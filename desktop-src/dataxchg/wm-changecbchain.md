---
title: WM_CHANGECBCHAIN Meldung (Winuser. h)
description: Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn ein Fenster aus der Kette entfernt wird. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104090"
---
# <a name="wm_changecbchain-message"></a>WM \_ CHANGECBCHAIN-Meldung

Wird an das erste Fenster in der Zwischenablage-Viewer-Kette gesendet, wenn ein Fenster aus der Kette entfernt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, das aus der Zwischenablage-Viewer-Kette entfernt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das nächste Fenster in der Kette nach dem Fenster, das entfernt wird. Dieser Parameter ist **null** , wenn das Fenster, das entfernt wird, das letzte Fenster in der Kette ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Jedes Fenster der Zwischenablage Anzeige speichert das Handle für das nächste Fenster in der Zwischenablage-Viewer-Kette. Anfänglich ist dieses Handle der Rückgabewert der Funktion [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Wenn ein Fenster der Zwischenablage Anzeige die **WM- \_ CHANGECBCHAIN** -Nachricht empfängt, sollte die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion aufgerufen werden, um die Nachricht an das nächste Fenster in der Kette zu übergeben, es sei denn, das Fenster wird im nächsten Fenster entfernt. In diesem Fall sollte der Zwischenablage-Viewer das durch den *LPARAM* -Parameter angegebene Handle als das nächste Fenster in der Kette speichern.

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

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

