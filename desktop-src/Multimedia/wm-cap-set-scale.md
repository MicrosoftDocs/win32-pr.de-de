---
title: WM_CAP_SET_SCALE Meldung (VFW. h)
description: Mit der \_ Einstellung für die WM-Cap- \_ \_ Skalierung wird die Skalierung der Preview-Videobilder aktiviert oder deaktiviert.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106112"
---
# <a name="wm_cap_set_scale-message"></a>Formel zum Festlegen der WM-Abdeckung \_ \_ \_

Mit der Einstellung für die **WM-Cap- \_ \_ \_ Skalierung** wird die Skalierung der Preview-Videobilder aktiviert oder deaktiviert. Wenn die Skalierung aktiviert ist, wird der erfasste Videoframe auf die Abmessungen des Aufzeichnungs Fensters gestreckt. Sie können diese Nachricht explizit oder mithilfe des [**cappreviewscale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) -Makros senden.


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*c*
</dt> <dd>

Flag für die Vorschau Skalierung. Geben Sie **true** für diesen Parameter an, um die Vorschau Rahmen auf die Größe des Erfassungs Fensters zu erweitern, oder auf **false** , um Sie in ihrer natürlichen Größe anzuzeigen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Durch das Skalieren von Vorschaubildern wird die sofortige Darstellung der aufgezeichneten Frames im Aufzeichnungs Fenster gesteuert. Dies hat keine Auswirkung auf die Größe der in der Datei gespeicherten Frames.

Die Skalierung hat keine Auswirkungen, wenn Sie das Overlay zum Anzeigen von Videos im Frame Puffer verwenden.

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

 

 





