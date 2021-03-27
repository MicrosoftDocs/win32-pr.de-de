---
title: 'Appendstructuredbuffer:: GetDimensions-Funktion'
description: 'Ruft die Ressourcen Dimensionen ab. | Appendstructuredbuffer:: GetDimensions-Funktion'
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
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981096"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>Appendstructuredbuffer:: GetDimensions-Funktion

Ruft die Ressourcen Dimensionen ab.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*numstructs* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Die Anzahl der Strukturen.

</dd> <dt>

*Stride* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Die Anzahl der Bytes in jedem Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Appendstructuredbuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




