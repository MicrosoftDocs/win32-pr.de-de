---
title: RWByteAddressBuffer::GetDimensions-Funktion
description: Ruft die Länge des Puffers ab. | RWByteAddressBuffer::GetDimensions-Funktion
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 2271f563251cfdb9c6f2a2174c91dc8c271c7354a2b10b9b2e7e55cb4af09d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725145"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a>RWByteAddressBuffer::GetDimensions-Funktion

Ruft die Länge des Puffers ab.

## <a name="syntax"></a>Syntax

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Dim* \[ out\]
</dt> <dd>

Typ: **uint**

Die Länge des Puffers in Bytes.

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

 

 




