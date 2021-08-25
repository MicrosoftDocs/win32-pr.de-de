---
title: ByteAddressBuffer::Load3(uint)-Funktion
description: Ruft drei Werte ab. | ByteAddressBuffer::Load3(uint)-Funktion
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3-Funktion HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bd36958eb2c16d45e6228c9919cb22bb772c8861131c26710fff032276bce6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510010"
---
# <a name="byteaddressbufferload3uint-function"></a>ByteAddressBuffer::Load3(uint)-Funktion

Ruft drei Werte ab.

## <a name="syntax"></a>Syntax

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*address* \[ In\]
</dt> <dd>

Typ: **uint**

Die Eingabeadresse in Bytes, die ein Vielfaches von 4 sein muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint3**

Drei Werte.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Load3-Methoden](byteaddressbuffer-load3.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




