---
title: WM_CAP_GET_MCI_DEVICE Meldung (VFW. h)
description: Die "WM \_ Cap \_ get \_ MCI Device"- \_ Meldung Ruft den Namen eines MCI-Geräts ab, das zuvor mit der "WM \_ Cap \_ Set \_ MCI \_ Device"-Meldung festgelegt wurde. Sie können diese Nachricht explizit oder mithilfe des capgetmcidevicename-Makros senden.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475072"
---
# <a name="wm_cap_get_mci_device-message"></a>WM- \_ Cap- \_ \_ MCI- \_ Geräte Nachricht erhalten

Die " **WM \_ Cap \_ get \_ MCI \_ Device** "-Meldung Ruft den Namen eines MCI-Geräts ab, das zuvor mit der " [**WM \_ Cap \_ Set \_ MCI \_ Device**](wm-cap-set-mci-device.md) "-Meldung festgelegt wurde. Sie können diese Nachricht explizit oder mithilfe des [**capgetmcidevicename**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) -Makros senden.


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*
</dt> <dd>

Länge (in Byte) des Puffers, auf den von **szName** verwiesen wird.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den MCI-Gerätenamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

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

 

 





