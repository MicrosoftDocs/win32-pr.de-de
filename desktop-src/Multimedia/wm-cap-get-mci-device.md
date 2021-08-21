---
title: WM_CAP_GET_MCI_DEVICE Meldung (Vfw.h)
description: Die \_ WM CAP \_ GET \_ MCI \_ DEVICE-Nachricht ruft den Namen eines MCI-Geräts ab, das zuvor mit der WM \_ CAP SET \_ \_ MCI \_ DEVICE-Nachricht festgelegt wurde. Sie können diese Nachricht explizit oder mithilfe des Makros capGetMCIDeviceName senden.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE nachricht Windows Multimedia
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
ms.openlocfilehash: b9471177693bfbd5646d93e8487395cdf330b8281a1f43fa00d79dc690e6d718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800653"
---
# <a name="wm_cap_get_mci_device-message"></a>WM \_ CAP \_ GET \_ MCI DEVICE \_ message

Die **WM CAP GET \_ \_ \_ MCI \_ DEVICE-Nachricht** ruft den Namen eines MCI-Geräts ab, das zuvor mit der [**WM CAP SET \_ \_ \_ MCI \_ DEVICE-Nachricht**](wm-cap-set-mci-device.md) festgelegt wurde. Sie können diese Nachricht explizit oder mithilfe des [**Makros capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) senden.


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Länge des Puffers in Bytes, auf den von **szName** verwiesen wird.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den MCI-Gerätenamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

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

 

 





