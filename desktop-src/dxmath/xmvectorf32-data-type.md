---
description: Ein nicht transparenter, portabler Typ zur Unterstützung der Verwendung der C/C++-Initialisierersyntax zum Laden von Gleitkommawerten in eine Instanz des XMVECTOR-Typs.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: XMVECTORF32-Datentyp (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1a39de246e3e0e4ab9a96197dbe4a286cb6ecabe327d60e5c506795af79dd11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739780"
---
# <a name="xmvectorf32-data-type"></a>XMVECTORF32-Datentyp

Ein nicht transparenter, portabler Typ zur Unterstützung der Verwendung der C/C++-Initialisierersyntax zum Laden von Gleitkommawerten in eine Instanz des [**XMVECTOR-Typs.**](xmvector-data-type.md)


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Hinweise

Eine Liste zusätzlicher Funktionen wie Konstruktoren und Operatoren, die bei der Programmierung in C++ verfügbar `XMVECTORF32` sind, finden Sie unter [XMVECTORF32-Erweiterungen.](ovw-xmvectorf32-extensions.md)

Die **XMVECTORF32-,** [**XMVECTORU32-,**](xmvectoru32-data-type.md) [**XMVECTORI32-**](xmvectori32-data-type.md)und [**XMVECTORU8-Strukturen**](xmvectoru8-data-type.md) werden als Mechanismus zum Erstellen von [**XMVECTOR**](xmvector-data-type.md) aus verschiedenen konstanten Datentypen (Gleitkomma, ganze Zahl ohne Vorzeichen, Integer und Byte) mit initialisierern bereitgestellt.

Dies ist aus Gründen der Portabilität und Optimierung erforderlich, um [**XMVECTOR**](xmvector-data-type.md)zu unterstützen, da es selbst keine Initialisierer unterstützt.

Beispiel:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
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

[**XMVECTORI32-Datentyp**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTOR-Datentyp**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORU32-Datentyp**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8-Datentyp**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




