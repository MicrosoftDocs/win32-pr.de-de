---
description: Ein nicht transparenter, portabler Typ, der die Verwendung der C/C++-Initialisierersyntax unterstützt, um ganzzahlige Werte in eine Instanz des XMVECTOR-Typs zu laden.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: XMVECTORI32-Datentyp (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4bb03dffb4c77575aab8c2a2680ecd821fea627f49325c6748ede607ef81f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739759"
---
# <a name="xmvectori32-data-type"></a>XMVECTORI32-Datentyp

Ein nicht transparenter, portabler Typ, der die Verwendung der C/C++-Initialisierersyntax unterstützt, um ganzzahlige Werte in eine Instanz des [**XMVECTOR-Typs**](xmvector-data-type.md) zu laden.


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a>Hinweise

Eine Liste der zusätzlichen Funktionen, z. B. Konstruktoren und Operatoren, die bei der Programmierung in C++ verfügbar `XMVECTORI32` sind, finden Sie unter [XMVECTORI32-Erweiterungen.](ovw-xmvectori32-extensions.md)

Die [**XMVECTORF32-,**](xmvectorf32-data-type.md) [**XMVECTORU32-,**](xmvectoru32-data-type.md) **XMVECTORI32-** und [**XMVECTORU8-Strukturen**](xmvectoru8-data-type.md) werden als Mechanismus zum Erstellen von [**XMVECTOR**](xmvector-data-type.md) aus verschiedenen konstanten Datentypen (Gleitkomma, ganze Zahl ohne Vorzeichen, Integer und Byte) mit initialisierern bereitgestellt.

Dies ist aus Gründen der Portabilität und Optimierung erforderlich, um [**XMVECTOR**](xmvector-data-type.md)zu unterstützen, da es selbst keine Initialisierer unterstützt.

Beispiel:


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



**Namespace:** Verwenden von DirectX

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectXMath-Bibliothekstypen](ovw-xnamath-reference-types.md)
</dt> <dt>

[**XMVECTOR-Datentyp**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTORU32-Datentyp**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8-Datentyp**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTORI32-Datentyp**](xmvectori32-data-type.md)
</dt> </dl>

 

 




