---
title: MCIWNDM_GETSTYLES Meldung (VFW. h)
description: Die mciwndm \_ getStyles-Nachricht Ruft die Flags ab, die die aktuellen, von einem Fenster verwendeten mciwnd-Fenster Stile angeben. Sie können diese Nachricht explizit oder mit dem mciwndgetstyles-Makro senden.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342661"
---
# <a name="mciwndm_getstyles-message"></a>Mciwndm \_ getStyles-Nachricht

Die **mciwndm \_ getStyles** -Nachricht Ruft die Flags ab, die die aktuellen, von einem Fenster verwendeten mciwnd-Fenster Stile angeben. Sie können diese Nachricht explizit oder mit dem [**mciwndgetstyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) -Makro senden.


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der die aktuellen Stile des mciwnd-Fensters darstellt. Der Rückgabewert ist der bitweise OR-Operator der mciwnd-Fenster Stile (mciwndf-Flags).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgetstyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





