---
title: 'Texture3D:: Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture3D:: Operator-Funktion'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
keywords:
- Operator Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761724"
---
# <a name="texture3doperator--function"></a>Texture3D:: Operator-Funktion

Gibt eine schreibgeschützte Ressourcen Variable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*POS* \[ in\]
</dt> <dd>

Typ: **uint3**

Die Indexposition. Enthält die Koordinaten (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

Diese Methode greift immer auf die erste MIP-Ebene zu. Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen den [**\[ \] \[ \] MIP.-Operator**](sm5-object-texture3d-mipsoperatorindex.md) .

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




