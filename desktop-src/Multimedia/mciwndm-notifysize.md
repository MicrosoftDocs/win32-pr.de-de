---
title: MCIWNDM_NOTIFYSIZE Meldung (VFW. h)
description: Die Meldung mciwndm \_ notifiysize benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fenstergröße geändert hat.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103434"
---
# <a name="mciwndm_notifysize-message"></a>Meldung zu mciwndm \_ notifiysize

Die Meldung **mciwndm \_ notifiysize** benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich die Fenstergröße geändert hat.


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle für das mciwnd-Fenster.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die Benachrichtigung über Änderungen in der Größe eines mciwnd-Fensters aktivieren, indem Sie den mciwndf- \_ Fenster Stil "notifysize" angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





