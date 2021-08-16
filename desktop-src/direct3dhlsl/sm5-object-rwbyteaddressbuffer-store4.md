---
title: RWByteAddressBuffer::Store4-Funktion
description: Legt vier Werte fest.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Store4-Funktion HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc644647616f6c6654023be23aaa8e420dbb85ad439547d1befd44c0ea7b210c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789971"
---
# <a name="store4-function"></a>Store4-Funktion

Legt vier Werte fest.

## <a name="syntax"></a>Syntax

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Adresse* \[ In\]
</dt> <dd>

Typ: **uint**

Die Eingabeadresse in Bytes, die ein Vielfaches von 4 sein muss.

</dd> <dt>

*-Werte* \[ In\]
</dt> <dd>

Typ: **uint4**

Vier Eingabewerte.

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

 

 




