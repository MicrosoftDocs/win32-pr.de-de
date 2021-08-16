---
description: Einmal an ein Fenster gesendet, nachdem die modale Schleife zum Verschieben oder Dimensionieren beendet wurde.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: WM_EXITSIZEMOVE-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f451e846f2a262a30ccc73121d52c3732dbdfb160fe529535dcf353f077c351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849252"
---
# <a name="wm_exitsizemove-message"></a>WM \_ EXITSIZEMOVE-Nachricht

Einmal an ein Fenster gesendet, nachdem die modale Schleife zum Verschieben oder Dimensionieren beendet wurde. Das Fenster wechselt in die modale Schleife zum Verschieben oder Ändern der Größe, wenn der Benutzer auf die Titelleiste oder den Größenrahmen des Fensters klickt oder wenn das Fenster die [**WM \_ SYSCOMMAND-Nachricht**](../menurc/wm-syscommand.md) an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergibt und der *wParam-Parameter* der Nachricht den **SC \_ MOV** E- oder **SC \_ SIZE-Wert** angibt. Der Vorgang ist abgeschlossen, wenn [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zurückgegeben wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ENTERIZEMOVE**](wm-entersizemove.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
