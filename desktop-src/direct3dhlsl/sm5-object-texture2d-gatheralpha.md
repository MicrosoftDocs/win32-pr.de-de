---
title: Texture2D::GatherAlpha(S,float,int)-Funktion
description: Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden. | Texture2D::GatherAlpha(S,float,int)-Funktion
ms.assetid: 4c980e06-d768-479e-bee3-1b2541c23038
keywords:
- GatherAlpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12ea7c643c8e86925163594856980c20aae09d61cd9421d6060449ed80da81f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789825"
---
# <a name="texture2dgatheralphasfloatint-function"></a>Texture2D::GatherAlpha(S,float,int)-Funktion

Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.

## <a name="syntax"></a>Syntax

``` syntax
TemplateType GatherAlpha(
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

*location* \[ In\]
</dt> <dd>

Typ: **float2**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*offset* \[ In\]
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

[GatherAlpha-Methoden](texture2d-gatheralpha.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




