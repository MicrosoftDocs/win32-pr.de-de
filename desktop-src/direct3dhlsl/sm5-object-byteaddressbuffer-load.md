---
title: ByteAddressBuffer::Load(int)-Funktion
description: Ruft einen Wert ab. | ByteAddressBuffer::Load(int)-Funktion
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Load-Funktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a9854f85ebd92b9f57e4b2339f374ad8f7816ea7b9ba31e37c9404b08c14864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671450"
---
# <a name="byteaddressbufferloadint-function"></a>ByteAddressBuffer::Load(int)-Funktion

Ruft einen Wert ab.

## <a name="syntax"></a>Syntax

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Adresse* \[ In\]
</dt> <dd>

Typ: **int**

Die Eingabeadresse in Bytes, die ein Vielfaches von 4 sein muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Ein -Wert.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Laden von Methoden](byteaddressbuffer-load.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




