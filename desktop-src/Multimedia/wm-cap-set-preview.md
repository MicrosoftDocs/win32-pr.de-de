---
title: WM_CAP_SET_PREVIEW-Nachricht (Vfw.h)
description: Die \_ WM CAP \_ SET \_ PREVIEW-Meldung aktiviert oder deaktiviert den Vorschaumodus.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25bf7f1ce2a61cb104c1e1764f9bca9c82d3aa40d44cc8a1eef9ce435584271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369384"
---
# <a name="wm_cap_set_preview-message"></a>WM \_ CAP \_ SET \_ PREVIEW-Meldung

Die **WM CAP SET \_ \_ \_ PREVIEW-Meldung** aktiviert oder deaktiviert den Vorschaumodus. Im Vorschaumodus werden Frames von der Erfassungshardware in den Systemspeicher übertragen und dann mithilfe von GDI-Funktionen im Erfassungsfenster angezeigt. Sie können diese Nachricht explizit oder mithilfe des [**CapPreview-Makros**](/windows/desktop/api/Vfw/nf-vfw-cappreview) senden.


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Vorschauflag. Geben Sie **TRUE** für diesen Parameter an, um den Vorschaumodus zu aktivieren, oder **FALSE,** um ihn zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Im Vorschaumodus werden erhebliche CPU-Ressourcen verwendet. Anwendungen können die Vorschau deaktivieren oder die Vorschaurate verringern, wenn eine andere Anwendung den Fokus hat. Der **fLiveWindow-Member** der [**CAPSTATUS-Struktur**](/windows/win32/api/vfw/ns-vfw-capstatus) gibt an, ob der Vorschaumodus derzeit aktiviert ist.

Durch aktivieren des Vorschaumodus wird der Überlagerungsmodus automatisch deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





