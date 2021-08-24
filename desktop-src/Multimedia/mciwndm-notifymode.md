---
title: MCIWNDM_NOTIFYMODE (Vfw.h)
description: Die MCIWNDM NOTIFYMODE-Meldung benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich der Betriebsmodus des \_ MCI-Geräts geändert hat.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE von Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c610904512e2b39a5c0f16781c1d9f27155f7826941aebfc66fcd9259f7ee8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525420"
---
# <a name="mciwndm_notifymode-message"></a>MCIWNDM \_ NOTIFYMODE-Nachricht

Die **MCIWNDM \_ NOTIFYMODE-Meldung** benachrichtigt das übergeordnete Fenster einer Anwendung, dass sich der Betriebsmodus des MCI-Geräts geändert hat.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle für das MCIWnd-Fenster.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Modus*
</dt> <dd>

Ganze Zahl, die dem MCI-Modus entspricht.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können die Benachrichtigung über Modusänderungen eines MCI-Geräts aktivieren, indem Sie den MCIWNDF \_ NOTIFYMODE-Fensterstil angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





