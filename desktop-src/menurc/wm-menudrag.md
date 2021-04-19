---
title: WM_MENUDRAG Meldung (Winuser. h)
description: Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Benutzer ein Menü Element zieht.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346769"
---
# <a name="wm_menudrag-message"></a>WM- \_ menudrag-Meldung

Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Benutzer ein Menü Element zieht.


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Position des Elements, an dem der Zieh Vorgang begonnen wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Menü, das das Element enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung muss einen der folgenden Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                   | BESCHREIBUNG                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_ Fortsetzen**</dt> von <dt>0</dt> </dl> | Das Menü sollte aktiv bleiben. Wenn die Maus losgelassen wird, sollte Sie ignoriert werden.<br/> |
| <dl> <dt>**MND \_ Endmenu**</dt> <dt>1</dt> </dl>  | Das Menü sollte beendet werden.<br/>                                                      |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung kann die [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) -Funktion als Reaktion auf diese Nachricht aufzurufen.

Um ein Drag & Drop-Menü zu erstellen, rufen Sie [**setmenuinfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) mit **MNS \_ DragDrop** auf.

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

[**Setmenuinfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

