---
title: MCIWNDM_SETPALETTE (Vfw.h)
description: Die MCIWNDM SETPALETTE-Nachricht sendet ein Palettenhand handle an das \_ MCI-Gerät, das dem MCIWnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des Makros MCIWndSetPalette senden.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE von Windows Multimedia
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
ms.openlocfilehash: 7b4986224fd23898ef33f8fdda4c12d17880a8bc42441b29cd1865fb7fdfa687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525230"
---
# <a name="mciwndm_setpalette-message"></a>MCIWNDM \_ SETPALETTE-Meldung

Die **MCIWNDM \_ SETPALETTE-Nachricht** sendet ein Palettenhand handle an das MCI-Gerät, das dem MCIWnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) senden.


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*hpal*
</dt> <dd>

Palettenhand handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





