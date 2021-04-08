---
title: WM_CAP_SET_PREVIEWRATE Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ previewrate"-Meldung legt die Frame-Anzeige Rate im Vorschaumodus fest. Sie können diese Nachricht explizit oder mithilfe des cappreviewrate-Makros senden.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957134"
---
# <a name="wm_cap_set_previewrate-message"></a>\_ \_ Previewrate-Meldung für WM-Cap-Set \_

Die " **WM \_ Cap \_ Set \_ previewrate** "-Meldung legt die Frame-Anzeige Rate im Vorschaumodus fest. Sie können diese Nachricht explizit oder mithilfe des [**cappreviewrate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) -Makros senden.


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*
</dt> <dd>

Rate (in Millisekunden), mit der neue Frames aufgezeichnet und angezeigt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.

## <a name="remarks"></a>Bemerkungen

Im Vorschaumodus werden beträchtliche CPU-Ressourcen verwendet. Anwendungen können die Vorschau deaktivieren oder die Vorschau Rate verringern, wenn eine andere Anwendung den Fokus hat. Während der Streaming-Video Erfassung hat die Vorschau Aufgabe eine niedrigere Priorität als das Schreiben von Frames auf den Datenträger, und Vorschau Rahmen werden nur angezeigt, wenn keine anderen Puffer zum Schreiben verfügbar sind.

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

 

 





