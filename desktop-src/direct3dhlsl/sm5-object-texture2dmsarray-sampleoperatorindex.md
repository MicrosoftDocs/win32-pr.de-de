---
title: Texture2DMSArray::sample. Operatorfunktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture2DMSArray::sample. Operatorfunktion
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: 09ac18e7830dfe6b18718deed56e8495ba476dcedcb8290eab4e16aa0d7f24fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508325"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray::sample. Operatorfunktion

Gibt eine schreibgeschützte Ressourcenvariable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
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

Typ: **uint3**

Die Indexposition. Die erste und zweite Komponente enthalten die Koordinaten (x, y). Die dritte Komponente gibt den gewünschten Arrayslice an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture2DMSArray<float4, 4> alpha;

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

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




