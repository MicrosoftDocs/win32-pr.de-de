---
title: ICM_ABOUT Meldung (VFW. h)
description: In der ICM Info- \_ Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Dialogfeld Info anzuzeigen, oder ein Video Komprimierungs Treiber wird abgefragt, um zu bestimmen, ob er über ein Dialogfeld Info verfügt Sie können diese Nachricht explizit oder mithilfe des icabout-Makros senden.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040079"
---
# <a name="icm_about-message"></a>ICM \_ zur Meldung

In der ICM Info-Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Dialogfeld Info anzuzeigen, oder ein Video Komprimierungs Treiber wird abgefragt, um zu bestimmen, ob er über ein Dialogfeld Info verfügt **\_** Sie können diese Nachricht explizit oder mithilfe des [**icabout**](/windows/desktop/api/Vfw/nf-vfw-icabout) -Makros senden.


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle für das übergeordnete Fenster des angezeigten Dialog Felds. Sie können auch bestimmen, ob ein Treiber über ein Dialogfeld Info verfügt, indem Sie-1 in diesem Parameter angeben, wie im [**icqueryabout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) -Makro. Der Treiber gibt ICERR \_ OK zurück, wenn ein Info Dialogfeld oder ICERR \_ nicht unterstützt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





