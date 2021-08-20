---
title: Texture2D::GatherRed(S,float,int)-Funktion
description: Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück. | Texture2D::GatherRed(S,float,int)-Funktion
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- GatherRed-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 879ba1cdad400a065fae46bd858db5569390ae0ae2a2ad338bfb9faed62bbdca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508639"
---
# <a name="texture2dgatherredsfloatint-function"></a>Texture2D::GatherRed(S,float,int)-Funktion

Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
TemplateType GatherRed(
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



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GatherRed-Methoden](texture2d-gatherred.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




