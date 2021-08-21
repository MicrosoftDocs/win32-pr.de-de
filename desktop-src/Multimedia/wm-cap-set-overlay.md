---
title: WM_CAP_SET_OVERLAY Nachricht (Vfw.h)
description: Die WM \_ CAP \_ SET \_ OVERLAY-Meldung aktiviert oder deaktiviert den Überlagerungsmodus. Im Überlagerungsmodus wird das Video mithilfe von Hardwareüberlagerungen angezeigt. Sie können diese Nachricht explizit oder mithilfe des capOverlay-Makros senden.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10f2161f3c163fb5f6c411293770a2b2ba3907bef7eb03aad2d67b0e0637abbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135092"
---
# <a name="wm_cap_set_overlay-message"></a>WM \_ CAP \_ SET \_ OVERLAY-Nachricht

Die **WM CAP SET \_ \_ \_ OVERLAY-Meldung** aktiviert oder deaktiviert den Überlagerungsmodus. Im Überlagerungsmodus wird das Video mithilfe von Hardwareüberlagerungen angezeigt. Sie können diese Nachricht explizit oder mithilfe des [**CapOverlay-Makros**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) senden.


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Überlagerungsflag. Geben Sie **TRUE** für diesen Parameter an, um den Überlagerungsmodus zu aktivieren, oder **FALSE,** um ihn zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Die Verwendung einer Überlagerung erfordert keine CPU-Ressourcen.

Der **fHasOverlay-Member** der [**CAPDRIVERCAPS-Struktur**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) gibt an, ob das Gerät überlagert werden kann. Der **fOverlayWindow-Member** der [**CAPSTATUS-Struktur**](/windows/win32/api/vfw/ns-vfw-capstatus) gibt an, ob der Überlagerungsmodus derzeit aktiviert ist.

Durch aktivieren des Überlagerungsmodus wird der Vorschaumodus automatisch deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





