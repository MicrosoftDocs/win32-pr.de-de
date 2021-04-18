---
title: WM_INITMENU Meldung (Winuser. h)
description: Wird gesendet, wenn ein Menü aktiv wird.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340007"
---
# <a name="wm_initmenu-message"></a>WM- \_ InitMenu-Meldung

Wird gesendet, wenn ein Menü aktiv wird. Sie tritt auf, wenn der Benutzer auf ein Element in der Menüleiste klickt oder eine Menü Taste drückt. Dadurch kann die Anwendung das Menü ändern, bevor es angezeigt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Menü, das initialisiert werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Eine **WM- \_ InitMenu** -Meldung wird nur gesendet, wenn zum ersten Mal auf ein Menü zugegriffen wird. für jeden Zugriff wird nur eine **WM- \_ InitMenu** -Nachricht generiert. Wenn Sie die Maus z. b. über mehrere Menü Elemente bewegen, während Sie die Schaltfläche gedrückt halten, werden keine neuen Nachrichten generiert. **WM \_ InitMenu** bietet keine Informationen zu Menü Elementen.

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

[**WM \_ initmenupopup**](wm-initmenupopup.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

