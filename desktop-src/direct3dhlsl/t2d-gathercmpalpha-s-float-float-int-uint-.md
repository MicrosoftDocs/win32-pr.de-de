---
title: Texture2D::GatherCmpAlpha(S,float,float,int,uint)-Funktion
description: Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zusammen mit dem Kachelzuordnungsstatus zurück. | Texture2D::GatherCmpAlpha(S,float,float,int,uint)-Funktion
ms.assetid: 4E281512-2E0A-49A5-B568-8CE793A854F9
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
ms.openlocfilehash: e5d4cc054d832bcaea7987fda26f8c000a7c6c2bbfe5e2f13366a99fcddb0e01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671180"
---
# <a name="texture2dgathercmpalphasfloatfloatintuint-function"></a>Texture2D::GatherCmpAlpha(S,float,float,int,uint)-Funktion

Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zusammen mit dem Kachelzuordnungsstatus zurück.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
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

*Offset* \[ In\]
</dt> <dd>

Typ: **int**

Der Offset, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

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



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GatherCmpAlpha-Methoden](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 
