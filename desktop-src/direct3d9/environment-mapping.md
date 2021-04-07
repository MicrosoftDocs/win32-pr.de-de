---
description: Die Umgebungs Zuordnung ist eine Technik, die hochgradig reflektierenden Oberflächen ohne Verwendung der Ray-Ablauf Verfolgung simuliert.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Umgebungs Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745952"
---
# <a name="environment-mapping-direct3d-9"></a><span data-ttu-id="54a2f-103">Umgebungs Zuordnung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="54a2f-103">Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="54a2f-104">Die Umgebungs Zuordnung ist eine Technik, die hochgradig reflektierenden Oberflächen ohne Verwendung der Ray-Ablauf Verfolgung simuliert.</span><span class="sxs-lookup"><span data-stu-id="54a2f-104">Environment mapping is a technique that simulates highly reflective surfaces without using ray tracing.</span></span> <span data-ttu-id="54a2f-105">In der Praxis wendet die Umgebungs Zuordnung eine spezielle Textur Karte an, die ein Bild der Szene enthält, die ein Objekt für das Objekt selbst umgibt.</span><span class="sxs-lookup"><span data-stu-id="54a2f-105">In practice, environment mapping applies a special texture map that contains an image of the scene surrounding an object to the object itself.</span></span> <span data-ttu-id="54a2f-106">Das Ergebnis ähnelt der Darstellung einer reflektierenden Oberfläche, so nah genug, um das Auge zu täuschen, ohne dass eine der komplexen Berechnungen an der Ray-Ablauf Verfolgung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="54a2f-106">The result approximates the appearance of a reflective surface, close enough to fool the eye, without incurring any of the complex computations involved in ray tracing.</span></span>

<span data-ttu-id="54a2f-107">In der folgenden Abbildung wird ein Typ der Umgebungs Zuordnung mit dem Namen sphärischen Umgebungs Zuordnung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="54a2f-107">The following illustration demonstrates a type of environment mapping called spherical environment mapping.</span></span> <span data-ttu-id="54a2f-108">Weitere Informationen finden Sie unter [sphärischen Umgebungs Zuordnung](spherical-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="54a2f-108">For details, see [Spherical Environment Mapping](spherical-environment-mapping.md).</span></span>

![Darstellung eines "Teekanne" mit einer angewendeten Textur, die die Umgebung reflektiert](images/spheremapped-teapot.png)

<span data-ttu-id="54a2f-110">Die "Teekanne" in diesem Bild scheint der Umgebung widerzuspiegeln. Dabei handelt es sich tatsächlich um eine Textur, die auf das Objekt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="54a2f-110">The teapot in this image appears to reflect its surroundings; this is actually a texture being applied to the object.</span></span> <span data-ttu-id="54a2f-111">Da die Umgebungs Zuordnung eine Textur in Kombination mit speziell berechneten Texturkoordinaten verwendet, kann Sie in Echtzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="54a2f-111">Because environment mapping uses a texture, combined with specially computed texture coordinates, it can be performed in real-time.</span></span>

<span data-ttu-id="54a2f-112">Dieser Abschnitt enthält Informationen zum Durchführen von zwei gängigen Typen der Umgebungs Zuordnung mit Direct3D.</span><span class="sxs-lookup"><span data-stu-id="54a2f-112">This section provides information about performing two common types of environment mapping with Direct3D.</span></span> <span data-ttu-id="54a2f-113">Es gibt viele Arten von Umgebungs Zuordnung, die in der gesamten Grafikbranche verwendet werden. die folgenden Themen Zielen jedoch auf die beiden gängigsten Formen ab: kubische Umgebungs Zuordnung und sphärischen Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="54a2f-113">There are many types of environment mapping in use throughout the graphics industry, but the following topics target the two most common forms: cubic environment mapping and spherical environment mapping.</span></span>

-   [<span data-ttu-id="54a2f-114">Kubische Umgebungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="54a2f-114">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
-   [<span data-ttu-id="54a2f-115">Sphärischen Umgebungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="54a2f-115">Spherical Environment Mapping</span></span>](spherical-environment-mapping.md)

## <a name="related-topics"></a><span data-ttu-id="54a2f-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54a2f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54a2f-117">Pixel Pipeline</span><span class="sxs-lookup"><span data-stu-id="54a2f-117">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



