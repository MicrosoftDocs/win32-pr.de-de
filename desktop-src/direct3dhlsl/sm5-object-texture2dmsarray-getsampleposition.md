---
title: Texture2DMSArray::GetSamplePosition-Funktion
description: Ruft die Position des angegebenen Beispiels ab. | Texture2DMSArray::GetSamplePosition-Funktion
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- GetSamplePosition-Funktion HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9da6727120dcb19d9dd51c83d62f85d842036edb2197d33e298259480b248642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508416"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Texture2DMSArray::GetSamplePosition-Funktion

Ruft die Position des angegebenen Beispiels ab.

## <a name="syntax"></a>Syntax

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*sampleindex* \[ In\]
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Der nullbasierte Index einer Beispielposition.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float2**

Ein Beispielspeicherort.

## <a name="remarks"></a>Hinweise

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
