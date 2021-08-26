---
description: Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungsstruktur.
ms.assetid: ''
title: TraceRay-Funktion
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: 4e22a26d7bd2fd91029c106133667bce98c163d90d99f0700dac7f2bdf0796fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027980"
---
# <a name="traceray-function"></a>TraceRay-Funktion

Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungsstruktur.

## <a name="syntax"></a>Syntax
Diese systeminterne Funktionsdefinition entspricht der folgenden Funktionsvorlage:

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a>Parameter

`AccelerationStructure`

Die zu verwendende Beschleunigungsstruktur der obersten Ebene. Das Angeben einer NULL-Beschleunigungsstruktur erzwingt einen Fehlfehler.

`RayFlags`

Gültige Kombination von [ray_flag](ray_flag.md) Werten. Nur definierte Rayflags werden vom System weitergegeben, d. h. sie sind für den intrinsischen [RayFlags-Shader](rayflags.md) sichtbar.

`InstanceInclusionMask`

Eine ganze Zahl ohne Vorzeichen, deren unterste 8 Bits verwendet werden, um geometry-Instanzen basierend auf der InstanceMask in jeder Instanz einzuschließen oder abzulehnen. Beispiel:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Eine ganze Zahl ohne Vorzeichen, die den Offset angibt, der in Adressierungsberechnungen in Shadertabellen für die Treffergruppenindizierung hinzugefügt werden soll.  Es werden nur die unteren 4 Bits dieses Werts verwendet.

`MultiplierForGeometryContributionToHitGroupIndex`

Eine ganze Zahl ohne Vorzeichen, die den Schritt angibt, der mit *GeometryContributionToHitGroupIndex* multipliziert werden soll. Dies ist nur der 0-basierte Index, den die Geometrie von der App in ihre Beschleunigungsstruktur auf der unteren Ebene bereitgestellt hat. Es werden nur die untersten 16 Bits dieses Multiplikatorwerts verwendet.

`MissShaderIndex`

Eine ganze Zahl ohne Vorzeichen, die den Index des fehlenden Shaders innerhalb einer Shadertabelle angibt.

`Ray`

Ein [**RayDesc,**](raydesc.md) der den zu verfolgenden Strahl darstellt.

`Payload`

Eine benutzerdefinierte Raynutzlast, auf die sowohl für die Eingabe als auch für die Ausgabe durch Shader zugegriffen wird, die während des Raytracings aufgerufen werden.  Nach Abschluss von [**TraceRay**](traceray-function.md) kann der Aufrufer auch auf die Nutzlast zugreifen.

## <a name="return-value"></a>Rückgabewert

**void**

## <a name="remarks"></a>Hinweise

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




