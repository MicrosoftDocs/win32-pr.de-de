---
description: Ein Alias für uint16 t, der mit einer 16-Bit-Gleitkommazahl gepackt ist, die aus einem Vorzeichenbit, einem \_ 5-Bit-Exponenten und einer 10-Bit-Mantisse besteht.
ms.assetid: E84E0EBA-5C34-41AA-84DB-7A65EBDCAD15
title: HALF-Datentyp (DirectXPackedVector.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b7288324ae5935a23e67a35f402ab6041da55073915d812b39096cab30733
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985040"
---
# <a name="half-data-type"></a>HALF-Datentyp

Ein Alias für **uint16 \_ t** gepackt mit einer 16-Bit-Gleitkommazahl, die aus einem Vorzeichenbit, einem 5-Bit-Exponenten und einer 10-Bit-Mantisse besteht.


```C++
typedef uint16_t HALF;
```



## <a name="remarks"></a>Hinweise

Der HALF-Datentyp entspricht dem FORMAT IEEE 754 binary16.

HALF \_ MIN = 6,10352e-5f

HALF \_ MAX = 65504.f

Weitere Informationen zum HALF-Datentyp finden Sie unter [Gleitkommaformat mit halber Genauigkeit.](https://en.wikipedia.org/wiki/Half_precision_floating-point_format)

**Namespace:** DirectX::P ackedVector verwenden

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DirectXPackedVector.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectXMath-Bibliothekstypen](ovw-xnamath-reference-types.md)
</dt> </dl>

 

 




