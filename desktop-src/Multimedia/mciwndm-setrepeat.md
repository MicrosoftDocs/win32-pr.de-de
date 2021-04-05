---
title: MCIWNDM_SETREPEAT Meldung (VFW. h)
description: Die mciwndm \_ SetRepeat-Nachricht legt das wiederholungsflag fest, das der kontinuierlichen Wiedergabe zugeordnet ist.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859064"
---
# <a name="mciwndm_setrepeat-message"></a>Mciwndm- \_ Nachricht

Die **mciwndm \_ SetRepeat** -Nachricht legt das wiederholungsflag fest, das der kontinuierlichen Wiedergabe zugeordnet ist. Die **mciwndm \_** -Nachricht "" wird zusammen mit dem Befehl " [MCI \_ Play](mci-play.md) " verwendet, um eine fortlaufende Wiedergabe Schleife bereitzustellen. Sie können diese Nachricht explizit oder mit dem [**mciwndltrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) -Makro senden.


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*c*
</dt> <dd>

Neuer Zustand des Wiederholungs Flags. Geben Sie **true** an, um die kontinuierliche Wiedergabe zu aktivieren

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="remarks"></a>Bemerkungen

Derzeit ist MCIAVI das einzige Gerät, das die fortlaufende Wiedergabe unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI- \_ Play](mci-play.md)
</dt> <dt>

[**Mciwndgtrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





