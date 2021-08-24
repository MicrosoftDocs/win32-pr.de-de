---
description: Der REFERENCE \_ TIME-Datentyp definiert die Einheiten für Verweiszeiten in DirectShow. Jede Einheit der Referenzzeit beträgt 100 Nanosekunden.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f1600e820ac59c53144743933701a61e4a7b753f814dde06c5c663a760938d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747320"
---
# <a name="reference_time"></a>\_REFERENZZEIT

Der **REFERENCE \_ TIME-Datentyp** definiert die Einheiten für Verweiszeiten in DirectShow. Jede Einheit der Referenzzeit beträgt 100 Nanosekunden.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Hinweise

Der **REFERENCE \_ TIME-Datentyp** ist eine 64-Bit-Ganzzahl.

Referenzzeiten werden in der Regel anhand einer der folgenden Baselines gemessen:

-   Eine absolute Uhrzeit. In diesem Fall hängt die Baseline von der Implementierung der Uhr ab. Weitere Informationen finden Sie unter [Referenzuhren.](reference-clocks.md)
-   Relativ zum Beginn der Wiedergabe.

Weitere Informationen zu Referenzzeiten finden Sie unter [Uhrzeit und Uhren in DirectShow.](time-and-clocks-in-directshow.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Strmif.h (include Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Datentypen](directshow-data-types.md)
</dt> </dl>

 

 




