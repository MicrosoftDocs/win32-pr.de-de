---
title: Texture1DArray::mips. Operatorfunktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture1DArray::mips. Operatorfunktion
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
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
ms.openlocfilehash: f1c4397f60c03968d7c8dba034865aa283a50e8d70b9836aaee86cb910d612ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905321"
---
# <a name="texture1darraymipsoperator----function"></a>Texture1DArray::mips. Operatorfunktion

Gibt eine schreibgeschützte Ressourcenvariable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*mipSlice* \[ In\]
</dt> <dd>

Typ: **uint**

Der MIP-Sliceindex.

</dd> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint2**

Die Indexposition. Die erste Komponente enthält die x-Koordinate. Die zweite Komponente gibt den gewünschten Arrayslice an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




