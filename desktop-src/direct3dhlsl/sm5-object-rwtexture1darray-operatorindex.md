---
title: RWTexture1DArray::Operator-Funktion
description: Gibt eine Ressourcenvariable zurück. | RWTexture1DArray::Operator-Funktion
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 2e0735e3d9945d15c2f8473155612a40cbf652349eb531f089f5a4aa44451484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509282"
---
# <a name="rwtexture1darrayoperator--function"></a>RWTexture1DArray::Operator-Funktion

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

Die Indexposition. Die erste Komponente enthält die x-Koordinate. Die zweite Komponente gibt den gewünschten Arrayslice an.

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

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




