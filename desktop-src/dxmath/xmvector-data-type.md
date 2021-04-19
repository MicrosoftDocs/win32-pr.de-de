---
description: Ein portabler Typ, der zum Darstellen eines Vektors von Gleit Komma-oder ganzzahligen 4 32-Bit-Komponenten verwendet wird, die jeweils optimal ausgerichtet und einem Hardware Vektor Register zugeordnet sind.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Xmvector-Datentyp (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361284"
---
# <a name="xmvector-data-type"></a>Xmvector-Datentyp

Ein portabler Typ, der zum Darstellen eines Vektors von Gleit Komma-oder ganzzahligen 4 32-Bit-Komponenten verwendet wird, die jeweils optimal ausgerichtet und einem Hardware Vektor Register zugeordnet sind.

## <a name="remarks"></a>Bemerkungen

Eine Liste der zusätzlichen Funktionen, wie z. b. Konstruktoren und Operatoren, die `XMVECTOR` beim Programmieren in C++ verfügbar sind, finden Sie unter [xmvector Extensions](ovw-xmvector-extensions.md).

In der directxmath-Bibliothek ist ein nicht transparenter Typ, um Portabilität und Optimierung vollständig zu unterstützen `XMVECTOR` . Die tatsächliche Implementierung von `XMVECTOR` ist plattformabhängig.

Im Allgemeinen sollte Code nicht auf die Besonderheiten einer bestimmten plattformspezifischen Implementierung von beruhen `XMVECTOR` . Plattformspezifische Implementierungen haben folgende Merkmale:

-   Sie sind nicht portabel.
-   Sie können sich zwischen Releases ändern.
-   Die Verletzung der Verwendung von Implementierungsdetails ist möglicherweise suboptimal.

Entwickler sollten die Funktionen " [Accessor](ovw-xnamath-reference-functions-accessors.md)", " [Load](ovw-xnamath-reference-functions-load.md)" und " [Store](ovw-xnamath-reference-functions-storage.md) " der directxmath-Bibliothek verwenden, um die Vektoren zu erhalten und festzulegen, und die [Bibliotheks-4D-Vektor Funktionen der directxmath-Bibliothek](ovw-xnamath-reference-functions-vector4.md) .

Informationen zu-Projekten, die ausführliche Informationen zur Implementierung `XMVECTOR` von auf verschiedenen Plattformen benötigen, finden Sie unter [Bibliotheks internale](pg-xnamath-internals.md).

### <a name="compiler-aliases"></a>Compileraliase

In der Header Datei "directxmath. h" werden Aliase für das- `XMVECTOR` Objekt verwendet, insbesondere " **cxmvector** " und " **fxmvector**". Der Header verwendet diese Aliase, um die optimalen Inline Aufruf Konventionen verschiedener Compiler einzuhalten. Bei den meisten Projekten, für die directxmath verwendet wird, genügt es, diese Typen als exakten Alias für zu behandeln `XMVECTOR` .

Beispiel:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Informationen zu-Projekten, die ausführliche Informationen dazu benötigen, wie verschiedene Plattformen ihre Aufruf Konventionen verarbeiten, finden Sie unter [Bibliotheks](pg-xnamath-internals.md)interne Informationen.

Bei xnamath 2. x hat der `XMVECTOR` Datentyp die Member. x,. y,. z,. und. w, was im Allgemeinen zu einer schlechten Leistung führt. Die Verwendung des XM \_ Strict \_ VECTOR4-Typs bietet ein Opt-in der directxmath-Definition eines nicht transparenten Datentyps.

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

[**XMVECTORU32-Datentyp**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8-Datentyp**](xmvectoru8-data-type.md)
</dt> <dt>

[**Xmvector-Datentyp**](xmvector-data-type.md)
</dt> </dl>

 

 




