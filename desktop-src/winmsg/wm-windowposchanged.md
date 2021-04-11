---
description: Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge aufgrund eines Aufrufes der Funktion SetWindowPos oder einer anderen Fenster Verwaltungsfunktion geändert wurde.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: WM_WINDOWPOSCHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128957"
---
# <a name="wm_windowposchanged-message"></a>WM- \_ windowposchge-Nachricht

Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge aufgrund eines Aufrufes der Funktion [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) oder einer anderen Fenster Verwaltungsfunktion geändert wurde.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) -Struktur, die Informationen über die neue Größe und Position des Fensters enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Standardmäßig sendet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die [**WM- \_ Größe**](wm-size.md) und die WM-Verschiebungs Nachricht an das-Fenster. [**\_**](wm-move.md) Die **WM- \_ Größe** und die WM-Verschiebungs Nachricht werden nicht gesendet, wenn eine Anwendung die **WM- \_ windowposchangsnachricht** verarbeitet, ohne **defwindowproc** Aufrufs. **\_** Es ist effizienter, jede verschiebe-oder Größen Änderungs Verarbeitung während der **WM- \_ windowposchge** -Nachricht auszuführen, ohne **defwindowproc** aufzurufenden.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Enddeferwindowpos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ verschieben**](wm-move.md)
</dt> <dt>

[**WM- \_ Größe**](wm-size.md)
</dt> <dt>

[**WM- \_ windowposchanging**](wm-windowposchanging.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
