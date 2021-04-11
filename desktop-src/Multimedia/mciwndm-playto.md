---
title: MCIWNDM_PLAYTO Meldung (VFW. h)
description: Die mciwndm \_ playto-Nachricht gibt den Inhalt eines MCI-Geräts von der aktuellen Position bis zur angegebenen Endposition oder bis zur Wiedergabe durch einen anderen Befehl wieder.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO-Nachricht (Multimedia)
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
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105429"
---
# <a name="mciwndm_playto-message"></a>Mciwndm \_ playto-Meldung

Die **mciwndm \_ playto** -Nachricht gibt den Inhalt eines MCI-Geräts von der aktuellen Position bis zur angegebenen Endposition oder bis zur Wiedergabe durch einen anderen Befehl wieder. Wenn die angegebene Endposition hinter dem Ende des Inhalts liegt, wird die Wiedergabe am Ende des Inhalts angehalten. Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) senden.


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*auszu*
</dt> <dd>

Endposition. Die Einheiten für die Endposition hängen vom aktuellen Zeitformat ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Dieses Makro wird mithilfe der Makros " [**mciwndseek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) " und " [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) " definiert, die wiederum den MCI-Befehl " [ \_ Seek](mci-seek.md) " und die **mciwndm- \_ playto** -Nachricht verwenden.

Sie können auch einen Start-und einen endspeicherort für die Wiedergabe angeben, indem Sie das [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) -Makro verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI- \_ Suche](mci-seek.md)
</dt> <dt>

[**Mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**Mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**Mciwndseek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





