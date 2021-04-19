---
description: Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von UInt32 \_ t-Werten in eine Instanz des xmvector-Typs unterstützt.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: XMVECTORU32-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354222"
---
# <a name="xmvectoru32-data-type"></a>XMVECTORU32-Datentyp

Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von UInt32 \_ t-Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a>Bemerkungen

Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die mit XMVECTORU32 bei der Programmierung in C++ verfügbar sind, finden Sie unter [XMVECTORU32 Extensions](ovw-xmvectoru32-extensions.md).

Die [**XMVECTORF32**](xmvectorf32-data-type.md)-, **XMVECTORU32**-, [**XMVECTORI32**](xmvectori32-data-type.md)-und [**XMVECTORU8**](xmvectoru8-data-type.md) -Strukturen werden als Mechanismus zur Erstellung von [**xmvector**](xmvector-data-type.md) aus unterschiedlichen Konstanten Datentypen (Gleit Komma Zahl, Ganzzahl ohne Vorzeichen, Ganzzahl und Byte) mithilfe von Initialisierern bereitgestellt.

Dies ist für die Unterstützung von [**xmvector**](xmvector-data-type.md)erforderlich, da Initialisierer aus Gründen der Portabilität und Optimierung nicht selbst unterstützt werden.

Beispiel:

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
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

[**XMVECTORI32-Datentyp**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> <dt>

[**Xmvector-Datentyp**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORU8-Datentyp**](xmvectoru8-data-type.md)
</dt> <dt>

[XMVECTORU32-Erweiterungen](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




