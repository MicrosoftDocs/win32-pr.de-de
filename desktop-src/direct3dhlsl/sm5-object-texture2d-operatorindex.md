---
title: Texture2D::Operator-Funktion
description: Gibt eine schreibgeschützte Ressourcenvariable zurück. | Texture2D::Operator-Funktion
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 99323f1dcf212fc42c413a4be8231aa22acbd00cf3f40b408e3f9f5eca59f578
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095070"
---
# <a name="texture2doperator--function"></a>Texture2D::Operator-Funktion

Gibt eine schreibgeschützte Ressourcenvariable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint2**

Die Indexposition. Enthält die Koordinaten (x, y).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Methode greift immer auf die erste MIP-Ebene zu. Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen die [**\[ \] \[ \] mip.operator-Methode.**](sm5-object-texture2d-mipsoperatorindex.md)

Die Texturbeispiele können für die bilineare Interpolation verwendet werden.

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

 

 




