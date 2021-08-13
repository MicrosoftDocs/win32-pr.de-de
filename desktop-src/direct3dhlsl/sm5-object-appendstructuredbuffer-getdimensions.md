---
title: AppendStructuredBuffer::GetDimensions-Funktion
description: Ruft die Ressourcendimensionen ab. | AppendStructuredBuffer::GetDimensions-Funktion
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- GetDimensions-Funktion HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96f40417834b8e23a9e746e4e4e3df93b96c1fc2affc7cd9147842e389dc99d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790651"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>AppendStructuredBuffer::GetDimensions-Funktion

Ruft die Ressourcendimensionen ab.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*numStructs* \[ out\]
</dt> <dd>

Typ: **uint**

Die Anzahl der Strukturen.

</dd> <dt>

*stride* \[ out\]
</dt> <dd>

Typ: **uint**

Die Anzahl der Bytes in jedem Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




