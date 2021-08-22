---
title: EvaluateAttributeSnapped-Funktion
description: Wertet am Pixelschwerpunkt mit einem Offset aus.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- EvaluateAttributeSnapped-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5408b2c8133947b948bc42eb6ff0c725584b0cf2c60ccf0731a9d584d3c898a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512017"
---
# <a name="evaluateattributesnapped-function"></a>EvaluateAttributeSnapped-Funktion

Wertet am Pixelschwerpunkt mit einem Offset aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **attrib numeric**

Der Eingabewert.

</dd> <dt>

*offset* \[ In\]
</dt> <dd>

Typ: **int2**

Ein 2D-Offset vom Pixelmittelpunkt unter Verwendung eines 16x16-Rasters.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Bereich für den *offset-Parameter* muss durch den folgenden Bytecode definiert werden.

Es werden nur die am wenigsten signifikanten 4 Bits der ersten beiden Komponenten (U, V) des Pixeloffsets verwendet. Die Konvertierung vom 4-Bit-Festpunkt in float ist wie folgt (MSB... LSB), wobei msb ein Teil des Bruchs ist und das Vorzeichen bestimmt:

-   1000 = -0,5f (-8 / 16)
-   1001 = -0,4375f (-7 / 16)
-   1010 = -0,375f (-6 / 16)
-   1011 = -0,3125f (-5 / 16)
-   1100 = -0,25f (-4 / 16)
-   1101 = -0,1875f (-3 / 16)
-   1110 = -0,125f (-2 / 16)
-   1111 = -0,0625f (-1 / 16)
-   0000 = 0,0f ( 0 / 16)
-   0001 = 0,0625f ( 1 / 16)
-   0010 = 0,125f ( 2 / 16)
-   0011 = 0,1875f ( 3 / 16)
-   0100 = 0,25f ( 4 / 16)
-   0101 = 0,3125f ( 5 / 16)
-   0110 = 0,375f ( 6 / 16)
-   0111 = 0,4375f ( 7 / 16)

> [!Note]  
> Die linken und oberen Ränder eines Pixels sind im Offset enthalten. der untere und rechte Rand sind jedoch nicht enthalten. Alle anderen Bits in der 32-Bit-Ganzzahl, die Sie und V-Offsetwerte haben, werden ignoriert.

 

Eine Implementierung kann den vom Shader bereitgestellten Offset verwenden und einen vollständigen festen 32-Bit-Punktwert (28,4) abrufen, der den gültigen Bereich umfasst, indem die folgende Berechnung erfolgt:


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Wenn eine Implementierung den Offset einem Gleitkommaoffset zuordnen muss, führt sie die folgende Berechnung aus:


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




