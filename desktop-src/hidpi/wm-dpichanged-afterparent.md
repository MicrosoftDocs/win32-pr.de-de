---
title: WM_DPICHANGED_AFTERPARENT Meldung (Winuser.h)
description: Bei Fenstern der obersten Ebene pro Monitor v2 wird diese Meldung an alle HWNDs in der untergeordneten HWDN-Struktur des Fensters gesendet, für das eine DPI-Änderung erfolgt. | WM_DPICHANGED_AFTERPARENT Meldung (Winuser.h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT Meldung Hoher DPI-Anteil
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
ms.openlocfilehash: d47f303db19438f1e7e2cd77df60ddace76bec791bb1789bed47e3f09d8a197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759363"
---
# <a name="wm_dpichanged_afterparent-message"></a>WM \_ DPICHANGED \_ AFTERPARENT-Nachricht

Bei Fenstern der obersten Ebene pro [Monitor v2](dpi-awareness-context.md) wird diese Meldung an alle HWNDs in der untergeordneten HWDN-Struktur des Fensters gesendet, für das eine DPI-Änderung erfolgt. Diese Meldung tritt auf, nachdem das Fenster der obersten Ebene [**WM \_ DPICHANGED**](wm-dpichanged.md)empfängt und die untergeordnete Struktur von oben nach unten durchläuft.


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

## <a name="remarks"></a>Hinweise

Diese Meldung wird in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)nicht standardmäßig verarbeitet.

Diese Meldung wird nur gesendet, wenn das Fenster der obersten Ebene über einen DPI-Awareness-Kontext von PMv2 verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WM \_ DPICHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ DPICHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

