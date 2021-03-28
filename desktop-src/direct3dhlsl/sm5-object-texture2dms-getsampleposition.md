---
title: 'Texture2DMS:: getsampleposition-Funktion'
description: Gibt die Beispiel Position für den bereitgestellten Beispiel Index zurück.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
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
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517324"
---
# <a name="texture2dmsgetsampleposition-function"></a>Texture2DMS:: getsampleposition-Funktion

Gibt die Beispiel Position für den bereitgestellten Beispiel Index zurück.

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

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
