---
description: Frühe, computergenerierte 3D-Images, obwohl Sie in der Regel für Ihre Zeit erweitert sind, haben tendenziell ein glänzendes Kunststoff Erscheinungsbild.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Grundlegende texturierungskonzepte (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338923"
---
# <a name="basic-texturing-concepts-direct3d-9"></a><span data-ttu-id="db682-103">Grundlegende texturierungskonzepte (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db682-103">Basic Texturing Concepts (Direct3D 9)</span></span>

<span data-ttu-id="db682-104">Frühe, computergenerierte 3D-Images, obwohl Sie in der Regel für Ihre Zeit erweitert sind, haben tendenziell ein glänzendes Kunststoff Erscheinungsbild.</span><span class="sxs-lookup"><span data-stu-id="db682-104">Early computer-generated 3D images, although generally advanced for their time, tended to have a shiny plastic look.</span></span> <span data-ttu-id="db682-105">Sie fehlten nicht die Typen von Markierungen, wie z. b. scuffs, Risse, Fingerabdrücke und smudges, die 3D-Objekten eine realistische visuelle Komplexität einräumen.</span><span class="sxs-lookup"><span data-stu-id="db682-105">They lacked the types of markings-such as scuffs, cracks, fingerprints, and smudges-that give 3D objects realistic visual complexity.</span></span> <span data-ttu-id="db682-106">In den letzten Jahren haben sich die Texturen in den Entwicklern als Tool zur Verbesserung des Realismus von computergenerierten 3D-Images erfreut.</span><span class="sxs-lookup"><span data-stu-id="db682-106">In recent years, textures have gained popularity among developers as a tool for enhancing the realism of computer-generated 3D images.</span></span>

<span data-ttu-id="db682-107">In der täglichen Verwendung bezieht sich die Wort Textur auf die glätttheit oder die rautheit eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="db682-107">In its everyday use, the word texture refers to an object's smoothness or roughness.</span></span> <span data-ttu-id="db682-108">In Computergrafiken ist eine Textur jedoch eine Bitmap von Pixel Farben, die einem Objekt die Darstellung der Textur verleiht.</span><span class="sxs-lookup"><span data-stu-id="db682-108">In computer graphics, however, a texture is a bitmap of pixel colors that give an object the appearance of texture.</span></span>

<span data-ttu-id="db682-109">Da Direct3D-Texturen Bitmaps sind, kann jede Bitmap auf ein Direct3D-primitiv angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="db682-109">Because Direct3D textures are bitmaps, any bitmap can be applied to a Direct3D primitive.</span></span> <span data-ttu-id="db682-110">Beispielsweise können Anwendungen Objekte erstellen und bearbeiten, für die offenbar ein Holz kornmuster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="db682-110">For instance, applications can create and manipulate objects that appear to have a wood grain pattern in them.</span></span> <span data-ttu-id="db682-111">Grass, Dirt und Rocks können auf einen Satz von 3D-primitiven angewendet werden, die einen Hügel bilden.</span><span class="sxs-lookup"><span data-stu-id="db682-111">Grass, dirt, and rocks can be applied to a set of 3D primitives that form a hill.</span></span> <span data-ttu-id="db682-112">Das Ergebnis ist ein realistisch aussehende Hügel.</span><span class="sxs-lookup"><span data-stu-id="db682-112">The result is a realistic-looking hillside.</span></span> <span data-ttu-id="db682-113">Sie können Texturing auch zum Erstellen von Effekten verwenden, z. b. bei Vorzeichen an einem Straßenrand, bei Rock Schichten in einer Klippe oder in der Darstellung von Marmor auf einem Boden.</span><span class="sxs-lookup"><span data-stu-id="db682-113">You can also use texturing to create effects such as signs along a roadside, rock strata in a cliff, or the appearance of marble on a floor.</span></span>

<span data-ttu-id="db682-114">Außerdem unterstützt Direct3D erweiterte texturierungstechniken, wie z. b. Textur Mischung, mit oder ohne Transparenz und einfache Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="db682-114">In addition, Direct3D supports more advanced texturing techniques such as texture blending-with or without transparency-and light mapping.</span></span> <span data-ttu-id="db682-115">Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md) und [Light Mapping with Texturen (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="db682-115">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md) and [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

<span data-ttu-id="db682-116">Wenn Ihre Anwendung ein HAL-Gerät (Hardware Abstraktion Layer) oder ein Software Gerät erstellt, kann Sie die Texturen 8, 16, 24, 32, 64 oder 128-Bit verwenden.</span><span class="sxs-lookup"><span data-stu-id="db682-116">If your application creates a hardware abstraction layer (HAL) device or a software device, it can use 8, 16, 24, 32, 64, or 128-bit textures.</span></span>

<span data-ttu-id="db682-117">Weitere Informationen finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="db682-117">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="db682-118">Textur Adressierungs Modi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db682-118">Texture Addressing Modes (Direct3D 9)</span></span>](texture-addressing-modes.md)
-   [<span data-ttu-id="db682-119">Struktur Änderungs Bereiche (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db682-119">Texture Dirty Regions (Direct3D 9)</span></span>](texture-dirty-regions.md)
-   [<span data-ttu-id="db682-120">Textur Paletten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="db682-120">Texture Palettes (Direct3D 9)</span></span>](texture-palettes.md)

## <a name="related-topics"></a><span data-ttu-id="db682-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db682-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db682-122">Direct3D-Texturen</span><span class="sxs-lookup"><span data-stu-id="db682-122">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



