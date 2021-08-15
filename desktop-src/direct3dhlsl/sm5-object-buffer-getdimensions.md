---
title: Buffer::GetDimensions-Funktion
description: Ruft die Länge des Puffers ab. | Buffer::GetDimensions-Funktion
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: d7c56d673e533b4626a57669cf884d80da63d7848cfc7a3e248762f6c4f42088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986100"
---
# <a name="buffergetdimensions-function"></a>Buffer::GetDimensions-Funktion

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



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




