---
title: MCIWNDM_SETPALETTE Meldung (VFW. h)
description: Die mciwndm- \_ SetPalette-Nachricht sendet ein Palettenhandle an das MCI-Gerät, das dem mciwnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des mciwndsetpalette-Makros senden.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477829"
---
# <a name="mciwndm_setpalette-message"></a>Mciwndm- \_ SetPalette-Nachricht

Die **mciwndm- \_ SetPalette** -Nachricht sendet ein Palettenhandle an das MCI-Gerät, das dem mciwnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**mciwndsetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) -Makros senden.


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*hpal*
</dt> <dd>

Palettenhandle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndsetpalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





