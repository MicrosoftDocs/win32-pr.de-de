---
description: Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungs Struktur.
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
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106355728"
---
# <a name="traceray-function"></a>TraceRay-Funktion

Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungs Struktur.

## <a name="syntax"></a>Syntax
Diese intrinsische Funktionsdefinition entspricht der folgenden Funktions Vorlage:

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

Die zu verwendende Beschleunigungs Struktur auf oberster Ebene. Die Angabe einer NULL-Beschleunigungs Struktur erzwingt einen Fehler.

`RayFlags`

Gültige Kombination von [ray_flag](ray_flag.md) Werten. Nur definierte Ray-Flags werden vom System weitergegeben, d. h., Sie sind für den systeminternen [rayflags](rayflags.md) -Shader sichtbar.

`InstanceInclusionMask`

Eine ganze Zahl ohne Vorzeichen, von der die unteren 8 Bits verwendet werden, um geometry-Instanzen auf der Grundlage von instancemask in jeder Instanz einzubeziehen oder abzulehnen. Beispiel:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Eine ganze Zahl ohne Vorzeichen, die den Offset angibt, der zur Adressierung von Berechnungen in shadertabellen für die Treffer Gruppen Indizierung hinzugefügt  Nur die untersten 4 Bits dieses Werts werden verwendet.

`MultiplierForGeometryContributionToHitGroupIndex`

Eine Ganzzahl ohne Vorzeichen, die den Schritt angibt, der von *geometrycontributiontohitgroupindex* multipliziert werden soll. Hierbei handelt es sich nur um den 0-basierten Index, den die Geometrie von der app in der Struktur der untersten Beschleunigung bereitgestellt hat. Es werden nur die untersten 16 Bits dieses Multiplikator-Werts verwendet.

`MissShaderIndex`

Eine ganze Zahl ohne Vorzeichen, die den Index des fehlshaders innerhalb einer shadertabelle angibt.

`Ray`

Ein [**raydebug**](raydesc.md) -Objekt, das den zu über mittelenden Strahl darstellt.

`Payload`

Eine benutzerdefinierte Strahl Nutzlast, auf die sowohl für die Eingabe als auch für die Ausgabe durch Shader zugegriffen wird, die während der Raytracing  Nachdem [**traceray**](traceray-function.md) abgeschlossen ist, kann der Aufrufer auch auf die Nutzlast zugreifen.

## <a name="return-value"></a>Rückgabewert

**void**

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




