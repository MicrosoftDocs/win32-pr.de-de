---
title: RWStructuredBuffer::GetDimensions-Funktion
description: Ruft die Ressourcendimensionen ab. | RWStructuredBuffer::GetDimensions-Funktion
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 760a546d7d60afbb41438416a9602ab55981834acd9969bc535c9a82df6e5e50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789926"
---
# <a name="rwstructuredbuffergetdimensions-function"></a>RWStructuredBuffer::GetDimensions-Funktion

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

Die Anzahl der Strukturen in der Ressource.

</dd> <dt>

*stride* \[ out\]
</dt> <dd>

Typ: **uint**

Der Schritt jedes Strukturelements in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nichts

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




