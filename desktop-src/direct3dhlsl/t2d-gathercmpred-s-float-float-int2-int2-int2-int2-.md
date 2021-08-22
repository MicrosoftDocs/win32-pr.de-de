---
title: Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2)-Funktion
description: Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück. | Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2)-Funktion
ms.assetid: B20A766E-0B4F-4FBA-A691-70ACE7BECF33
keywords:
- GatherCmpRed-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f5314fb143d8607a66402ca2b27fdf4902ffb08646d55b6fed0702c0979c8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507607"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2-function"></a>Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2)-Funktion

Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpRed(
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



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GatherCmpRed-Methoden](texture2d-gathercmpred.md)
</dt> </dl>

 

 




