---
title: Evaluateattributesnapped-Funktion
description: Wertet den Pixel Schwerpunkt mit einem Offset aus.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- Evaluateattributesnapped-Funktion HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992895"
---
# <a name="evaluateattributesnapped-function"></a>Evaluateattributesnapped-Funktion

Wertet den Pixel Schwerpunkt mit einem Offset aus.

## <a name="syntax"></a>Syntax

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Type: **atzb numeric**

Der Eingabewert.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Typ: **int2**

Ein 2D-Offset aus dem Pixel Center unter Verwendung eines 16x16-Rasters.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Bereich für den *Offset* -Parameter muss durch den folgenden Bytecode definiert werden.

Es werden nur die am wenigsten wichtigen 4 Bits der ersten beiden Komponenten (U, V) des Pixel Offsets verwendet. Die Konvertierung des 4-Bit-Fixpunkts in float ist wie folgt (MSB... LSB), wobei MSB Teil des Bruchteils ist und das Vorzeichen bestimmt:

-   1000 =-0,5 f (-8/16)
-   1001 =-0.4375 f (-7/16)
-   1010 =-0,375 f (-6/16)
-   1011 =-0.3125 f (-5/16)
-   1100 =-0,25 f (-4/16)
-   1101 =-0.1875 f (-3/16)
-   1110 =-0,125 f (-2/16)
-   1111 =-0.0625 f (-1/16)
-   0000 = 0,0 f (0/16)
-   0001 = 0.0625 f (1/16)
-   0010 = 0,125 f (2/16)
-   0011 = 0.1875 f (3/16)
-   0100 = 0,25 f (4/16)
-   0101 = 0.3125 f (5/16)
-   0110 = 0,375 f (6/16)
-   0111 = 0.4375 f (7/16)

> [!Note]  
> Der linke und obere Rand eines Pixels sind im Offset enthalten. die unteren und rechten Ränder werden jedoch nicht eingeschlossen. Alle anderen Bits in der 32-Bit-Ganzzahl von Werten für Werte und V-Offset werden ignoriert.

 

Eine-Implementierung kann den vom Shader bereitgestellten Offset annehmen und einen vollständigen 32-Bit-fest Komma Wert (28,4) abrufen, der den gültigen Bereich umfasst, indem die folgende Berechnung durchgeführt wird:


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



Wenn eine Implementierung den Offset einem Gleit Komma Offset zuordnen muss, wird die folgende Berechnung durchführt:


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




