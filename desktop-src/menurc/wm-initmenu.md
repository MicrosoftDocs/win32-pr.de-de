---
title: WM_INITMENU (Winuser.h)
description: Wird gesendet, wenn ein Menü aktiv wird.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU von Nachrichtenmenüs und anderen Ressourcen
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
ms.openlocfilehash: fff775849abf6a7e3be4530ce893e1ae8821cb4be6e9fb2888ef9bb0ee6d67d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939570"
---
# <a name="wm_initmenu-message"></a>WM \_ INITMENU-Nachricht

Wird gesendet, wenn ein Menü aktiv wird. Dies tritt auf, wenn der Benutzer auf ein Element in der Menüleiste klickt oder eine Menütaste drückt. Dadurch kann die Anwendung das Menü ändern, bevor es angezeigt wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das zu initialisierende Menü.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Eine **WM \_ INITMENU-Nachricht** wird nur gesendet, wenn zum ersten Mal auf ein Menü zugegriffen wird. Für jeden Zugriff wird nur eine **WM \_ INITMENU-Nachricht** generiert. Wenn Sie beispielsweise die Maus über mehrere Menüelemente bewegen, während Sie die Schaltfläche gedrückt halten, werden keine neuen Nachrichten generiert. **WM \_ INITMENU** stellt keine Informationen zu Menüelementen zur Verfügung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ INITMENUPOPUP**](wm-initmenupopup.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

