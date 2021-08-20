---
title: WM_CAP_DRIVER_GET_CAPS Nachricht (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ DRIVER GET \_ \_ CAPS gibt die Hardwarefunktionen des Erfassungstreibers zurück, der derzeit mit einem Erfassungsfenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des CapDriverGetCaps-Makros senden.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aecc863234cddf64bece47896015fd01e97093d227951aef69363136e55cabe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687080"
---
# <a name="wm_cap_driver_get_caps-message"></a>WM CAP DRIVER GET CAPS message (WM \_ CAP \_ DRIVER GET \_ \_ CAPS-Meldung)

Die **MELDUNG WM CAP DRIVER GET \_ \_ \_ \_ CAPS** gibt die Hardwarefunktionen des Erfassungstreibers zurück, der derzeit mit einem Erfassungsfenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des [**CapDriverGetCaps-Makros**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) senden.


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Größe der Struktur in Bytes, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*
</dt> <dd>

Zeiger auf die [**CAPDRIVERCAPS-Struktur,**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) die die Hardwarefunktionen enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, oder **FALSE,** wenn das Erfassungsfenster nicht mit einem Erfassungstreiber verbunden ist.

## <a name="remarks"></a>Hinweise

Die in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) zurückgegebenen Funktionen sind für einen bestimmten Erfassungstreiber konstant. Anwendungen müssen diese Informationen einmal abrufen, wenn der Erfassungstreiber zum ersten Mal mit einem Erfassungsfenster verbunden ist.

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

 

 





