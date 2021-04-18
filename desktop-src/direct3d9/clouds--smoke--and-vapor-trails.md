---
description: Clouds, Rauch und dampfpfade können alle durch eine Erweiterung der Methode zum abboarding erstellt werden.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Clouds, Rauch und Dampfwege (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571222"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a><span data-ttu-id="63c87-103">Clouds, Rauch und Dampfwege (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63c87-103">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>

<span data-ttu-id="63c87-104">Clouds, Rauch und dampfpfade können alle durch eine Erweiterung der Methode zum abboarding erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="63c87-104">Clouds, smoke, and vapor trails can all be created by an extension of the billboarding technique.</span></span> <span data-ttu-id="63c87-105">Siehe [fakboardingvorgang (Direct3D 9)](billboarding.md).</span><span class="sxs-lookup"><span data-stu-id="63c87-105">See [Billboarding (Direct3D 9)](billboarding.md).</span></span> <span data-ttu-id="63c87-106">Durch das Drehen des Billboard auf zwei Achsen anstelle eines solchen kann die Anwendung es dem Benutzer ermöglichen, ein Billboard aus beliebigen Winkeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="63c87-106">By rotating the billboard on two axes instead of one, your application can enable the user to view a billboard from any angle.</span></span> <span data-ttu-id="63c87-107">In der Regel dreht eine Anwendung das Billboard auf den horizontalen und vertikalen Achsen.</span><span class="sxs-lookup"><span data-stu-id="63c87-107">Typically, an application rotates the billboard on the horizontal and vertical axes.</span></span>

<span data-ttu-id="63c87-108">Um eine einfache Cloud zu erstellen, kann die Anwendung ein rechteckiges primitiv auf einer oder zwei Achsen Drehen, sodass der primitive dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="63c87-108">To make a simple cloud, your application can rotate a rectangular primitive on one or two axes so that the primitive faces the user.</span></span> <span data-ttu-id="63c87-109">Eine cloudähnliche Textur kann dann mit Transparenz auf die primitive angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="63c87-109">A cloud-like texture can then be applied to the primitive with transparency.</span></span> <span data-ttu-id="63c87-110">Ausführliche Informationen zum Anwenden transparenter Texturen auf primitive finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="63c87-110">For details on applying transparent textures to primitives, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="63c87-111">Sie können die Cloud animieren, indem Sie im Laufe der Zeit eine Reihe von Texturen anwenden.</span><span class="sxs-lookup"><span data-stu-id="63c87-111">You can animate the cloud by applying a series of textures over time.</span></span>

<span data-ttu-id="63c87-112">Eine Anwendung kann komplexere Clouds erstellen, indem Sie Sie aus einer Gruppe von primitiven bilden.</span><span class="sxs-lookup"><span data-stu-id="63c87-112">An application can create more complex clouds by forming them from a group of primitives.</span></span> <span data-ttu-id="63c87-113">Jeder Teil der Cloud ist ein rechteckiges primitiv.</span><span class="sxs-lookup"><span data-stu-id="63c87-113">Each part of the cloud is a rectangular primitive.</span></span> <span data-ttu-id="63c87-114">Die primitiven können im Laufe der Zeit unabhängig verschoben werden, um die Darstellung eines dynamischen Mist zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="63c87-114">The primitives can be moved independently over time to give the appearance of a dynamic mist.</span></span> <span data-ttu-id="63c87-115">In der folgenden Abbildung wird dieses Konzept veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="63c87-115">The following illustration shows this concept.</span></span>

![Abbildung von primitiven, die komplexere Clouds bilden](images/cloud.png)

<span data-ttu-id="63c87-117">Das Aussehen von Rauch wird ähnlich wie Clouds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="63c87-117">The appearance of smoke is displayed in a manner similar to clouds.</span></span> <span data-ttu-id="63c87-118">Es sind in der Regel mehrere Billboards erforderlich, z.b. komplexe Clouds.</span><span class="sxs-lookup"><span data-stu-id="63c87-118">It typically requires multiple billboards, like complex clouds.</span></span> <span data-ttu-id="63c87-119">In der Regel wird ein Rauch angezeigt, der sich im Laufe der Zeit befindet, sodass die Plakate, aus denen sich die Rauch-Plume bilden, entsprechend verschoben werden</span><span class="sxs-lookup"><span data-stu-id="63c87-119">Smoke usually billows and rises over time, so the billboards that make up the smoke plume need to move accordingly.</span></span> <span data-ttu-id="63c87-120">Möglicherweise müssen Sie weitere Billboards hinzufügen, wenn Plume ansteigt und verteilt wird.</span><span class="sxs-lookup"><span data-stu-id="63c87-120">You may need to add more billboards as the plume rises and disperses.</span></span>

<span data-ttu-id="63c87-121">Ein dampfpfad ist ein Rauch-Plume, der nicht steigt.</span><span class="sxs-lookup"><span data-stu-id="63c87-121">A vapor trail is a smoke plume that doesn't rise.</span></span> <span data-ttu-id="63c87-122">Wie eine Rauch-Plume wird Sie jedoch über einen Zeitraum verteilt.</span><span class="sxs-lookup"><span data-stu-id="63c87-122">However, like a smoke plume, it disperses over time.</span></span> <span data-ttu-id="63c87-123">In der folgenden Abbildung wird veranschaulicht, wie Sie mithilfe von Billboards einen dampfpfad simulieren.</span><span class="sxs-lookup"><span data-stu-id="63c87-123">The following illustration shows the technique of using billboards to simulate a vapor trail.</span></span>

![Abbildung von Plakatwänden, die einen Dampf Pfad simulieren](images/vapor.png)

## <a name="related-topics"></a><span data-ttu-id="63c87-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63c87-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63c87-126">Alpha Beispiele</span><span class="sxs-lookup"><span data-stu-id="63c87-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



