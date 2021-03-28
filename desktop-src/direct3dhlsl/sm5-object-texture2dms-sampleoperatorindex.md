---
title: 'Texture2DMS:: Sample. Operator-Funktion'
description: 'Ruft einen Wert aus der Ressource an dem Speicherort und dem angegebenen Beispiel Index ab. | Texture2DMS:: Sample. Operator-Funktion'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
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
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219381"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS:: Sample. Operator-Funktion

Ruft einen Wert aus der Ressource an dem Speicherort und dem angegebenen Beispiel Index ab.

## <a name="syntax"></a>Syntax

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
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

Typ: **uint2**

Die Indexposition. Die-Komponenten enthalten die (x, y)-Koordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture2DMS<float4, 8> tex;

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

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




