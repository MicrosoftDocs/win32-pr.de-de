---
title: RWBuffer::GetDimensions-Funktion
description: Ruft die Länge des Puffers ab. | RWBuffer::GetDimensions-Funktion
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 586f266fea0dbc035e8ff3a61e39cb18a7102d792ee05c44345a1b702cc1b574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118240"
---
# <a name="rwbuffergetdimensions-function"></a>RWBuffer::GetDimensions-Funktion

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

Nichts

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Rwbuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




