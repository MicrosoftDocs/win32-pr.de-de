---
title: WM_GESTURENOTIFY Meldung (Winuser. h)
description: Gibt Ihnen die Möglichkeit, die Gesten Konfiguration festzulegen.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- Windows-Fingereingabe für WM_GESTURENOTIFY Meldung
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
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104529"
---
# <a name="wm_gesturenotify-message"></a>WM \_ gesturenotify-Meldung

Gibt Ihnen die Möglichkeit, die Gesten Konfiguration festzulegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**gesturenotifystruct**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Von [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)sollte ein Wert zurückgegeben werden.

## <a name="remarks"></a>Bemerkungen

Wenn die **WM- \_ gesturenotify** -Nachricht empfangen wird, kann die Anwendung [**setgestureconfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) verwenden, um die zu empfangenden Gesten anzugeben. Diese Nachricht sollte immer mit der [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion zusammengefügt werden.

> [!Note]  
> Durch die Verarbeitung der " **\_ gesturenotify** "-Meldung wird die Gesten Konfiguration für die Lebensdauer des Fensters und nicht nur für die nächste Geste geändert.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie alle Gesten aktiviert werden. Weitere Beispiele finden Sie unter [**setgestureconfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[Programmier Handbuch für Windows-Touchgesten](guide-multi-touch-gestures.md)
</dt> <dt>

[**Gesturenotifystruct**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**Setgestureconfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

