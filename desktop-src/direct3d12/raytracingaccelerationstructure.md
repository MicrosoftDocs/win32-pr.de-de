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
# <a name="raytracingaccelerationstructure"></a><span data-ttu-id="c60a2-103">RaytracingAccelerationStructure</span><span class="sxs-lookup"><span data-stu-id="c60a2-103">RaytracingAccelerationStructure</span></span>

<span data-ttu-id="c60a2-104">Ein Ressourcentyp, der in HLSL deklariert und in [**traceray**](traceray-function.md) übergeben werden kann, um die Beschleunigungs Ressource der obersten Ebene anzugeben, die mithilfe von **buildraytracingaccelerationstructure** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c60a2-104">A resource type that can be declared in HLSL and passed into [**TraceRay**](traceray-function.md) to indicate the top-level acceleration resource built using **BuildRaytracingAccelerationStructure**.</span></span> <span data-ttu-id="c60a2-105">Er ist als rohpuffer-SRV in einer Deskriptortabelle oder einem Stamm Deskriptor-SRV gebunden.</span><span class="sxs-lookup"><span data-stu-id="c60a2-105">It is bound as a raw buffer SRV in a descriptor table or root descriptor SRV.</span></span>  <span data-ttu-id="c60a2-106">Die-Deklaration in HLSL lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c60a2-106">The declaration in HLSL is as follows:</span></span>


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

<span data-ttu-id="c60a2-107">Dieses Beispiel zeigt ein Array mit einer unbegrenzten Größe von beschleunigungsstrukturen, das impliziert, dass ein deskriptorheap stammt, da Stamm Deskriptoren nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="c60a2-107">This example shows an unbounded size array of acceleration structures, which implies coming from a descriptor heap since root descriptors can’t be indexed.</span></span>

<span data-ttu-id="c60a2-108">**Raytracingaccelerationstructure** ist eine nicht transparente Ressource ohne verfügbare Methoden für Shader.</span><span class="sxs-lookup"><span data-stu-id="c60a2-108">**RaytracingAccelerationStructure** is an opaque resource with no methods available to shaders.</span></span>


 

 




