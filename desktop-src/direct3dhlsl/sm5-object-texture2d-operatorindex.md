---
title: 'Texture2D:: Operator-Funktion'
description: 'Gibt eine schreibgeschützte Ressourcen Variable zurück. | Texture2D:: Operator-Funktion'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981704"
---
# <a name="texture2doperator--function"></a>Texture2D:: Operator-Funktion

Gibt eine schreibgeschützte Ressourcen Variable zurück.

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*POS* \[ in\]
</dt> <dd>

Typ: **uint2**

Die Indexposition. Enthält die (x, y)-Koordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcen Variable.

## <a name="remarks"></a>Bemerkungen

Diese Methode greift immer auf die erste MIP-Ebene zu. Um andere MIP-Ebenen anzugeben, verwenden Sie stattdessen die [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2d-mipsoperatorindex.md) -Methode.

Die Textur Beispiele können für bilineare Interpolationen verwendet werden.

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




