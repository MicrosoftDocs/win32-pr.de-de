---
title: RaytracingAccelerationStructure
description: Ein Ressourcentyp, der in HLSL deklariert und an TraceRay übergeben werden kann, um die Beschleunigungsressource der obersten Ebene anzugeben, die mit BuildRaytracingAccelerationStructure erstellt wurde.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 4728e167fe9fbc353c51accaa92d9b9d4086a0bfff3f098f43b93523cd63a792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123618"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Ein Ressourcentyp, der in HLSL deklariert und an [**TraceRay**](traceray-function.md) übergeben werden kann, um die Beschleunigungsressource der obersten Ebene anzugeben, die mit **BuildRaytracingAccelerationStructure erstellt wurde.** Sie wird als unformatierter Puffer-SRV in einer Deskriptortabelle oder einem Stammdeskriptor-SRV gebunden.  Die Deklaration in HLSL lautet wie folgt:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

Dieses Beispiel zeigt ein Array mit einer ungebundenen Größe von Beschleunigungsstrukturen, was darauf hindeutet, dass er von einem Deskriptorhap kommt, da Stammdeskriptoren nicht indiziert werden können.

**RaytracingAccelerationStructure** ist eine nicht transparente Ressource ohne Methoden, die Shadern zur Verfügung stehen.


 

 




