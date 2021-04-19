---
title: WM_DPICHANGED_AFTERPARENT Meldung (Winuser. h)
description: Für Fenster der obersten Ebene von Monitor v2 wird diese Nachricht an alle hwnds in der untergeordneten hwdn-Struktur des Fensters gesendet, das eine dpi-Änderung durchläuft. | WM_DPICHANGED_AFTERPARENT Meldung (Winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT Message High dpi
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357209"
---
# <a name="wm_dpichanged_afterparent-message"></a>WM-dpichanged-nach-über \_ \_ geordnete Nachricht

Für Fenster der obersten Ebene von [Monitor v2](dpi-awareness-context.md) wird diese Nachricht an alle hwnds in der untergeordneten hwdn-Struktur des Fensters gesendet, das eine dpi-Änderung durchläuft. Diese Meldung tritt auf, nachdem das Fenster der obersten Ebene [**WM \_ dpichanged**](wm-dpichanged.md)empfängt und die untergeordnete Struktur von oben nach unten durchläuft.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Wert wird nicht verwendet und ist 0 (null).

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Wert wird nicht verwendet und ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Wert wird vom System nicht verwendet und ignoriert.

## <a name="remarks"></a>Bemerkungen

In [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)gibt es keine Standardbehandlung für diese Nachricht.

Diese Meldung wird nur gesendet, wenn das Fenster der obersten Ebene den dpi-Kontext PMv2 hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ dpichanged**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ dpichanged \_ beforeparent**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

