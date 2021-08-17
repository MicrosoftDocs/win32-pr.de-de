---
title: Texture2D::GatherAlpha(S,float,int2,int2,int2,int2,uint)-Funktion
description: Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden. | Texture2D::GatherAlpha(S,float,int2,int2,int2,int2,uint)-Funktion
ms.assetid: C088BC6A-397C-4702-9BFA-0B2F10C833BD
keywords:
- GatherAlpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 349cd761c576514ce031937edbf2bff4544acec18f7196dea06d2bcdca0b4108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724068"
---
# <a name="texture2dgatheralphasfloatint2int2int2int2uint-function"></a>Texture2D::GatherAlpha(S,float,int2,int2,int2,int2,uint)-Funktion

Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
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

Typ: **SamplerState**

Der nullbasierte Samplerindex.

</dd> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **float**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*Offset1* \[ In\]
</dt> <dd>

Typ: **int2**

Die erste Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset2* \[ In\]
</dt> <dd>

Typ: **int2**

Die zweite Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset3* \[ In\]
</dt> <dd>

Typ: **int2**

Die dritte Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

</dd> <dt>

*Offset4* \[ In\]
</dt> <dd>

Typ: **int2**

Die vierte Offsetkomponente, die vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

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



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GatherAlpha-Methoden](texture2d-gatheralpha.md)
</dt> </dl>

 

 
