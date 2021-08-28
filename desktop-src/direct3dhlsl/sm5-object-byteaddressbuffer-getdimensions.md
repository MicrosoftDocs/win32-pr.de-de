---
title: ByteAddressBuffer::GetDimensions-Funktion
description: Ruft die Länge des Puffers ab. | ByteAddressBuffer::GetDimensions-Funktion
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 398b5a6dba995a11dcf4ce8a78fecee9bb185ce98ec285453bdd52c1180a4eb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067720"
---
# <a name="byteaddressbuffergetdimensions-function"></a>ByteAddressBuffer::GetDimensions-Funktion

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
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ByteAddressBuffer](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




