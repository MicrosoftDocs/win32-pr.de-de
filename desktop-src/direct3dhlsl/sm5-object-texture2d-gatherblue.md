---
title: Texture2D::GatherBlue(S,float,int)-Funktion
description: Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden. | Texture2D::GatherBlue(S,float,int)-Funktion
ms.assetid: 6d753ef2-2818-4990-81df-52dda044d21d
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
ms.openlocfilehash: caadf785617ee1e28e2bfffef4d7ccb534bff8d760b982ccc2284920475729a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789815"
---
# <a name="texture2dgatherbluesfloatint-function"></a>Texture2D::GatherBlue(S,float,int)-Funktion

Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.

## <a name="syntax"></a>Syntax

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **sampler**

Der nullbasierte Samplerindex.

</dd> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **float2**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Typ: **int2**

Ein Offset, der vor der Stichprobenentnahme auf die Texturkoordinate angewendet wird.

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
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




