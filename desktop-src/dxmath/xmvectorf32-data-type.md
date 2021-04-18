---
description: Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Gleit Komma Werten in eine Instanz des xmvector-Typs unterstützt.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: XMVECTORF32-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365484"
---
# <a name="xmvectorf32-data-type"></a>XMVECTORF32-Datentyp

Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Gleit Komma Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Bemerkungen

Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die `XMVECTORF32` beim Programmieren in C++ verfügbar sind, finden Sie unter [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).

Die **XMVECTORF32**-, [**XMVECTORU32**](xmvectoru32-data-type.md)-, [**XMVECTORI32**](xmvectori32-data-type.md)-und [**XMVECTORU8**](xmvectoru8-data-type.md) -Strukturen werden als Mechanismus zur Erstellung von [**xmvector**](xmvector-data-type.md) aus unterschiedlichen Konstanten Datentypen (Gleit Komma Zahl, Ganzzahl ohne Vorzeichen, Ganzzahl und Byte) mithilfe von Initialisierern bereitgestellt.

Dies ist für die Unterstützung von [**xmvector**](xmvector-data-type.md)erforderlich, da Initialisierer aus Gründen der Portabilität und Optimierung nicht selbst unterstützt werden.

Beispiel:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
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

[**XMVECTORI32-Datentyp**](xmvectori32-data-type.md)
</dt> <dt>

[**Xmvector-Datentyp**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORU32-Datentyp**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8-Datentyp**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




