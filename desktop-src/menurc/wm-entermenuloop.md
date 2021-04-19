---
title: WM_ENTERMENULOOP Meldung (Winuser. h)
description: Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife eingegeben wurde.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337720"
---
# <a name="wm_entermenuloop-message"></a>WM- \_ entermenuloop-Meldung

Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife eingegeben wurde.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob das Menü Fenster mithilfe der [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion eingegeben wurde. Dieser Parameter hat den Wert true, wenn das Menü Fenster mithilfe von **TrackPopupMenu** eingegeben wurde, und **false** , wenn dies nicht der **Fall** war.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt 0 (null) zurück.

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

[**WM- \_ exitmenuloop**](wm-exitmenuloop.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

