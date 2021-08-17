---
title: RWByteAddressBuffer::Load2(uint)-Funktion
description: Ruft zwei Werte ab. | RWByteAddressBuffer::Load2(uint)-Funktion
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Load2-Funktion HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f71fd2d0585803fb10de3fddfa29c10838d73e32ba7d63b5619be91b042cb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725057"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>RWByteAddressBuffer::Load2(uint)-Funktion

Ruft zwei Werte ab.

## <a name="syntax"></a>Syntax

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Adresse* \[ In\]
</dt> <dd>

Typ: **uint**

Die Eingabeadresse in Bytes, die ein Vielfaches von 4 sein muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint2**

Zwei Werte.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load2-Methoden](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




