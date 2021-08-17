---
title: Texture2D::mips. Operatorfunktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture2D::mips. Operatorfunktion
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 0d8c915c340e69eedc8b66a1665b6e600c0134b66cb6cd81fe6b803681e5fdeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789496"
---
# <a name="texture2dmipsoperator----function"></a>Texture2D::mips. Operatorfunktion

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

Der Index des Mipslices.

</dd> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint2**

Die Indexposition. Enthält die Koordinaten (x, y).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

### <a name="usage-example"></a>Verwendungsbeispiel


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




