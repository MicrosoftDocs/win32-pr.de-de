---
description: Texturen sind ein leistungsstarkes Tool, um mit dem Computer realistische 3D-Bilder zu erzeugen. Direct3D unterstützt einen umfangreichen Texturfunktionssatz und ermöglicht Entwicklern dadurch den einfachen Zugriff auf erweiterte Texturtechniken.
ms.assetid: 48dcbc86-631e-4bc7-b809-b0e4a0a9ae8e
title: Direct3D-Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afebd7217b36ad5f740616e198963314a1d2aca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123451"
---
# <a name="direct3d-textures-direct3d-9"></a><span data-ttu-id="1aa75-104">Direct3D-Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-104">Direct3D Textures (Direct3D 9)</span></span>

<span data-ttu-id="1aa75-105">Texturen sind ein leistungsstarkes Tool, um mit dem Computer realistische 3D-Bilder zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="1aa75-105">Textures are a powerful tool in creating realism in computer-generated 3D images.</span></span> <span data-ttu-id="1aa75-106">Direct3D unterstützt einen umfangreichen Texturfunktionssatz und ermöglicht Entwicklern dadurch den einfachen Zugriff auf erweiterte Texturtechniken.</span><span class="sxs-lookup"><span data-stu-id="1aa75-106">Direct3D supports an extensive texturing feature set, providing developers with easy access to advanced texturing techniques.</span></span>

<span data-ttu-id="1aa75-107">In diesem Abschnitt erhalten Sie einen Einstieg in die Verwendung von Texturen.</span><span class="sxs-lookup"><span data-stu-id="1aa75-107">This section will get you started using textures.</span></span>

-   [<span data-ttu-id="1aa75-108">Grundlegende texturierungskonzepte (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-108">Basic Texturing Concepts (Direct3D 9)</span></span>](basic-texturing-concepts.md)
-   [<span data-ttu-id="1aa75-109">Texturkoordinaten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-109">Texture Coordinates (Direct3D 9)</span></span>](texture-coordinates.md)
-   [<span data-ttu-id="1aa75-110">Textur Filterung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-110">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
-   [<span data-ttu-id="1aa75-111">Textur Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-111">Texture Resources (Direct3D 9)</span></span>](texture-resources.md)
-   [<span data-ttu-id="1aa75-112">Textur Wrapping (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-112">Texture Wrapping (Direct3D 9)</span></span>](texture-wrapping.md)
-   [<span data-ttu-id="1aa75-113">Textur Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-113">Texture Blending (Direct3D 9)</span></span>](texture-blending.md)

<span data-ttu-id="1aa75-114">Diese Themen werden ausführlicher über zusätzliche texturierungsfunktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="1aa75-114">These topics will go into more detail about additional texturing functionality.</span></span>

-   [<span data-ttu-id="1aa75-115">Automatische Generierung von Mipmaps (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-115">Automatic Generation of Mipmaps (Direct3D 9)</span></span>](automatic-generation-of-mipmaps.md)
-   [<span data-ttu-id="1aa75-116">Automatische Textur Verwaltung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-116">Automatic Texture Management (Direct3D 9)</span></span>](automatic-texture-management.md)
-   [<span data-ttu-id="1aa75-117">Komprimierte Textur Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-117">Compressed Texture Resources (Direct3D 9)</span></span>](compressed-texture-resources.md)
-   [<span data-ttu-id="1aa75-118">Überlegungen zur Hardware für die Texturierung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-118">Hardware Considerations for Texturing (Direct3D 9)</span></span>](hardware-considerations-for-texturing.md)
-   [<span data-ttu-id="1aa75-119">Volumetextur-Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1aa75-119">Volume Texture Resources (Direct3D 9)</span></span>](volume-texture-resources.md)

<span data-ttu-id="1aa75-120">Um die Leistung zu verbessern, sollten Sie dynamische Texturen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1aa75-120">For improved performance, consider using dynamic textures.</span></span> <span data-ttu-id="1aa75-121">Eine dynamische Textur kann gesperrt, geschrieben und in jedem Frame entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="1aa75-121">A dynamic texture can be locked, written to, and unlocked each frame.</span></span> <span data-ttu-id="1aa75-122">Siehe [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="1aa75-122">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1aa75-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1aa75-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aa75-124">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="1aa75-124">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



