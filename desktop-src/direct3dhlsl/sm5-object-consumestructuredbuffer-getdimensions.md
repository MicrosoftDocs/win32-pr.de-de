---
title: ConsumeStructuredBuffer::GetDimensions-Funktion
description: Ruft die Ressourcendimensionen ab. | ConsumeStructuredBuffer::GetDimensions-Funktion
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: 5cc7c7c9234d00343f91a3fcb137eed65b95515a07f765cf8fce6893e2d4998a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788390"
---
# <a name="consumestructuredbuffergetdimensions-function"></a>ConsumeStructuredBuffer::GetDimensions-Funktion

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

Der Schritt jedes Elements in Bytes.

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

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




