---
title: TextureCubeArray::GatherCmpAlpha(S,float,float,uint)-Funktion
description: Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zusammen mit dem Kachelzuordnungsstatus zurück. | TextureCubeArray::GatherCmpAlpha(S,float,float,uint)-Funktion
ms.assetid: EA1D7176-3F70-4867-9854-80206A871B23
keywords:
- GatherCmpAlpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f462b11b406920d1fce99592fdef00fd6c15ba08c50b35f818d68650a97b923
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723413"
---
# <a name="texturecubearraygathercmpalphasfloatfloatuint-function"></a>TextureCubeArray::GatherCmpAlpha(S,float,float,uint)-Funktion

Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zusammen mit dem Kachelzuordnungsstatus zurück.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpAlpha(
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

Typ: **SamplerState**

Der nullbasierte Samplerindex.

</dd> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **float**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*CompareValue* \[ In\]
</dt> <dd>

Typ: **float**

Ein -Wert, der mit jedem Stichprobenwert verglichen werden soll.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die systeminterne [**CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE** zurück, wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte aus einer nicht zugeordneten Kachel stammen, gibt **CheckAccessFullyMapped** **FALSE** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **TemplateType**

Ein Wert mit vier Komponenten, dessen Typ mit dem Vorlagentyp identisch ist.

## <a name="remarks"></a>Hinweise

Die Texturbeispiele können für die bilineare Interpolation verwendet werden.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GatherCmpAlpha-Methoden](texturecubearray-gathercmpalpha.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
