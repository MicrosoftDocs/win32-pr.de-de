---
title: Texture2DArray::GatherAlpha(S,float,int,uint)-Funktion
description: Gibt die vier Texelwerte zurück, die in einem bilinealen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden. | Texture2DArray::GatherAlpha(S,float,int,uint)-Funktion
ms.assetid: B04F29A7-0EC9-49F0-9662-00F1DD0F3E5B
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
ms.openlocfilehash: 6efa67eb0f2e3eed33f18788443723fadce825a381511019dcc24d941656865c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788290"
---
# <a name="texture2darraygatheralphasfloatintuint-function"></a>Texture2DArray::GatherAlpha(S,float,int,uint)-Funktion

Gibt die vier Texelwerte zurück, die in einem bilinealen Filtervorgang zusammen mit dem Kachelzuordnungsstatus verwendet werden.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
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

*Offset* \[ In\]
</dt> <dd>

Typ: **int**

Der Offset, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

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

[GatherAlpha-Methoden](texture2darray-gatheralpha.md)
</dt> </dl>

 

 
