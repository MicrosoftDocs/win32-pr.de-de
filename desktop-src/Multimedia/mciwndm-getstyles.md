---
title: MCIWNDM_GETSTYLES Nachricht (Vfw.h)
description: Die MCIWNDM \_ GETSTYLES-Nachricht ruft die Flags ab, die die aktuellen MCIWnd-Fensterstile angeben, die von einem Fenster verwendet werden. Sie können diese Nachricht explizit oder mithilfe des MCIWndGetStyles-Makros senden.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES nachricht Windows Multimedia
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
ms.openlocfilehash: 036bd687c5d7828fade23994b9141488354added5ee38d38bafc9c5ce22a954c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783290"
---
# <a name="mciwndm_getstyles-message"></a>MCIWNDM \_ GETSTYLES-Nachricht

Die **MCIWNDM \_ GETSTYLES-Nachricht** ruft die Flags ab, die die aktuellen MCIWnd-Fensterstile angeben, die von einem Fenster verwendet werden. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndGetStyles-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) senden.


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der die aktuellen Stile des MCIWnd-Fensters darstellt. Der Rückgabewert ist der bitweise OR-Operator der MCIWnd-Fensterstile (MCIWNDF-Flags).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





