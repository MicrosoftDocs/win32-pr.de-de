---
title: MCIWNDM_PLAYTO (Vfw.h)
description: Die MCIWNDM PLAYTO-Nachricht gibt den Inhalt eines MCI-Geräts von der aktuellen Position bis zum angegebenen Endspeicherort oder so lange wieder, bis die Wiedergabe durch einen anderen \_ Befehl beendet wird.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO von Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61004706c8dfacb05ad47c6ddf261ac813d58f5076dfdd4e134896b3f8c646e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037940"
---
# <a name="mciwndm_playto-message"></a>MCIWNDM \_ PLAYTO-Nachricht

Die **MCIWNDM \_ PLAYTO-Nachricht** gibt den Inhalt eines MCI-Geräts von der aktuellen Position bis zum angegebenen Endspeicherort oder so lange wieder, bis die Wiedergabe durch einen anderen Befehl beendet wird. Wenn sich die angegebene Endposition hinter dem Ende des Inhalts befindet, wird die Wiedergabe am Ende des Inhalts beendet. Sie können diese Nachricht explizit oder mithilfe des [**MCIWndPlayTo-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) senden.


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Verleihen*
</dt> <dd>

Endposition. Die Einheiten für die Endposition hängen vom aktuellen Zeitformat ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Dieses Makro wird mithilfe der [**Makros MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) und [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) definiert, die wiederum den [MCI \_ SEEK-Befehl](mci-seek.md) und die **MCIWNDM \_ PLAYTO-Nachricht** verwenden.

Sie können auch mithilfe des [**MCIWndPlayFromTo-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) sowohl einen Start- als auch einen Endort für die Wiedergabe angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI \_ SEEK](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





