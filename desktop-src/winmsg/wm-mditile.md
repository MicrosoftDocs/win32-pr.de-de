---
description: Eine Anwendung sendet die WM- \_ mditile-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten MDI-Fenster in einem Kachel Format anzuordnen.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: WM_MDITILE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214544"
---
# <a name="wm_mditile-message"></a>WM- \_ mditile-Nachricht

Eine Anwendung sendet die **WM- \_ mditile** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten MDI-Fenster in einem Kachel Format anzuordnen.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die gezitzungsoption. Dieser Parameter kann einen der folgenden Werte aufweisen, optional kombiniert mit **mditile \_ skipdeaktiviert** , um zu verhindern, dass deaktivierte untergeordnete MDI-Fenster nebeneinander gekachelt werden.



| Wert                                                                                                                                                                                                                                    | Bedeutung                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**Mditile \_ HORIZONTAL**</dt> <dt>0x0001</dt> </dl> | Kacheln Fenster horizontal.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**Mditile \_ Vertikal**</dt> <dt>0x0000</dt> </dl>       | Kacheln Fenster vertikal.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**".

Wenn die Meldung fehlschlägt, ist der Rückgabewert **false**.

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

[**WM- \_ mdicascade**](wm-mdicascade.md)
</dt> <dt>

[**WM- \_ mdiiconarrange**](wm-mdiiconarrange.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Mehrere Dokument Schnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




