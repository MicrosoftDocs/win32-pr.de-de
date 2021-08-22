---
title: WM_DPICHANGED_BEFOREPARENT (Winuser.h)
description: Bei Fenstern der obersten Ebene pro Monitor v2 wird diese Meldung an alle HWNDs in der untergeordneten HWDN-Struktur des Fensters gesendet, für das eine DPI-Änderung ausgeführt wird. | WM_DPICHANGED_BEFOREPARENT (Winuser.h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT meldung High DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a52216052f597ce26e5be476a970ff78f0297c08124c9b1ca89453b6fca76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557670"
---
# <a name="wm_dpichanged_beforeparent-message"></a>WM \_ DPICHANGED \_ BEFOREPARENT-Meldung

Bei Fenstern der obersten Ebene pro [Monitor v2](dpi-awareness-context.md) wird diese Meldung an alle HWNDs in der untergeordneten HWDN-Struktur des Fensters gesendet, für das eine DPI-Änderung ausgeführt wird. Diese Meldung tritt auf, bevor das Fenster der obersten Ebene [**WM \_ DPICHANGED**](wm-dpichanged.md)empfängt und die untergeordnete Struktur von unten nach oben durchläuft.


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
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

Dieser Wert wird nicht verwendet und vom System ignoriert.

## <a name="remarks"></a>Hinweise

Es gibt keine Standardbehandlung dieser Meldung in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Diese Meldung wird nur gesendet, wenn das Fenster der obersten Ebene über den DPI-Bewusstseinskontext PMv2 verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM \_ DPICHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ DPICHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)
</dt> </dl>

 

