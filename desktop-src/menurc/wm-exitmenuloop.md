---
title: WM_EXITMENULOOP Meldung (Winuser. h)
description: Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife beendet wurde.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741705"
---
# <a name="wm_exitmenuloop-message"></a>WM \_ exitmenuloop-Meldung

Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife beendet wurde.


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob das Menü ein Kontextmenü ist. Dieser Parameter hat den Wert **true** , wenn es sich um ein Kontextmenü handelt, andernfalls **false** .

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

[**WM- \_ entermenuloop**](wm-entermenuloop.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

