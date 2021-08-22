---
title: RWTexture2DArray::Operator-Funktion
description: Gibt eine Ressourcenvariable zurück. | RWTexture2DArray::Operator-Funktion
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: 8650b4aed51915591438501fb2c929b846e5be1d4de1219017ec1eb45980d552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985920"
---
# <a name="rwtexture2darrayoperator--function"></a>RWTexture2DArray::Operator-Funktion

Gibt eine Ressourcenvariable zurück.

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

Eine Ressourcenvariable.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[RWTexture2DArray](sm5-object-rwtexture2darray.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




