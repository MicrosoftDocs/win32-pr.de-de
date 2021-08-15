---
title: ByteAddressBuffer::Load4(uint)-Funktion
description: Ruft vier Werte ab. | ByteAddressBuffer::Load4(uint)-Funktion
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
keywords:
- Load4-Funktion HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a623c62ce9038d4e06cfbb952808aeb0530cb2e937c83578d9ef0e71c9b0a038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510000"
---
# <a name="byteaddressbufferload4uint-function"></a>ByteAddressBuffer::Load4(uint)-Funktion

Ruft vier Werte ab.

## <a name="syntax"></a>Syntax

``` syntax
uint4 Load4(
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

Typ: **uint4**

Vier Werte.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Load4-Methoden](byteaddressbuffer-load4.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




