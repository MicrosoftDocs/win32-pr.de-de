---
title: Zuordnung zwischen d3d9-und D3D8-Deklarationen
description: In dieser Tabelle werden Member einer D3DVERTEXELEMENT9-Deklaration einer Direct3D 8-Deklaration zugeordnet.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745552"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Zuordnung zwischen d3d9-und D3D8-Deklarationen

In dieser Tabelle werden Member einer [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Deklaration einer Direct3D 8-Deklaration zugeordnet.



| Direct3D 9-Nutzung           | Direct3D 9-Verwendungs Index | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| D3DDECLUSAGE- \_ Position     | 0                      | D3DVSDE- \_ Position     |
| D3DDECLUSAGE- \_ Position     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ Normal       | 0                      | D3DVSDE \_ Normal       |
| D3DDECLUSAGE \_ Normal       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ blendweight  | 0                      | D3DVSDE \_ blendweight  |
| D3DDECLUSAGE \_ blendindices | 0                      | D3DVSDE \_ blendindices |
| D3DDECLUSAGE \_ Psize        | 0                      | D3DVSDE \_ Psize        |
| D3DDECLUSAGE- \_ Farbe        | 0                      | D3DVSDE \_ diffuses      |
| D3DDECLUSAGE- \_ Farbe        | 1                      | D3DVSDE \_ Glanz     |
| D3DDECLUSAGE \_ texcoord     | n                      | D3DVSDE \_ texcoordn    |



 

Wenn eine Deklaration für die Verarbeitung von Hardware Scheitel Punkten auf einem Direct3D 7-Treiber verwendet wird, wird Sie von der Direct3D-Laufzeit mit den folgenden Regeln in eine FVF-Datei konvertiert:

-   Es sollte nur Stream 0 verwendet werden (ersichtlich aus der maxstreams-Obergrenze).
-   Die Reihenfolge der Scheitelpunkt Elemente sollte mit der Reihenfolge der "f"-Bits identisch sein.
-   Lücken in Texturkoordinaten sind nicht zulässig.
-   Alle Vertex-Elemente, die nicht in der Tabelle beschrieben werden, können nicht für alle Pre-DirectX 8-Treiber in eine gültige FVF konvertiert werden und können daher nicht für diese Treiber verwendet werden.
-   Nur D3DDECLTYPE \_ FLOAT2 ist für Scheitelpunkt Elemente mit D3DDECLUSAGE \_ texcoord zulässig, wenn das Gerät keines der D3DPTEXTURECAPS \_ projizierten oder D3DPTEXTURECAPS \_ cubemap-Caps festgelegt hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Deklaration](vertex-declaration.md)
</dt> </dl>

 

 



