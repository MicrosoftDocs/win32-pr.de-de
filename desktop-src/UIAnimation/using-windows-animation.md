---
title: Windows-Animations Aufgaben
description: In den Themen in diesem Abschnitt werden die grundlegenden Aufgaben beschrieben, die für Anwendungen erforderlich sind, die Windows Animation Manager verwenden.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Windows Animation Windows Animation, Tasks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339434"
---
# <a name="windows-animation-tasks"></a><span data-ttu-id="a40f0-104">Windows-Animations Aufgaben</span><span class="sxs-lookup"><span data-stu-id="a40f0-104">Windows Animation Tasks</span></span>

<span data-ttu-id="a40f0-105">In den Themen in diesem Abschnitt werden die grundlegenden Aufgaben beschrieben, die für Anwendungen erforderlich sind, die Windows Animation Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="a40f0-105">The topics contained in this section describe the basic tasks required of applications that use Windows Animation Manager.</span></span>

<span data-ttu-id="a40f0-106">Diese Aufgaben sind in der richtigen Reihenfolge enthalten:</span><span class="sxs-lookup"><span data-stu-id="a40f0-106">These tasks, in order, include:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a40f0-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a40f0-107">In this section</span></span>



| <span data-ttu-id="a40f0-108">Thema</span><span class="sxs-lookup"><span data-stu-id="a40f0-108">Topic</span></span>                                                                                                | <span data-ttu-id="a40f0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a40f0-109">Description</span></span>                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a40f0-110">Erstellen der Haupt Animations Objekte</span><span class="sxs-lookup"><span data-stu-id="a40f0-110">Create the Main Animation Objects</span></span>](adding-animation-to-an-application.md)<br/>               | <span data-ttu-id="a40f0-111">Um die Windows-Animation in Ihrer Anwendung zu verwenden, besteht der erste Schritt darin, eine kleine Gruppe von Haupt Animations Objekten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a40f0-111">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="a40f0-112">Erstellen von Animations Variablen</span><span class="sxs-lookup"><span data-stu-id="a40f0-112">Create Animation Variables</span></span>](create-animation-variables.md)<br/>                              | <span data-ttu-id="a40f0-113">Eine Anwendung muss eine Animations Variable für jedes visuelle Merkmal erstellen, das mithilfe der Windows-Animation animiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a40f0-113">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="a40f0-114">Aktualisieren des Animations-Managers und Zeichnen von Frames</span><span class="sxs-lookup"><span data-stu-id="a40f0-114">Update the Animation Manager and Draw Frames</span></span>](introducing-windows-animation-manager.md)<br/> | <span data-ttu-id="a40f0-115">Jedes Mal, wenn eine Anwendung ein Storyboard plant, muss die Anwendung die aktuelle Zeit für den Animations-Manager bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a40f0-115">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="a40f0-116">Die aktuelle Zeit ist auch erforderlich, wenn der Animations-Manager weitergeleitet wird, um seinen Zustand zu aktualisieren, und alle Animations Variablen auf die entsprechenden interintermierten Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a40f0-116">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span><br/> |
| [<span data-ttu-id="a40f0-117">Lesen der Animations Variablen Werte</span><span class="sxs-lookup"><span data-stu-id="a40f0-117">Read the Animation Variable Values</span></span>](updating---application-driven-animation.md)<br/>         | <span data-ttu-id="a40f0-118">Jedes Mal, wenn die Anwendung zeichnet, sollte Sie die aktuellen Werte der Animations Variablen lesen, die die zu animierenden visuellen Merkmale darstellen.</span><span class="sxs-lookup"><span data-stu-id="a40f0-118">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a40f0-119">Erstellen eines Storyboards und Hinzufügen von Übergängen</span><span class="sxs-lookup"><span data-stu-id="a40f0-119">Create a Storyboard and Add Transitions</span></span>](updating---timer-driven-animation.md)<br/>          | <span data-ttu-id="a40f0-120">Zum Erstellen einer Animation muss eine Anwendung ein Storyboard erstellen.</span><span class="sxs-lookup"><span data-stu-id="a40f0-120">To create an animation, an application must construct a storyboard.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="a40f0-121">Planen eines Storyboards</span><span class="sxs-lookup"><span data-stu-id="a40f0-121">Schedule a Storyboard</span></span>](scheduling-a-storyboard.md)<br/>                                      | <span data-ttu-id="a40f0-122">Nachdem ein Storyboard erstellt wurde, wird es vom Animations-Manager geplant.</span><span class="sxs-lookup"><span data-stu-id="a40f0-122">After a storyboard is created, it is scheduled by the animation manager.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="a40f0-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a40f0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a40f0-124">Übersicht über Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="a40f0-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="a40f0-125">Referenz zur Windows-Animation</span><span class="sxs-lookup"><span data-stu-id="a40f0-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="a40f0-126">Beispiele für Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="a40f0-126">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> </dl>

 

 





