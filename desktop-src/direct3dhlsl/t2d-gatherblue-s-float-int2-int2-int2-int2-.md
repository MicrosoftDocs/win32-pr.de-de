---
title: Texture2D::GatherBlue(S,float,int2,int2,int2,int2)-Funktion
description: Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden. | Texture2D::GatherBlue(S,float,int2,int2,int2,int2)-Funktion
ms.assetid: 0FFD3D82-E849-4C19-BEBC-85B9CCA40CA0
keywords:
- GatherBlue-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d71f166a6e4ea205a8d2e41579e3907576314ce93aaf14cbc926b86e2cbe09e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507756"
---
# <a name="gatherbluesfloatint2int2int2int2-function"></a>GatherBlue(S,float,int2,int2,int2,int2)-Funktion

Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherBlue(
  in SamplerState S,
  in float        Location,
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

[GatherBlue-Methoden](texture2d-gatherblue.md)
</dt> </dl>

 

 




