---
title: RWByteAddressBuffer::Store-Funktion
description: Legt einen Wert fest.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Store-Funktion HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be699a28eea213b8847f32a3b66f53739a7db86ee5964bd97559a6d534fff6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724942"
---
# <a name="store-function"></a>Store-Funktion

Legt einen Wert fest.

## <a name="syntax"></a>Syntax

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*address* \[ In\]
</dt> <dd>

Typ: **uint**

Die Eingabeadresse in Bytes, die ein Vielfaches von 4 sein muss.

</dd> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **uint**

Ein Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




