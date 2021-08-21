---
title: TextureCube::GatherCmpBlue(S,float,float,uint)-Funktion
description: Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zusammen mit dem Kachelzuordnungsstatus zurück. | TextureCube::GatherCmpBlue(S,float,float,uint)-Funktion
ms.assetid: 1D1FFF0E-9CA7-48A4-A305-C0B6059056E7
keywords:
- GatherCmpBlue-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 986ccd5811e41467fdafa4d1da47e2241ca4e63c5a18cc9d99290ae3a806a999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043368"
---
# <a name="texturecubegathercmpbluesfloatfloatuint-function"></a>TextureCube::GatherCmpBlue(S,float,float,uint)-Funktion

Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zusammen mit dem Kachelzuordnungsstatus zurück.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpBlue(
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

Ein -Wert, der jeweils mit jedem stichprobenentnahmen Wert verglichen werden soll.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die [**systeminterne CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE zurück,** wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource zugegriffen haben.](/windows/desktop/direct3d11/direct3d-11-2-features) Wenn Werte aus einer nicht zugeordneten Kachel übernommen wurden, gibt **CheckAccessFullyMapped** **FALSE zurück.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **TemplateType**

Ein Wert mit vier Komponenten, dessen Typ mit dem Vorlagentyp identisch ist.

## <a name="remarks"></a>Hinweise

Die Texturbeispiele können für die bilineare Interpolation verwendet werden.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GatherCmpBlue-Methoden](texturecube-gathercmpblue.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
