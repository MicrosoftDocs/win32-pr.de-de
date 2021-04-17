---
title: 'Texturecubearray:: gathercmpred (S, float, float, uint)-Funktion'
description: 'Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück. | Texturecubearray:: gathercmpred (S, float, float, uint)-Funktion'
ms.assetid: 2474ECF6-DA85-406F-8212-D71AD90730FD
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
ms.openlocfilehash: b64c32a5525faf3484715871b4fc0c4fb6470886
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352648"
---
# <a name="texturecubearraygathercmpredsfloatfloatuint-function"></a>Texturecubearray:: gathercmpred (S, float, float, uint)-Funktion

Für vier Texel-Werte, die in einem bilinearen Filter Vorgang verwendet werden, gibt einen Vergleich der roten Komponente mit einem Vergleichswert zusammen mit dem Status der Kachel Zuordnung zurück.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

[Gathercmpred-Methoden](texturecubearray-gathercmpred.md)
</dt> <dt>

[**Texturecubearray**](texturecubearray.md)
</dt> </dl>

 

 
