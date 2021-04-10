---
title: WM_CAP_DLG_VIDEOCOMPRESSION Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ DLG \_ videocompression" zeigt ein Dialogfeld an, in dem der Benutzer einen während des Erfassungs Vorgangs zu verwendenden Kompressor auswählen kann.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040577"
---
# <a name="wm_cap_dlg_videocompression-message"></a>WM- \_ Cap- \_ DLG- \_ Video Komprimierungs Meldung

Die Meldung " **WM \_ Cap \_ DLG \_ videocompression** " zeigt ein Dialogfeld an, in dem der Benutzer einen während des Erfassungs Vorgangs zu verwendenden Kompressor auswählen kann. Die Liste der verfügbaren Kompressoren kann sich von dem im Dialogfeld Videoformat des Erfassungs Treibers ausgewählten Videoformat unterscheiden. Sie können diese Nachricht explizit oder mithilfe des [**capdlgvideocompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) -Makros senden.


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Nachricht mit Erfassungs Treibern, die Frames nur im BI RGB-Format bereitstellen \_ . Diese Meldung ist am nützlichsten beim Schritt Aufzeichnungs Vorgang, um die Erfassung und Komprimierung in einem einzelnen Vorgang zu kombinieren. Das Komprimieren von Frames mit einem Software-Kompressor als Teil eines echt Zeit Erfassungs Vorgangs ist wahrscheinlich zu viel zeitaufwändig.

Die Komprimierung hat keine Auswirkungen auf die in die Zwischenablage kopierten Frames.

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

 

 





