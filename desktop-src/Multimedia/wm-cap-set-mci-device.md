---
title: WM_CAP_SET_MCI_DEVICE-Nachricht (Vfw.h)
description: Die MELDUNG WM \_ CAP \_ SET \_ MCI DEVICE gibt den Namen des \_ MCI-Videogeräts an, das zum Erfassen von Daten verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des Makros capSetMCIDeviceName senden.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2df82b171e2353b51198fcd4a908abb586d981417c3fd14e5a81731975012aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622179"
---
# <a name="wm_cap_set_mci_device-message"></a>WM CAP SET MCI DEVICE message (WM \_ CAP \_ SET \_ MCI \_ DEVICE-Meldung)

Die **MELDUNG WM CAP SET \_ \_ \_ MCI \_ DEVICE** gibt den Namen des MCI-Videogeräts an, das zum Erfassen von Daten verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des [**Makros capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) senden.


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Geräts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

In dieser Meldung wird der MCI-Gerätename in einer internen Struktur gespeichert. Das Gerät wird nicht geöffnet, oder es wird darauf zugegriffen. Der Standardgerätename ist **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





