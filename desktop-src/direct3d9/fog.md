---
description: Das Hinzufügen von Nebel zu einer 3D-Szene kann den Realismus verbessern, Ambiente bereitstellen oder einen Stimmungs Wert festlegen
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Nebel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341095"
---
# <a name="fog-direct3d-9"></a><span data-ttu-id="47ba7-103">Nebel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47ba7-103">Fog (Direct3D 9)</span></span>

<span data-ttu-id="47ba7-104">Das Hinzufügen von Nebel zu einer 3D-Szene kann den Realismus verbessern, Ambiente bereitstellen oder einen Stimmungs Wert festlegen</span><span class="sxs-lookup"><span data-stu-id="47ba7-104">Adding fog to a 3D scene can enhance realism, provide ambiance or set a mood, and obscure artifacts sometimes caused when distant geometry comes into view.</span></span> <span data-ttu-id="47ba7-105">Direct3D unterstützt zwei Nebel Modelle, Pixel Nebel und Scheitelpunkt Nebel, jeweils mit eigenen Features und Programmierschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="47ba7-105">Direct3D supports two fog models, pixel fog and vertex fog, each with its own features and programming interface.</span></span>

<span data-ttu-id="47ba7-106">Im Wesentlichen wird Nebel implementiert, indem die Farbe von Objekten in einer Szene mit einer ausgewählten Nebelfarbe auf der Grundlage der Tiefe eines Objekts in einer Szene oder der Entfernung vom Standpunkt kombiniert wird.</span><span class="sxs-lookup"><span data-stu-id="47ba7-106">Essentially, fog is implemented by blending the color of objects in a scene with a chosen fog color based on the depth of an object in a scene or its distance from the viewpoint.</span></span> <span data-ttu-id="47ba7-107">Wenn Objekte weiter entfernt werden, werden Ihre ursprüngliche Farbe mehr und mehr mit der ausgewählten Nebelfarbe kombiniert. Dadurch wird die Illusion erstellt, dass das Objekt zunehmend von kleinen, in der Szene gleitenden Partikeln verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="47ba7-107">As objects grow more distant, their original color blends more and more with the chosen fog color, creating the illusion that the object is being increasingly obscured by tiny particles floating in the scene.</span></span> <span data-ttu-id="47ba7-108">Die folgende Abbildung zeigt eine Szene, die ohne Nebel gerendert wird</span><span class="sxs-lookup"><span data-stu-id="47ba7-108">The following illustration shows a scene rendered without fog, and a similar scene rendered with fog enabled.</span></span>

![Darstellung der gleichen Szene mit und ohne Nebel](images/fogcomp.png)

<span data-ttu-id="47ba7-110">In dieser Abbildung hat die Szene auf der linken Seite einen klaren Horizont, über den keine Landschaft sichtbar ist, auch wenn Sie in der realen Welt sichtbar wäre.</span><span class="sxs-lookup"><span data-stu-id="47ba7-110">In this illustration, the scene on the left has a clear horizon, beyond which no scenery is visible, even though it would be visible in the real world.</span></span> <span data-ttu-id="47ba7-111">Die Szene auf der rechten Seite verdeckt den Horizont, indem eine mit der Hintergrundfarbe identische Nebelfarbe verwendet wird, sodass Polygone in den Abstand eingeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="47ba7-111">The scene on the right obscures the horizon by using a fog color identical to the background color, making polygons appear to fade into the distance.</span></span> <span data-ttu-id="47ba7-112">Durch die Kombination von diskreten Nebeleffekten mit dem Design der kreativen Szene können Sie Stimmungs Werte hinzufügen und die Farbe von Objekten in einer Szene weich gestalten.</span><span class="sxs-lookup"><span data-stu-id="47ba7-112">By combining discrete fog effects with creative scene design you can add mood and soften the color of objects in a scene.</span></span>

<span data-ttu-id="47ba7-113">Direct3D bietet zwei Möglichkeiten zum Hinzufügen von Nebel zu einer Szene: Pixel Nebel und Scheitelpunkt Nebel, die für die Anwendung der Nebeleffekte benannt werden.</span><span class="sxs-lookup"><span data-stu-id="47ba7-113">Direct3D provides two ways to add fog to a scene: pixel fog and vertex fog, named for how the fog effects are applied.</span></span> <span data-ttu-id="47ba7-114">Weitere Informationen finden Sie unter [Pixel Nebel (Direct3D 9)](pixel-fog.md) und [Scheitelpunkt Nebel (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="47ba7-114">For details, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span> <span data-ttu-id="47ba7-115">Kurz gesagt: Pixel Nebel, auch als "Tabellen Nebel" bezeichnet, wird im Gerätetreiber implementiert, und der Scheitelpunkt Nebel wird in der Direct3D-Beleuchtungs-Engine implementiert.</span><span class="sxs-lookup"><span data-stu-id="47ba7-115">In short, pixel fog - also called table fog - is implemented in the device driver and vertex fog is implemented in the Direct3D lighting engine.</span></span> <span data-ttu-id="47ba7-116">Eine Anwendung kann Nebel mit einem Vertexshader implementieren und ggf. Pixel Nebel gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="47ba7-116">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

> [!Note]  
> <span data-ttu-id="47ba7-117">Unabhängig davon, ob Sie Pixel oder Scheitelpunkt Nebel verwenden, muss die Anwendung eine konforme Projektions Matrix bereitstellen, um sicherzustellen, dass Nebeleffekte ordnungsgemäß angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="47ba7-117">Regardless of whether you use pixel or vertex fog, your application must provide a compliant projection matrix to ensure that fog effects are properly applied.</span></span> <span data-ttu-id="47ba7-118">Diese Einschränkung gilt auch für Anwendungen, die nicht die Direct3D-Transformation und Beleuchtungs-Engine verwenden.</span><span class="sxs-lookup"><span data-stu-id="47ba7-118">This restriction applies even to applications that do not use the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="47ba7-119">Weitere Details dazu, wie Sie eine geeignete Matrix bereitstellen können, finden Sie unter [Projektions Transformation (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="47ba7-119">For additional details about how you can provide an appropriate matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

 

<span data-ttu-id="47ba7-120">In den folgenden Themen werden Nebel und Informationen zur Verwendung verschiedener Nebel Features in Direct3D-Anwendungen vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="47ba7-120">The following topics introduce fog and present information about using various fog features in Direct3D applications.</span></span>

-   [<span data-ttu-id="47ba7-121">Nebel Formeln (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47ba7-121">Fog Formulas (Direct3D 9)</span></span>](fog-formulas.md)
-   [<span data-ttu-id="47ba7-122">Nebel Parameter (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47ba7-122">Fog Parameters (Direct3D 9)</span></span>](fog-parameters.md)
-   [<span data-ttu-id="47ba7-123">Nebel Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47ba7-123">Fog Blending (Direct3D 9)</span></span>](fog-blending.md)
-   [<span data-ttu-id="47ba7-124">Nebelfarbe (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47ba7-124">Fog Color (Direct3D 9)</span></span>](fog-color.md)
-   [<span data-ttu-id="47ba7-125">Scheitelpunkt Nebel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47ba7-125">Vertex Fog (Direct3D 9)</span></span>](vertex-fog.md)
-   [<span data-ttu-id="47ba7-126">Pixel Nebel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47ba7-126">Pixel Fog (Direct3D 9)</span></span>](pixel-fog.md)

<span data-ttu-id="47ba7-127">Nebel Mischung wird durch Rendering-Zustände gesteuert. Sie ist nicht Teil der programmierbaren Pixel Pipeline.</span><span class="sxs-lookup"><span data-stu-id="47ba7-127">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47ba7-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47ba7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47ba7-129">Direct3D-Rendering</span><span class="sxs-lookup"><span data-stu-id="47ba7-129">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



