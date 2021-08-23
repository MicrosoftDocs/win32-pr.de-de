---
title: RWTexture2D::Operator-Funktion
description: Gibt eine Ressourcenvariable zurück. | RWTexture2D::Operator-Funktion
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
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
ms.openlocfilehash: 4da16a89eb704e924931b8d3b4e5144d7154eed50f298aa0606b9b0fb5a45f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986000"
---
# <a name="rwtexture2doperator--function"></a>RWTexture2D::Operator-Funktion

Gibt eine Ressourcenvariable zurück.

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

Eine Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[RWTexture2D](sm5-object-rwtexture2d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




