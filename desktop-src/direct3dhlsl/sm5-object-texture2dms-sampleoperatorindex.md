---
title: Texture2DMS::sample. Operatorfunktion
description: Ruft einen Wert aus der Ressource am angegebenen Speicherort und Beispielindex ab. | Texture2DMS::sample. Operatorfunktion
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- Beispiel. Operatorfunktion HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5d7082ee72c49d3aa4be131491151b1bab65502e6fe85884b2a03573c497b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508472"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS::sample. Operatorfunktion

Ruft einen Wert aus der Ressource am angegebenen Speicherort und Beispielindex ab.

## <a name="syntax"></a>Syntax

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*sampleSlice* \[ In\]
</dt> <dd>

Typ: **uint**

Der Beispielsliceindex.

</dd> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint2**

Die Indexposition. Die Komponenten enthalten die Koordinaten (x, y).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




