---
title: AsDouble-Funktion
description: Interpretiert einen Umwandlungs Wert (2 32-Bit-Werte) in einen Double-Wert um.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- AsDouble-Funktion HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038141"
---
# <a name="asdouble-function"></a>AsDouble-Funktion

Interpretiert einen Umwandlungs Wert (2 32-Bit-Werte) in einen Double-Wert um.

## <a name="syntax"></a>Syntax

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*lowbits* \[ in\]
</dt> <dd>

Typ: **uint**

Das niedrige 32-Bit-Muster des Eingabe Werts.

</dd> <dt>

*highbits* \[ in\]
</dt> <dd>

Typ: **uint**

Das High 32-Bit-Muster des Eingabe Werts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Double**

Die Eingabe (2 32-Bit-Werte) wird als Double-Wert umgewandelt.

## <a name="remarks"></a>Bemerkungen

Außerdem ist die folgende überladene Version verfügbar:

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Wenn der Eingabe Wert 2 32-Bit-Komponenten ist, enthält der Rückgabetyp einen Double-Wert. Wenn der Eingabe Wert 4 32-Bit-Komponenten ist, enthält der Rückgabetyp zwei Double-Werte. Wenn der Eingabe Wert ein 64-Bit-Typ ist, hat der zurückgegebene Wert die gleiche Anzahl von Komponenten wie der Eingabe Wert.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




