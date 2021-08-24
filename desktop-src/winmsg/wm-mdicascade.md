---
description: Eine Anwendung sendet die WM \_ MDICASCADE-Nachricht an ein MDI-Clientfenster (Multiple Document Interface), um alle untergeordneten Fenster in einem kaskadierten Format zu anordnen.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: WM_MDICASCADE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59977b86a63c62d69571a6e5c631dd9044fb57f072adf04b0882e16af4f65e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448730"
---
# <a name="wm_mdicascade-message"></a>WM \_ MDICASCADE-Meldung

Eine Anwendung sendet die **WM \_ MDICASCADE-Nachricht** an ein MDI-Clientfenster (Multiple Document Interface), um alle untergeordneten Fenster in einem kaskadierten Format zu anordnen.


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Überlappungsverhalten. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_ SKIPDISABLED-0x0002**</dt> <dt></dt> </dl> | Verhindert, dass deaktivierte untergeordnete MDI-Fenster kaskadiert werden. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_ ZORDER**</dt> <dt>0x0004</dt> </dl>                   | Ordnet die Fenster in Z-Reihenfolge an.<br/>                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **BOOL**

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Meldung fehlschlägt, ist der Rückgabewert **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

[**WM \_ MDITILE**](wm-mditile.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mehrere Dokumentschnittstellen](multiple-document-interface.md)
</dt> </dl>

 

 




