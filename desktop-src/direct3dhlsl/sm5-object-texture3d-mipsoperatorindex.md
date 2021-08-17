---
title: Texture3D::mips. Operatorfunktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture3D::mips. Operatorfunktion
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
keywords:
- Mips. Operatorfunktion HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18ad563041c8ad0b601240f4353dad5bbc44ef418c267f72d07f0f753d12d993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724500"
---
# <a name="texture3dmipsoperator----function"></a>Texture3D::mips. Operatorfunktion

Gibt eine schreibgeschützte Ressourcenvariable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*mipSlice* \[ In\]
</dt> <dd>

Typ: **uint**

Der Index des Mipslices.

</dd> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint3**

Die Indexposition. Enthält die Koordinaten (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




