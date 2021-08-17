---
title: RWTexture1D::Operator-Funktion
description: Gibt eine Ressourcenvariable zurück. | RWTexture1D::Operator-Funktion
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: a6f338efd27573a86c661df36f9fc0e9906814bf15c1cc5d2d6c478a17f83a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724851"
---
# <a name="rwtexture1doperator--function"></a>RWTexture1D::Operator-Funktion

Gibt eine Ressourcenvariable zurück.

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

Eine Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




