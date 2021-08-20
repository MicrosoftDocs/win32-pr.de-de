---
title: WM_CAP_SET_VIDEOFORMAT Meldung (Vfw.h)
description: Die \_ WM CAP \_ SET \_ VIDEOFORMAT-Nachricht legt das Format der erfassten Videodaten fest. Sie können diese Nachricht explizit oder mithilfe des CapSetVideoFormat-Makros senden.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c543f613fedf54518579829d6825bd20dc4738ae03cb77f0996f8a58a123cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135015"
---
# <a name="wm_cap_set_videoformat-message"></a>WM \_ CAP \_ SET \_ VIDEOFORMAT-Meldung

Die **WM CAP SET \_ \_ \_ VIDEOFORMAT-Nachricht** legt das Format der erfassten Videodaten fest. Sie können diese Nachricht explizit oder mithilfe des [**CapSetVideoFormat-Makros**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) senden.


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe der Struktur in Bytes, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

Zeiger auf eine [**BITMAPINFO-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Da Videoformate gerätespezifisch sind, sollten Anwendungen den Rückgabewert dieser Funktion überprüfen, um zu ermitteln, ob das Format vom Treiber akzeptiert wird.

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

 

