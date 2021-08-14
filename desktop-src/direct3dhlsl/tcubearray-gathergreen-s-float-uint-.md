---
title: TextureCubeArray::GatherGreen(S,float,uint)-Funktion
description: Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden. | TextureCubeArray::GatherGreen(S,float,uint)-Funktion
ms.assetid: 0DEB1810-F2C7-4097-B2D3-20ED4E297561
keywords:
- GatherGreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 872e1df390dda30739881d9f221f5d6c63bbfbca311a1f07c3d94eac8c4d43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506499"
---
# <a name="texturecubearraygathergreensfloatuint-function"></a>TextureCubeArray::GatherGreen(S,float,uint)-Funktion

Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
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

[GatherGreen-Methoden](texturecubearray-gathergreen.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
