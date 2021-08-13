---
description: Eine Anwendung sendet die \_ WM-MDITILE-Nachricht an ein MDI-Clientfenster (Multiple Document Interface), um alle untergeordneten MDI-Fenster in einem Kachelformat anzuordnen.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: WM_MDITILE Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379394d413c0c9d15b9f63297934b97da6aff65b4ae5d803627cb0107493c4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436217"
---
# <a name="wm_mditile-message"></a>WM \_ MDITILE-Nachricht

Eine Anwendung sendet die **\_ WM-MDITILE-Nachricht** an ein MDI-Clientfenster (Multiple Document Interface), um alle untergeordneten MDI-Fenster in einem Kachelformat anzuordnen.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Kacheloption. Dieser Parameter kann einer der folgenden Werte sein, optional kombiniert mit **MDITILE \_ SKIPDISABLED,** um zu verhindern, dass deaktivierte untergeordnete MDI-Fenster gekachelt werden.



| Wert                                                                                                                                                                                                                                    | Bedeutung                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_ HORIZONTALE**</dt> <dt>0x0001</dt> </dl> | Kachelfenster horizontal.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_ VERTICAL**</dt> <dt>0x0000</dt> </dl>       | Kachelfenster vertikal.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Nachricht fehlschlägt, ist der Rückgabewert **FALSE.**

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

[**WM \_ MDICASCADE**](wm-mdicascade.md)
</dt> <dt>

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schnittstelle für mehrere Dokumente](multiple-document-interface.md)
</dt> </dl>

 

 




