---
description: Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Uint8 \_ t-Werten in eine Instanz des xmvector-Typs unterstützt.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: XMVECTORU8-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355265"
---
# <a name="xmvectoru8-data-type"></a>XMVECTORU8-Datentyp

Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Uint8 \_ t-Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>Bemerkungen

Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die mit XMVECTORU8 bei der Programmierung in C++ verfügbar sind, finden Sie unter [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).

Die [**XMVECTORF32**](xmvectorf32-data-type.md)-, [**XMVECTORU32**](xmvectoru32-data-type.md)-, [**XMVECTORI32**](xmvectori32-data-type.md)-und **XMVECTORU8** -Strukturen werden als Mechanismus zur Erstellung von [**xmvector**](xmvector-data-type.md) aus unterschiedlichen Konstanten Datentypen (Gleit Komma Zahl, Ganzzahl ohne Vorzeichen, Ganzzahl und Byte) mithilfe von Initialisierern bereitgestellt.

Dies ist für die Unterstützung von [**xmvector**](xmvector-data-type.md)erforderlich, da Initialisierer aus Gründen der Portabilität und Optimierung nicht selbst unterstützt werden.

Beispiel:

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**Namespace**: Verwenden von DirectX

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Directxmath. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Directxmath-Bibliothekstypen](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Xmvector-Datentyp**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTORI32-Datentyp**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTORU32-Datentyp**](xmvectoru32-data-type.md)
</dt> <dt>

[XMVECTORU8-Erweiterungen](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




