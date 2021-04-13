---
title: WM_CAP_DRIVER_GET_CAPS Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ Driver \_ get \_ Caps" gibt die Hardwarefunktionen des Aufzeichnungs Treibers zurück, der zurzeit mit einem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des capdrivergetcaps-Makros senden.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS-Nachricht (Multimedia)
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
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518959"
---
# <a name="wm_cap_driver_get_caps-message"></a>WM- \_ Cap- \_ Treiber \_ Get Caps- \_ Nachricht

Die Meldung " **WM \_ Cap \_ Driver \_ get \_ Caps** " gibt die Hardwarefunktionen des Aufzeichnungs Treibers zurück, der zurzeit mit einem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des [**capdrivergetcaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) -Makros senden.


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.

</dd> <dt>

<span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*pscaps*
</dt> <dd>

Ein Zeiger auf die [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur, die die Hardwarefunktionen enthalten soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.

## <a name="remarks"></a>Bemerkungen

Die in [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) zurückgegebenen Funktionen sind für einen bestimmten Erfassungs Treiber konstant. Anwendungen müssen diese Informationen einmal abrufen, wenn der Erfassungs Treiber zum ersten Mal mit einem Aufzeichnungs Fenster verbunden ist.

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

 

 





