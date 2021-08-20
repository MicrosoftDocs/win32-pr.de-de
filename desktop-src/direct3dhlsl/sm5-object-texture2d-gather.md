---
title: Texture2D::Gather(S,float,int)-Funktion
description: Gibt die vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden. | Texture2D::Gather(S,float,int)-Funktion
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
keywords:
- Gather-Funktion HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 263c3672f55e2f461d9a6c160a60b8222ddeda32ec239b846680d30af0f7fedc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853280"
---
# <a name="texture2dgathersfloatint-function"></a>Texture2D::Gather(S,float,int)-Funktion

Gibt die vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.

## <a name="syntax"></a>Syntax

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **sampler**

Der nullbasierte Samplerindex.

</dd> <dt>

*location* \[ In\]
</dt> <dd>

Typ: **float2**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*offset* \[ In\]
</dt> <dd>

Typ: **int2**

Der Offset, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird.

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

[Gather-Methoden](texture2d-gather.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




