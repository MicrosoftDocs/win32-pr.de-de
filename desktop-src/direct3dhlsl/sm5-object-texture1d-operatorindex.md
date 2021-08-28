---
title: Texture1D::Operator-Funktion
description: Gibt eine schreibgeschützte Ressourcenvariable für eine Texture1D zurück.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: d2c11ef313531adb9b129ffb99103ea6c7778462eddf8c1c76f4b235c92951c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985910"
---
# <a name="texture1doperator--function"></a>Texture1D::Operator-Funktion

Gibt eine schreibgeschützte Ressourcenvariable für eine [**Texture1D zurück.**](sm5-object-texture1d.md)

## <a name="syntax"></a>Syntax

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* \[ In\]
</dt> <dd>

Typ: **uint**

Die Indexposition. Enthält die x-Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **R**

Eine schreibgeschützte Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Methode greifen immer auf die erste MIP-Ebene zu. Verwenden Sie stattdessen den [**mip.operator, \[ \] \[ \]**](sm5-object-texture1d-mipsoperatorindex.md) um andere MIP-Ebenen anzugeben.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




