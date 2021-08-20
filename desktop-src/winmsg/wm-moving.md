---
description: Wird an ein Fenster gesendet, das der Benutzer bewegt. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Position des Ziehrechtecks überwachen und bei Bedarf seine Position ändern.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: WM_MOVING Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45c27a985d8f048cc5e1b73f021b1bcf48c4f2ecf6fac435c85ea40aa8f6fc93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030782"
---
# <a name="wm_moving-message"></a>WM \_ MOVING-Nachricht

Wird an ein Fenster gesendet, das der Benutzer bewegt. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Position des Ziehrechtecks überwachen und bei Bedarf seine Position ändern.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) mit der aktuellen Position des Fensters in Bildschirmkoordinaten. Um die Position des Ziehrechtecks zu ändern, muss eine Anwendung die Elemente dieser Struktur ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte **TRUE** zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ MOVE**](wm-move.md)
</dt> <dt>

[**GRÖßE DER WM \_**](wm-sizing.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
