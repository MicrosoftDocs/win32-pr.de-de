---
title: Zuordnung zwischen D3D9- und D3D8-Deklarationen
description: Diese Tabelle ordnet Elemente einer D3DVERTEXELEMENT9-Deklaration einer Direct3D 8-Deklaration zu.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e6c94836499a6f2bf5dc4e88c76b822ef3143278581a4020e76dba16c9869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069030"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Zuordnung zwischen D3D9- und D3D8-Deklarationen

Diese Tabelle ordnet Elemente einer [**D3DVERTEXELEMENT9-Deklaration**](d3dvertexelement9.md) einer Direct3D 8-Deklaration zu.



| Direct3D 9-Nutzung           | Direct3D 9-Nutzungsindex | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| D3DDECLUSAGE \_ POSITION     | 0                      | D3DVSDE-POSITION \_     |
| D3DDECLUSAGE \_ POSITION     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ NORMAL       | 0                      | D3DVSDE \_ NORMAL       |
| D3DDECLUSAGE \_ NORMAL       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ PSIZE        | 0                      | D3DVSDE \_ PSIZE        |
| D3DDECLUSAGE \_ COLOR        | 0                      | D3DVSDE \_ DIFFUSE      |
| D3DDECLUSAGE \_ COLOR        | 1                      | D3DVSDE \_ SPECULAR     |
| D3DDECLUSAGE \_ TEXCOORD     | n                      | D3DVSDE \_ TEXCOORDn    |



 

Wenn eine Deklaration mit Hardwarevertexverarbeitung auf einem Direct3D 7-Treiber verwendet wird, konvertiert die Direct3D-Runtime sie mit den folgenden Regeln in eine FVF:

-   Es sollte nur Stream 0 verwendet werden (siehe MaxStreams-Obergrenze).
-   Die Reihenfolge der Scheitelpunktelemente sollte mit der Reihenfolge der FVF-Bits identisch sein.
-   Lücken in Texturkoordinaten sind nicht zulässig.
-   Alle Scheitelpunktelemente, die in der Tabelle nicht beschrieben werden, können nicht für alle Pre-DirectX 8-Treiber in eine gültige FVF konvertiert und daher nicht für diese Treiber verwendet werden.
-   Nur D3DDECLTYPE FLOAT2 ist für Scheitelpunktelemente mit D3DDECLUSAGE TEXCOORD zulässig, wenn das Gerät keine der \_ \_ D3DPTEXTURECAPS PROJECTED- oder \_ D3DPTEXTURECAPS \_ CUBEMAP-Obergrenzen festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunktdeklaration](vertex-declaration.md)
</dt> </dl>

 

 



