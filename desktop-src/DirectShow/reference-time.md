---
description: Der Verweis \_ Zeit-Datentyp definiert die Einheiten für Verweis Zeiten in DirectShow. Jede Einheit der Verweis Zeit beträgt 100 Nanosekunden.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME ("strinmif. h")
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373960"
---
# <a name="reference_time"></a>Verweis \_ Zeit

Der **Verweis \_ Zeit** -Datentyp definiert die Einheiten für Verweis Zeiten in DirectShow. Jede Einheit der Verweis Zeit beträgt 100 Nanosekunden.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Bemerkungen

Der **Verweis \_ Zeit** -Datentyp ist eine ganze Zahl mit 64 Bit.

Verweis Zeiten werden normalerweise von einer der folgenden Baselines gemessen:

-   Eine absolute Uhrzeitangabe. In diesem Fall hängt die Baseline von der Implementierung der Uhr ab. Weitere Informationen finden Sie unter [Referenzuhren](reference-clocks.md).
-   Relativ zum Anfang der Wiedergabe.

Weitere Informationen zu Referenz Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Strinmif. h" (Include DShow. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Datentypen](directshow-data-types.md)
</dt> </dl>

 

 




