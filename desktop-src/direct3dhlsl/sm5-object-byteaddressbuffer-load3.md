---
title: 'Byteaddressbuffer:: Load3 (uint)-Funktion'
description: 'Ruft drei Werte ab. | Byteaddressbuffer:: Load3 (uint)-Funktion'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3-Funktion (HLSL)
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981929"
---
# <a name="byteaddressbufferload3uint-function"></a>Byteaddressbuffer:: Load3 (uint)-Funktion

Ruft drei Werte ab.

## <a name="syntax"></a>Syntax

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Adresse* \[ in\]
</dt> <dd>

Typ: **uint**

Die Eingabe Adresse in Byte, bei der es sich um ein Vielfaches von 4 handeln muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint3**

Drei Werte.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load3-Methoden](byteaddressbuffer-load3.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




