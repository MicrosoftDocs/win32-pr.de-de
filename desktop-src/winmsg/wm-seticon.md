---
description: Ordnet ein neues großes oder kleines Symbol einem Fenster zu. Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: WM_SETICON Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216040"
---
# <a name="wm_seticon-message"></a>WM- \_ Nachricht

Ordnet ein neues großes oder kleines Symbol einem Fenster zu. Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des festzulegenden Symbols. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                       | Bedeutung                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Symbol \_ Big**</dt> <dt>1</dt> </dl>       | Legen Sie das große Symbol für das Fenster fest.<br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Symbol \_ Kleiner**</dt> <dt>0</dt> </dl> | Legen Sie das kleine Symbol für das Fenster fest.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das neue große oder kleine Symbol. Wenn dieser Parameter **null** ist, wird das Symbol entfernt, das von *wParam* angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Der Rückgabewert ist ein Handle für das vorherige große oder kleine Symbol, abhängig vom Wert von *wParam*. Der Wert ist **null** , wenn das Fenster zuvor kein Symbol des Typs enthielt, der von *wParam* angegeben wurde.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt ein Handle für das vorherige große oder kleine Symbol zurück, das dem Fenster zugeordnet ist, je nach Wert von *wParam*.

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

[**WM- \_ getIcon**](wm-geticon.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
