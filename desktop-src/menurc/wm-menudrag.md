---
title: WM_MENUDRAG Meldung (Winuser.h)
description: Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Benutzer ein Menüelement zieht.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG Meldung Menüs und andere Ressourcen
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
ms.openlocfilehash: 22792c7606bb001b72b7c4751d14129bca02c5b4a5b337e0349a9a9a2120b62a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971799"
---
# <a name="wm_menudrag-message"></a>WM \_ MENUDRAG-Meldung

Wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Benutzer ein Menüelement zieht.


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Position des Elements, an der der Ziehvorgang begonnen hat.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Menü, das das Element enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung sollte einen der folgenden Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                   | Beschreibung                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_ CONTINUE**</dt> <dt>0</dt> </dl> | Das Menü sollte aktiv bleiben. Wenn die Maus losgelassen wird, sollte sie ignoriert werden.<br/> |
| <dl> <dt>**MND \_ ENDMENU**</dt> <dt>1</dt> </dl>  | Das Menü sollte beendet werden.<br/>                                                      |



 

## <a name="remarks"></a>Hinweise

Die Anwendung kann die [**DoDragDrop-Funktion**](/windows/win32/api/ole2/nf-ole2-dodragdrop) als Reaktion auf diese Meldung aufrufen.

To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.

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

[**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

