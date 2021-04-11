---
title: MCIWNDM_CAN_WINDOW Meldung (VFW. h)
description: Die Meldung "mciwndm \_ kann \_ ein Fenster" bestimmt, ob ein MCI-Gerät Fenster orientierte MCI-Befehle unterstützt. Sie können diese Nachricht explizit oder mithilfe des mciwndcanwindow-Makros senden.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- MCIWNDM_CAN_WINDOW-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949756"
---
# <a name="mciwndm_can_window-message"></a>Mciwndm \_ kann \_ Nachricht Fenster

Die Meldung " **mciwndm \_ kann ein \_ Fenster** " bestimmt, ob ein MCI-Gerät Fenster orientierte MCI-Befehle unterstützt. Sie können diese Nachricht explizit oder mithilfe des [**mciwndcanwindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) -Makros senden.


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn das Gerät Fenster orientierte MCI-Befehle unterstützt, andernfalls " **false** ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndcanwindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





