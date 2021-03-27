---
title: 'Texture2DArray:: gathergreen (S, float, int)-Funktion'
description: 'Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden. | Texture2DArray:: gathergreen (S, float, int)-Funktion'
ms.assetid: bfe9ab9f-64f7-4a50-aa46-2ec6effebce2
keywords:
- Gathergreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48a5d968ffe5eeb12fdb0240d1823a9b1834ae19
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219134"
---
# <a name="texture2darraygathergreensfloatint-function"></a>Texture2DArray:: gathergreen (S, float, int)-Funktion

Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.

## <a name="syntax"></a>Syntax

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **Sampler**

Der null basierte samplerindex.

</dd> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **float3**

Die Beispiel Koordinaten (u, v).

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Typ: **int2**

Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: **TemplateType**

Ein vier komponentenwert, dessen Typ mit dem Vorlagentyp identisch ist.

## <a name="remarks"></a>Bemerkungen

Die Textur Beispiele können für bilineare Interpolationen verwendet werden.

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Gathergreen-Methoden](texture2darray-gathergreen.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




