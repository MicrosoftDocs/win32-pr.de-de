---
title: WM_CAP_DRIVER_CONNECT (Vfw.h)
description: Die WM \_ CAP \_ DRIVER \_ CONNECT-Meldung verbindet ein Erfassungsfenster mit einem Erfassungstreiber. Sie können diese Nachricht explizit oder mithilfe des Makros capDriverConnect senden.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT von Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b0e54d496302488db653505321778bcd22546bd2ed9b2180aa0e15cb6969f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622629"
---
# <a name="wm_cap_driver_connect-message"></a>WM \_ CAP \_ DRIVER \_ CONNECT-Meldung

Die **WM CAP DRIVER \_ \_ \_ CONNECT-Meldung** verbindet ein Erfassungsfenster mit einem Erfassungstreiber. Sie können diese Nachricht explizit oder mithilfe des [**Makros capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) senden.


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Index des Erfassungstreibers. Der Index kann zwischen 0 und 9 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, oder **FALSE,** wenn der angegebene Erfassungstreiber nicht mit dem Erfassungsfenster verbunden werden kann.

## <a name="remarks"></a>Hinweise

Beim Verbinden eines Erfassungstreibers mit einem Erfassungsfenster werden alle zuvor verbundenen Erfassungstreiber automatisch getrennt.

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

[Videoaufnahmenachrichten](video-capture-messages.md)
</dt> </dl>

 

 





