---
description: Ein nicht transparenter, portabler Typ zur Unterstützung der Verwendung der C/C++-Initialisierersyntax zum Laden von uint8 \_ t-Werten in eine Instanz des XMVECTOR-Typs.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: XMVECTORU8-Datentyp (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3c335df3e74bc58776883b15d724c65d558bad30fc37e0e28547102260301a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276196"
---
# <a name="xmvectoru8-data-type"></a>XMVECTORU8-Datentyp

Ein nicht transparenter, portabler Typ zur Unterstützung der Verwendung der C/C++-Initialisierersyntax zum Laden von uint8 \_ t-Werten in eine Instanz des [**XMVECTOR-Typs.**](xmvector-data-type.md)


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>Hinweise

Eine Liste zusätzlicher Funktionen wie Konstruktoren und Operatoren, die bei der Programmierung in C++ mit XMVECTORU8 verfügbar sind, finden Sie unter [XMVECTORU8-Erweiterungen.](ovw-xmvectoru8-extensions.md)

Die [**XMVECTORF32-,**](xmvectorf32-data-type.md) [**XMVECTORU32-,**](xmvectoru32-data-type.md) [**XMVECTORI32-**](xmvectori32-data-type.md)und **XMVECTORU8-Strukturen** werden als Mechanismus zum Erstellen von [**XMVECTOR**](xmvector-data-type.md) aus verschiedenen konstanten Datentypen (Gleitkomma, ganze Zahl ohne Vorzeichen, Integer und Byte) mit initialisierern bereitgestellt.

Dies ist aus Gründen der Portabilität und Optimierung erforderlich, um [**XMVECTOR**](xmvector-data-type.md)zu unterstützen, da es selbst keine Initialisierer unterstützt.

Beispiel:

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**Namespace:** Verwenden von DirectX

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectXMath-Bibliothekstypen](ovw-xnamath-reference-types.md)
</dt> <dt>

[**XMVECTOR-Datentyp**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTORI32-Datentyp**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTORU32-Datentyp**](xmvectoru32-data-type.md)
</dt> <dt>

[XMVECTORU8-Erweiterungen](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




