---
title: WM_GESTURENOTIFY Meldung (Winuser.h)
description: Gibt Ihnen die Möglichkeit, die Gestenkonfiguration festzulegen.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY Nachricht Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d474f356310a0d7949cecf36e7af9cb586a76029171dfe27c1679970e481ed1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435236"
---
# <a name="wm_gesturenotify-message"></a>WM \_ GESTURENOTIFY-Nachricht

Gibt Ihnen die Möglichkeit, die Gestenkonfiguration festzulegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein Wert sollte von [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)zurückgegeben werden.

## <a name="remarks"></a>Hinweise

Wenn die **WM \_ GESTURENOTIFY-Nachricht** empfangen wird, kann die Anwendung [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) verwenden, um die zu empfangenden Gesten anzugeben. Diese Nachricht sollte immer mithilfe der [DefWindowProc-Funktion](/windows/win32/api/winuser/nf-winuser-defwindowproca) per Blase angezeigt werden.

> [!Note]  
> Die Behandlung der **WM \_ GESTURENOTIFY-Nachricht** ändert die Gestenkonfiguration für die Lebensdauer des Fensters, nicht nur für die nächste Geste.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie alle Gesten aktiviert werden. Weitere Beispiele finden Sie unter [**SetGestureConfig.**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[Windows Programmierhandbuch für Touchgesten](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

