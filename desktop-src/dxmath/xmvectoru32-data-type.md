---
description: Ein nicht transparenter, portabler Typ zur Unterstützung der Verwendung der C/C++-Initialisierersyntax zum Laden von uint32 t-Werten in eine Instanz des \_ XMVECTOR-Typs.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: XMVECTORU32-Datentyp (Directxmath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13d37a5630df37021637bed978943a48a665db16301f2067c82f050a8231bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891680"
---
# <a name="xmvectoru32-data-type"></a>XMVECTORU32-Datentyp

Ein nicht transparenter, portabler Typ zur Unterstützung der Verwendung der C/C++-Initialisierersyntax zum Laden von uint32 t-Werten in eine Instanz des \_ [**XMVECTOR-Typs.**](xmvector-data-type.md)


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a>Hinweise

Eine Liste der zusätzlichen Funktionen, z. B. Konstruktoren und Operatoren, die bei der Programmierung in C++ mit XMVECTORU32 verfügbar sind, finden Sie unter [XMVECTORU32-Erweiterungen](ovw-xmvectoru32-extensions.md).

Die [**XMVECTORF32-,**](xmvectorf32-data-type.md) **XMVECTORU32-,** [**XMVECTORI32-**](xmvectori32-data-type.md)und [**XMVECTORU8-Strukturen**](xmvectoru8-data-type.md) werden als Mechanismus zum Erstellen von [**XMVECTOR**](xmvector-data-type.md) aus verschiedenen konstanten Datentypen (Gleitkomma, ganze Zahl ohne Vorzeichen, ganze Zahl und Byte) unter Verwendung von Initialisierern bereitgestellt.

Dies ist erforderlich, um [**XMVECTOR**](xmvector-data-type.md)zu unterstützen, da es selbst aus Gründen der Portabilität und Optimierung keine Initialisierer unterstützt.

Beispiel:

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

**Namespace:** DirectX verwenden

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Directxmath.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectXMath-Bibliothekstypen](ovw-xnamath-reference-types.md)
</dt> <dt>

[**XMVECTORI32-Datentyp**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTOR-Datentyp**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORU8-Datentyp**](xmvectoru8-data-type.md)
</dt> <dt>

[XMVECTORU32-Erweiterungen](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




