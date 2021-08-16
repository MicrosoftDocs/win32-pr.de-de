---
title: Texture2D::GatherGreen(S,float,int2,int2,int2,int2)-Funktion
description: Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden. | Texture2D::GatherGreen(S,float,int2,int2,int2,int2)-Funktion
ms.assetid: 043434C0-BB12-4A08-A3E5-34C9738DEBDB
keywords:
- GatherGreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d0c7fa8f28a0a0ddc276af696b102df29de1362b948a4a909733cf14df35aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043588"
---
# <a name="texture2dgathergreensfloatint2int2int2int2-function"></a>Texture2D::GatherGreen(S,float,int2,int2,int2,int2)-Funktion

Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherGreen(
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

[GatherGreen-Methoden](texture2d-gathergreen.md)
</dt> </dl>

 

 




