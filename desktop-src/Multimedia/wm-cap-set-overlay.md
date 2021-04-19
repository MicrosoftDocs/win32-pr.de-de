---
title: WM_CAP_SET_OVERLAY Meldung (VFW. h)
description: Die WM-Obergrenze für die über \_ \_ \_ Lagerung aktiviert oder deaktiviert den Überlagerungs Modus. Im Überlagerungs Modus wird Video mithilfe der Hardware Überlagerung angezeigt. Sie können diese Nachricht explizit oder mithilfe des capoverlay-Makros senden.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY-Nachricht (Multimedia)
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
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346127"
---
# <a name="wm_cap_set_overlay-message"></a>Über \_ \_ \_ Lagerungs Nachricht für WM-Cap

Die **WM-Obergrenze für die über \_ \_ \_ Lagerung** aktiviert oder deaktiviert den Überlagerungs Modus. Im Überlagerungs Modus wird Video mithilfe der Hardware Überlagerung angezeigt. Sie können diese Nachricht explizit oder mithilfe des [**capoverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) -Makros senden.


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*c*
</dt> <dd>

Overlay-Flag. Geben Sie **true** für diesen Parameter an, um ihn zu aktivieren, oder **false** , um ihn zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Verwendung einer Überlagerung erfordert keine CPU-Ressourcen.

Der **fhasoverlay** -Member der [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur gibt an, ob das Gerät überlagern kann. Der **foverlaywindow** -Member der [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur gibt an, ob der Überlagerungs Modus aktuell aktiviert ist.

Durch Aktivieren des Überlagerungs Modus wird der Vorschaumodus automatisch deaktiviert.

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

 

 





