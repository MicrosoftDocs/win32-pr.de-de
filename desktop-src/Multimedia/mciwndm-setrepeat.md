---
title: MCIWNDM_SETREPEAT (Vfw.h)
description: Die MCIWNDM SETREPEAT-Meldung legt das Wiederholungsflag fest, \_ das der kontinuierlichen Wiedergabe zugeordnet ist.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT-Nachricht Windows Multimedia
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
ms.openlocfilehash: 158e0b52f01431886fd8a70e89efadfdd7335258c0808cdb6780bf06071e3280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807590"
---
# <a name="mciwndm_setrepeat-message"></a>MCIWNDM \_ SETREPEAT-Meldung

Die **MCIWNDM \_ SETREPEAT-Meldung** legt das Wiederholungsflag fest, das der kontinuierlichen Wiedergabe zugeordnet ist. Die **MCIWNDM \_ SETREPEAT-Nachricht** funktioniert in Verbindung mit dem [MCI \_ PLAY-Befehl,](mci-play.md) um eine kontinuierliche Wiedergabeschleife zu ermöglichen. Sie können diese Nachricht explizit oder mithilfe des [**Makros MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) senden.


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Neuer Zustand des Wiederholungsflags. Geben Sie **TRUE an,** um die fortlaufende Wiedergabe zu aktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Derzeit ist MCIAVI das einzige Gerät, das fortlaufende Wiedergabe unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI \_ PLAY](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





