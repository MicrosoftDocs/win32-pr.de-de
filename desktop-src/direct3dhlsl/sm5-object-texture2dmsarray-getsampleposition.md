---
title: 'Texture2DMSArray:: getsampleposition-Funktion'
description: 'Ruft die Position des angegebenen Beispiels ab. | Texture2DMSArray:: getsampleposition-Funktion'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- Getsampleposition-Funktion HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219380"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Texture2DMSArray:: getsampleposition-Funktion

Ruft die Position des angegebenen Beispiels ab.

## <a name="syntax"></a>Syntax

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*sampleingedex* \[ in\]
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Der null basierte Index eines Beispiel Speicher Orts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float2**

Ein Beispiel Speicherort.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
