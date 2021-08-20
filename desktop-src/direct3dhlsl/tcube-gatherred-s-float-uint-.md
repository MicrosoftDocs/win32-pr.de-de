---
title: TextureCube::GatherRed(S,float,uint)-Funktion
description: Gibt die roten Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden. | TextureCube::GatherRed(S,float,uint)-Funktion
ms.assetid: 6B298DFD-B996-40F4-9304-AA8283FDEC31
keywords:
- GatherRed-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3a1566ae6ab68a313bea8defa411ea08ca88c773ccc6ebb74a09c8351fb5f40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723423"
---
# <a name="texturecubegatherredsfloatuint-function"></a>TextureCube::GatherRed(S,float,uint)-Funktion

Gibt die roten Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherRed(
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

[GatherRed-Methoden](texturecube-gatherred.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
