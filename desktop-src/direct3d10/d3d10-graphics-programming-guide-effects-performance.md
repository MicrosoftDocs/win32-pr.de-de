---
description: Überlegungen zur Leistung (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Überlegungen zur Leistung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041379"
---
# <a name="performance-considerations-direct3d-10"></a><span data-ttu-id="4d9c6-103">Überlegungen zur Leistung (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4d9c6-103">Performance Considerations (Direct3D 10)</span></span>

## <a name="using-effect-pools"></a><span data-ttu-id="4d9c6-104">Verwenden von Effect-Pools</span><span class="sxs-lookup"><span data-stu-id="4d9c6-104">Using Effect Pools</span></span>

<span data-ttu-id="4d9c6-105">Das Rendern von Pipelines wird häufig verwendet, um viele Shader zum Rendern verschiedener Objekttypen und spezieller Effekte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-105">It is common for rendering pipelines to use many shaders to render different object types and special effects.</span></span> <span data-ttu-id="4d9c6-106">Der Shader ist eine Mischung aus Zuständen, die für alle Shader (z. b. eine Weltmatrix oder eine helle Position) und für jeden Shader spezifisch sind, z. b. die diffuse Farbe eines Objekts oder eine Glanz Hervorhebungs Berechnung.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-106">The shader are a mixture of states that a common among all the shaders such as a world matrix or a light position, and other state that is specific to each shader such as an object's diffuse color, or specular highlight calculation.</span></span> <span data-ttu-id="4d9c6-107">Ein Effekt Pool ist eine Position im Speicher, in der der Zustand gespeichert wird, der über viele Shader hinweg verwendet wird, sowie allgemeine Geräte Objekte, wie z. b. Shader, gerenstatusobjekte und Konstantenpuffer.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-107">An effect pool is a place in memory to store state that is used across many shaders, as well as common device objects such as shaders, render state objects and constant buffers.</span></span> <span data-ttu-id="4d9c6-108">Die Leistungsverbesserung ergibt sich aus der Aktualisierung des allgemeinen Zustands für alle Shader, die diesen Zustand benötigen.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-108">The performance improvement results from updating the common state once for all the shaders that need that state.</span></span>

<span data-ttu-id="4d9c6-109">Ein Effekt Pool ist ein gemeinsam genutzter Speicherort für den Zustand des Effekts.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-109">An effect pool is a shared memory location for effect state.</span></span> <span data-ttu-id="4d9c6-110">Ein Pool wird ähnlich wie ein Effekt erstellt. Sie kann aus dem Arbeitsspeicher (oder einer Datei oder einer Ressource) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-110">A pool is created similarly to an effect; it can be created from memory (or a file or a resource).</span></span> <span data-ttu-id="4d9c6-111">Dies führt zu zwei unterschiedlichen Arten von Effekten: einen globalen Effekt, der nicht von einem Zustand in anderen Effekten abhängig ist, und ein untergeordneter Effekt, der von einem anderen Effekt abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-111">This leads to two different types of effects: a global effect that does not depend on state in other effect versus a child effect which depends on state in another effect.</span></span>

<span data-ttu-id="4d9c6-112">Beim Erstellen des Effekts geben Sie an, ob ein Effekt ein globaler Effekt (der Standardfall) oder ein untergeordneter Effekt ist (durch Bereitstellen des d3d10 Effect-Flag zum Kompilieren des untergeordneten [ \_ \_ \_ \_ Effekts](d3d10-effect.md) ).</span><span class="sxs-lookup"><span data-stu-id="4d9c6-112">You specify whether an effect is a global effect (the default case) or a child effect (by supplying the [D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT](d3d10-effect.md) flag) when the effect is created.</span></span> <span data-ttu-id="4d9c6-113">Ein globaler Effekt kann als Effekt Pool dienen. ein untergeordneter Effekt kann kein Effekt Pool sein.</span><span class="sxs-lookup"><span data-stu-id="4d9c6-113">A global effect can serve as an effect pool; a child effect cannot be an effect pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d9c6-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d9c6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d9c6-115">Rendern eines Effekts</span><span class="sxs-lookup"><span data-stu-id="4d9c6-115">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[<span data-ttu-id="4d9c6-116">Effekte (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4d9c6-116">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



