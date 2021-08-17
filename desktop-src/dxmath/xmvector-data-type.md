---
description: Ein portabler Typ, der einen Vektor von vier 32-Bit-Gleitkomma- oder Ganzzahlkomponenten darstellt, die jeweils optimal ausgerichtet und einem Hardwarevektorregister zugeordnet sind.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: XMVECTOR-Datentyp (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0a65c7da346163c3cbfaab7c68982f56eb6c424b7f74a3ec01c754eb4104a5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094480"
---
# <a name="xmvector-data-type"></a>XMVECTOR-Datentyp

Ein portabler Typ, der einen Vektor von vier 32-Bit-Gleitkomma- oder Ganzzahlkomponenten darstellt, die jeweils optimal ausgerichtet und einem Hardwarevektorregister zugeordnet sind.

## <a name="remarks"></a>Hinweise

Eine Liste der zusätzlichen Funktionen, z. B. Konstruktoren und Operatoren, die bei der Programmierung in C++ zur Verfügung stehen, finden Sie `XMVECTOR` unter [XMVECTOR-Erweiterungen](ovw-xmvector-extensions.md).

In der DirectXMath-Bibliothek ist zur vollständigen Unterstützung von Portabilität und Optimierung standardmäßig ein `XMVECTOR` nicht transparenter Typ. Die tatsächliche Implementierung von `XMVECTOR` ist plattformabhängig.

Im Allgemeinen sollte code nicht auf den Besonderheiten einer bestimmten plattformspezifischen Implementierung von `XMVECTOR` basieren. Plattformspezifische Implementierungen haben die folgenden Merkmale:

-   Sie sind nicht portabel.
-   Sie können sich zwischen Releases ändern.
-   Die uneinstige Verwendung von Implementierungsdetails kann suboptimal sein.

Entwickler sollten die [Accessorfunktionen](ovw-xnamath-reference-functions-accessors.md)der DirectXMath [](ovw-xnamath-reference-functions-storage.md) Library [verwenden,](ovw-xnamath-reference-functions-load.md)laden und speichern, um die Vektoren zu erhalten und zu legen, und die [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) verwenden, um sie zu bearbeiten.

Informationen zu Projekten, die ausführliche Informationen zur Implementierung auf verschiedenen Plattformen benötigen, finden `XMVECTOR` Sie unter [Bibliotheksinternes](pg-xnamath-internals.md).

### <a name="compiler-aliases"></a>Compileraliase

Die DirectXMath.h-Headerdatei verwendet Aliase für das -Objekt, insbesondere `XMVECTOR` **CXMVECTOR** und **FXMVECTOR.** Der Header verwendet diese Aliase, um den optimalen In-Line-Aufrufkonventionen verschiedener Compiler zu entsprechen. Für die meisten Projekte, die DirectXMath verwenden, ist es ausreichend, diese Typen als genauen Alias für zu `XMVECTOR` behandeln.

Beispiel:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Informationen zu Projekten, die detaillierte Informationen dazu benötigen, wie verschiedene Plattformen ihre Aufrufkonventionen behandeln, finden Sie unter [Bibliotheksinternes](pg-xnamath-internals.md).

Für XNAMATH 2.x verfügt der Datentyp über Elementelemente vom Typ `XMVECTOR` .x, .y, .z, .and .w, die in der Regel eine schlechte Leistung verursachen. Die Verwendung des XM STRICT VECTOR4-Typs ermöglicht die Verwendung der \_ \_ DirectXMath-Definition eines nicht transparenten Datentyps.

**Namespace:** DirectX verwenden

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

[**XMVECTORF32-Datentyp**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTORU32-Datentyp**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8-Datentyp**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTOR-Datentyp**](xmvector-data-type.md)
</dt> </dl>

 

 




