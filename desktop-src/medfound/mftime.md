---
description: Definiert Einheiten von 100 Nanosekunden.
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: Mftime (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e82c99c3c4a42b652c04595d086951c3c1a71a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361323"
---
# <a name="mftime"></a>MF-Zeit

Definiert Einheiten von 100 Nanosekunden.


```C++
typedef LONGLONG MFTIME;
```



## <a name="examples"></a>Beispiele


```C++
const MFTIME ONE_SECOND = 10000000; // One second.
const LONG   ONE_MSEC = 1000;       // One millisecond

// Convert 100-nanosecond units to milliseconds.

inline LONG MFTimeToMsec(const LONGLONG& time)
{
    return (LONG)(time / (ONE_SECOND / ONE_MSEC));
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Datatypes](media-foundation-datatypes.md)
</dt> </dl>

 

 




