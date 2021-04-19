---
description: Wird an ein Fenster gesendet, das der Benutzer verschiebt. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Position des Zieh Rechtecks überwachen und ggf. ihre Position ändern.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: WM_MOVING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346101"
---
# <a name="wm_moving-message"></a>WM-Verschiebungs \_ Meldung

Wird an ein Fenster gesendet, das der Benutzer verschiebt. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Position des Zieh Rechtecks überwachen und ggf. ihre Position ändern.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur mit der aktuellen Position des Fensters in Bildschirm Koordinaten. Um die Position des Zieh Rechtecks zu ändern, muss eine Anwendung die Elemente dieser Struktur ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.

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

[**WM \_ verschieben**](wm-move.md)
</dt> <dt>

[**WM- \_ Größe**](wm-sizing.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
