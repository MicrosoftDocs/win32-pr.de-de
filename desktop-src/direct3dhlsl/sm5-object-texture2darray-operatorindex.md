---
title: Texture2DArray::Operator-Funktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture2DArray::Operator-Funktion
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 752b037cfc5d7c6e7ecc008aec6c45bb05356170b9b7154abca87f01fa146f55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095040"
---
# <a name="texture2darrayoperator--function"></a>Texture2DArray::Operator-Funktion

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

Die Indexposition. Die erste und die zweite Komponente enthalten die Koordinaten (x, y). Die dritte Komponente gibt den gewünschten Arrayslice an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Methode greift immer auf die erste MIP-Ebene zu. Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen die [**\[ \] \[ \] mip.operator-Methode.**](sm5-object-texture2darray-mipsoperatorindex.md)

Die Texturbeispiele können für die bilineare Interpolation verwendet werden.

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

 

 




