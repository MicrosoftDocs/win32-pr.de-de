---
title: RaytracingAccelerationStructure
description: Ein Ressourcentyp, der in HLSL deklariert und in traceray übergeben werden kann, um die Beschleunigungs Ressource der obersten Ebene anzugeben, die mithilfe von buildraytracingaccelerationstructure erstellt wurde.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106363880"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Ein Ressourcentyp, der in HLSL deklariert und in [**traceray**](traceray-function.md) übergeben werden kann, um die Beschleunigungs Ressource der obersten Ebene anzugeben, die mithilfe von **buildraytracingaccelerationstructure** erstellt wurde. Er ist als rohpuffer-SRV in einer Deskriptortabelle oder einem Stamm Deskriptor-SRV gebunden.  Die-Deklaration in HLSL lautet wie folgt:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

Dieses Beispiel zeigt ein Array mit einer unbegrenzten Größe von beschleunigungsstrukturen, das impliziert, dass ein deskriptorheap stammt, da Stamm Deskriptoren nicht indiziert werden können.

**Raytracingaccelerationstructure** ist eine nicht transparente Ressource ohne verfügbare Methoden für Shader.


 

 




