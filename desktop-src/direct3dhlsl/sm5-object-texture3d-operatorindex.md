---
title: Texture3D::Operator-Funktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture3D::Operator-Funktion
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
keywords:
- Operatorfunktion HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d701e5f9ba46d17c305fda0a936700e10a1348440e55c913537f2a2d00a5c57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985700"
---
# <a name="texture3doperator--function"></a>Texture3D::Operator-Funktion

Gibt eine schreibgeschützte Ressourcenvariable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint3**

Die Indexposition. Enthält die Koordinaten (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Methode greift immer auf die erste MIP-Ebene zu. Verwenden Sie stattdessen den [**\[ \] \[ \] mip.operator,**](sm5-object-texture3d-mipsoperatorindex.md) um andere MIP-Ebenen anzugeben.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




