---
title: Struktur der Schnittmengen Attribute
description: Eine in HLSL deklarierte Struktur, die Treffer Attribute für Dreiecks Schnittstellen mit fester Funktion oder an einem Achsen ausgerichteten Begrenzungsfeld für die prozedurale Schnittmenge darstellt.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106365220"
---
# <a name="intersection-attributes-structure"></a><span data-ttu-id="ea7b6-103">Struktur der Schnittmengen Attribute</span><span class="sxs-lookup"><span data-stu-id="ea7b6-103">Intersection attributes structure</span></span> 

<span data-ttu-id="ea7b6-104">Eine in HLSL deklarierte Struktur, die Treffer Attribute für Dreiecks Schnittstellen mit fester Funktion oder an einem Achsen ausgerichteten Begrenzungsfeld für die prozedurale Schnittmenge darstellt.</span><span class="sxs-lookup"><span data-stu-id="ea7b6-104">A structure declared in HLSL to represent hit attributes for fixed-function triangle intersection or axis-aligned bounding box for procedural primitive intersection.</span></span>

## <a name="fixed-function-triangle-intersection"></a><span data-ttu-id="ea7b6-105">Dreiecks Schnittmenge mit fester Funktion</span><span class="sxs-lookup"><span data-stu-id="ea7b6-105">Fixed-function triangle intersection</span></span>

<span data-ttu-id="ea7b6-106">Die folgende Struktur wird in HLSL deklariert, um Treffer Attribute für Dreiecks Schnittstellen mit fester Funktion darzustellen:</span><span class="sxs-lookup"><span data-stu-id="ea7b6-106">The following structure is declared in HLSL to represent hit attributes for fixed-function triangle intersection:</span></span>


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

<span data-ttu-id="ea7b6-107">[Alle Treffer](any-hit-shader.md) -und [nächsten Treffer](closest-hit-shader.md) -Shader, die mithilfe von Dreiecks Schnittstellen mit fester Funktion aufgerufen wurden, müssen diese Struktur für Treffer Attribute verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea7b6-107">[Any hit](any-hit-shader.md) and [closest hit](closest-hit-shader.md) shaders invoked using fixed-function triangle intersection must use this structure for hit attributes.</span></span> <span data-ttu-id="ea7b6-108">Bei den Attributen a0, a1 und a2 für die 3 Scheitel Punkte eines Dreiecks ist "barycentrics. x" die Gewichtung für a1 und barycentrics. y ist die Gewichtung für a2.</span><span class="sxs-lookup"><span data-stu-id="ea7b6-108">Given attributes a0, a1 and a2 for the 3 vertices of a triangle, barycentrics.x is the weight for a1 and barycentrics.y is the weight for a2.</span></span>  <span data-ttu-id="ea7b6-109">Die APP kann z. b. wie folgt interpolieren: a = a0 + barycentrics. x \* (a1-a0) + baryzentrics. y \* (a2 – a0).</span><span class="sxs-lookup"><span data-stu-id="ea7b6-109">For example, the app can interpolate by doing:  a = a0 + barycentrics.x \* (a1-a0) + barycentrics.y\* (a2 – a0).</span></span>

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a><span data-ttu-id="ea7b6-110">Achsen gerichtetes Begrenzungsfeld für prozedurale Schnittmenge</span><span class="sxs-lookup"><span data-stu-id="ea7b6-110">Axis-aligned bounding box for procedural primitive intersection</span></span>

<span data-ttu-id="ea7b6-111">Wenn Achsen ausgerichtete Begrenzungs Felder für Schnittmengen mit prozeduralen primitiven verwendet werden, wird ein Schnittstellen-Shader ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ea7b6-111">When axis-aligned bounding boxes are used for intersection with procedural primitives, an intersection shader is triggered.</span></span>  <span data-ttu-id="ea7b6-112">Dieser Shader stellt dem [**reporthit**](reporthit-function.md) -Befehl eine benutzerdefinierte Schnittmengen-Attribut Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="ea7b6-112">That shader provides a user-defined intersection attribute structure to the [**ReportHit**](reporthit-function.md) call.</span></span>  <span data-ttu-id="ea7b6-113">Alle Treffer-und nächsten Treffer-Shader, die in derselben Treffer Gruppe mit diesem schnittsshader gebunden sind, müssen dieselbe Struktur für Treffer Attribute verwenden, auch wenn auf die Attribute nicht verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ea7b6-113">The any hit and closest hit shaders bound in the same hit group with this intersection shader must use the same structure for hit attributes, even if the attributes are not referenced.</span></span>  <span data-ttu-id="ea7b6-114">Die maximale Attribut Struktur Größe beträgt 32 Bytes und wird als **Maximale \_ Attribut Größe von D3D12 Raytracing \_ \_ \_ \_ in \_ Byte** definiert.</span><span class="sxs-lookup"><span data-stu-id="ea7b6-114">The maximum attribute structure size is 32 bytes, defined as **D3D12\_RAYTRACING\_MAX\_ATTRIBUTE\_SIZE\_IN\_BYTES**.</span></span>


