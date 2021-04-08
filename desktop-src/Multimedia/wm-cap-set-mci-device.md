---
title: WM_CAP_SET_MCI_DEVICE Meldung (VFW. h)
description: Die \_ \_ MCI-Geräte Meldung "WM Cap Set" \_ \_ gibt den Namen des MCI-Videogeräts an, das zum Erfassen von Daten verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des capabtmcidevicename-Makros senden.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE-Nachricht (Multimedia)
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
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740056"
---
# <a name="wm_cap_set_mci_device-message"></a>WM- \_ Cap- \_ \_ Geräte Nachricht für MCI- \_ Gerät festlegen

Die **\_ \_ \_ MCI- \_ Geräte Meldung "WM Cap Set** " gibt den Namen des MCI-Videogeräts an, das zum Erfassen von Daten verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des [**capabtmcidevicename**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) -Makros senden.


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Geräts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

In dieser Meldung wird der MCI-Gerätename in einer internen Struktur gespeichert. Das Gerät wird nicht geöffnet, oder es wird nicht darauf zugegriffen. Der Standardgeräte Name ist **null**.

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

 

 





