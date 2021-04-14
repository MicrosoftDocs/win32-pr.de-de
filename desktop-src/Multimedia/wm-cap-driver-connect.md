---
title: WM_CAP_DRIVER_CONNECT Meldung (VFW. h)
description: Mit der CONNECT-Nachricht des WM- \_ Cap- \_ Treibers wird \_ ein Aufzeichnungs Fenster mit einem Aufzeichnungs Treiber verbunden. Sie können diese Nachricht explizit oder mithilfe des capdriverconnect-Makros senden.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT-Nachricht (Multimedia)
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
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391818"
---
# <a name="wm_cap_driver_connect-message"></a>\_ \_ \_ Verbindungs Meldung zum WM-Cap-Treiber

Mit der CONNECT-Nachricht des **WM- \_ Cap- \_ Treibers \_** wird ein Aufzeichnungs Fenster mit einem Aufzeichnungs Treiber verbunden. Sie können diese Nachricht explizit oder mithilfe des [**capdriverconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) -Makros senden.


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Der Index des Erfassungs Treibers. Der Index kann zwischen 0 und 9 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn der angegebene Erfassungs Treiber nicht mit dem Erfassungsfenster verbunden werden kann.

## <a name="remarks"></a>Bemerkungen

Durch das Verbinden eines Erfassungs Treibers mit einem Aufzeichnungs Fenster wird automatisch eine Verbindung mit allen zuvor verbundenen Aufzeichnungs Treibern getrennt.

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

 

 





