---
description: Wird einmal an ein Fenster gesendet, nachdem es die modale Verschiebungs-oder Anpassungs Schleife verlassen hat.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: WM_EXITSIZEMOVE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347482"
---
# <a name="wm_exitsizemove-message"></a>WM- \_ exitsizemove-Meldung

Wird einmal an ein Fenster gesendet, nachdem es die modale Verschiebungs-oder Anpassungs Schleife verlassen hat. Das Fenster wechselt in die modale Verschiebungs-oder Anpassungs Schleife, wenn der Benutzer auf die Titelleiste des Fensters oder den Größen Anpassungsrahmen klickt, oder wenn das Fenster die " [**WM \_ syscommand**](../menurc/wm-syscommand.md) "-Meldung an die Funktion " [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) " übergibt und der *wParam* -Parameter der Meldung den Wert **SC \_ MOV** E oder **SC \_ size** angibt. Der Vorgang ist fertiggestellt, wenn [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zurückgegeben wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

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

[**WM \_ Enterprise**](wm-entersizemove.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
