---
title: Texture2DArray::mips. Operatorfunktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture2DArray::mips. Operatorfunktion
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
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
ms.openlocfilehash: f5dff48f721e45ef7853c125b1d7d0d32d5cb311a3dbc3b31d4100f3038a8fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724591"
---
# <a name="texture2darraymipsoperator----function"></a>Texture2DArray::mips. Operatorfunktion

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

Die Indexposition. Die erste und die zweite Komponente enthalten die Koordinaten (x, y). Die dritte Komponente gibt den gewünschten Arrayslice an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




