---
title: Texture2DArray::GatherCmpGreen(S,float,float,int2,int2,int2,int2)-Funktion
description: Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück. | Texture2DArray::GatherCmpGreen(S,float,float,int2,int2,int2,int2)-Funktion
ms.assetid: 5A4B8AEB-B278-4456-893A-CAE61BFD6CA5
keywords:
- GatherCmpGreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e45997d3238038d3260594b5e568ca628f170af73dbabf7e382dddb2587dbb4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507363"
---
# <a name="texture2darraygathercmpgreensfloatfloatint2int2int2int2-function"></a>Texture2DArray::GatherCmpGreen(S,float,float,int2,int2,int2,int2)-Funktion

Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpGreen(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Typ: **SamplerState**

Der nullbasierte Samplerindex.

</dd> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **float**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*CompareValue* \[ In\]
</dt> <dd>

Typ: **float**

Ein -Wert, der mit jedem Stichprobenwert verglichen werden soll.

</dd> <dt>

*Offset1* \[ In\]
</dt> <dd>

Typ: **int2**

Die erste Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset2* \[ In\]
</dt> <dd>

Typ: **int2**

Die zweite Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset3* \[ In\]
</dt> <dd>

Typ: **int2**

Die dritte Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset4* \[ In\]
</dt> <dd>

Typ: **int2**

Die vierte Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **TemplateType**

Ein Wert mit vier Komponenten, dessen Typ mit dem Vorlagentyp identisch ist.

## <a name="remarks"></a>Hinweise

Die Texturbeispiele können für die bilineare Interpolation verwendet werden.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GatherCmpGreen-Methoden](texture2darray-gathercmpgreen.md)
</dt> </dl>

 

 




