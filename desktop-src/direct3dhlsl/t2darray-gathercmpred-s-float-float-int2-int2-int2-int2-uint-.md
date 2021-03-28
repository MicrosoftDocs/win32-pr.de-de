---
title: 'Texture2DArray:: gathercmpred (S, float, float, int2, int2, int2, int2, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texture2DArray:: gathercmpred (S, float, float, int2, int2, int2, int2, uint)-Funktion'
ms.assetid: E41E1328-AE31-445E-AF01-1DB201E8A278
keywords:
- Gathercmpred-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12c6e3762ed4152d1e75bcb93c67663f92e923b1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981976"
---
# <a name="texture2darraygathercmpredsfloatfloatint2int2int2int2uint-function"></a>Texture2DArray:: gathercmpred (S, float, float, int2, int2, int2, int2, uint)-Funktion

Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
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

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion. **Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.

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

[Gathercmpred-Methoden](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
