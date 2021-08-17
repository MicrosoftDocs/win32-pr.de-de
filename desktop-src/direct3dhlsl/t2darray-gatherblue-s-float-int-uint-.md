---
title: Texture2DArray::GatherBlue(S,float,int,uint)-Funktion
description: Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden, zusammen mit dem Kachelzuordnungsstatus. | Texture2DArray::GatherBlue(S,float,int,uint)-Funktion
ms.assetid: A0745768-EE92-4036-84F5-2699D26441B3
keywords:
- GatherBlue-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e7af5f6c4f37fd4139e839e5ff6d52bf71b3f1fdda9f72c65e9f0a43e351a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723882"
---
# <a name="texture2darraygatherbluesfloatintuint-function"></a>Texture2DArray::GatherBlue(S,float,int,uint)-Funktion

Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden, zusammen mit dem Kachelzuordnungsstatus.

## <a name="syntax"></a>Syntax


``` syntax
TemplateType GatherBlue(
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



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GatherBlue-Methoden](texture2darray-gatherblue.md)
</dt> </dl>

 

 
