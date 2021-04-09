---
title: WM_CAP_SET_PREVIEW Meldung (VFW. h)
description: Die WM- \_ Obergrenze für die \_ Festlegung von \_ Voreinstellungen aktiviert oder deaktiviert den Vorschaumodus.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW-Nachricht (Multimedia)
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
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106113"
---
# <a name="wm_cap_set_preview-message"></a>WM- \_ Obergrenze für \_ festgelegte \_ Vorschau

Die **WM- \_ Obergrenze für die \_ Festlegung von \_ Voreinstellungen** aktiviert oder deaktiviert den Vorschaumodus. Im Vorschaumodus werden Frames von der Aufzeichnungs Hardware in den Systemspeicher übertragen und dann im Erfassungsfenster mithilfe von GDI-Funktionen angezeigt. Sie können diese Nachricht explizit oder mithilfe des [**cappreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) -Makros senden.


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*c*
</dt> <dd>

Vorschauflag. Geben Sie **true** für diesen Parameter an, um den Vorschaumodus zu aktivieren oder **false** , um ihn zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Im Vorschaumodus werden beträchtliche CPU-Ressourcen verwendet. Anwendungen können die Vorschau deaktivieren oder die Vorschau Rate verringern, wenn eine andere Anwendung den Fokus hat. Der **flivewindow** -Member der [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur zeigt an, ob der Vorschaumodus aktuell aktiviert ist.

Durch Aktivieren des Vorschaumodus wird der Überlagerungs Modus automatisch deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





