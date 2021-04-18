---
title: 'Texture2D:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben. | Texture2D:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion'
ms.assetid: C8325626-F281-4D10-9299-0E5DA01BB1BD
keywords:
- Gathercmpalpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5095fdb83814ab8c7d52add0fba05cbbf876678
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981849"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2-function"></a>Texture2D:: gathercmpalpha (S, float, float, int2, int2, int2, int2)-Funktion

Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpAlpha(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Typ: **samplerstate**

Der null basierte samplerindex.

</dd> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **float**

Die Beispiel Koordinaten (u, v).

</dd> <dt>

*CompareValue* \[ in\]
</dt> <dd>

Typ: **float**

Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.

</dd> <dt>

*Offset1* \[ in\]
</dt> <dd>

Typ: **int2**

Die erste Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset2* \[ in\]
</dt> <dd>

Typ: **int2**

Die zweite Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset3* \[ in\]
</dt> <dd>

Typ: **int2**

Die dritte Offset Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset4* \[ in\]
</dt> <dd>

Typ: **int2**

Die vierte Offset-Komponente, die vor dem Sampling auf die Texturkoordinaten angewendet wird.

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

[Gathercmpalpha-Methoden](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 




