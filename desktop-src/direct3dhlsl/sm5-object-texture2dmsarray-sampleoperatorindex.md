---
title: 'Texture2DMSArray:: Sample. Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture2DMSArray:: Sample. Operator-Funktion'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
keywords:
- Blutprobe. Operator Function HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982005"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray:: Sample. Operator-Funktion

Gibt eine schreibgeschützte Ressourcen Variable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*sampleslice* \[ in\]
</dt> <dd>

Typ: **uint**

Der Beispiel-Slice-Index.

</dd> <dt>

*POS* \[ in\]
</dt> <dd>

Typ: **uint3**

Die Indexposition. Die erste und die zweite Komponente enthalten die (x, y)-Koordinaten. Die dritte Komponente gibt den gewünschten Array Slice an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




