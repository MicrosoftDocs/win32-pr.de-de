---
description: Beim Erstellen von 3D-Szenen kann eine Anwendung manchmal Leistungsvorteile erzielen, indem 2D-Objekte auf eine Weise gerendert werden, die Sie als 3D-Objekte eingibt. Dies ist die grundlegende Idee hinter der Methode des fakboardingverfahrens.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Fakboardingvorgang (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344230"
---
# <a name="billboarding-direct3d-9"></a><span data-ttu-id="79395-104">Fakboardingvorgang (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="79395-104">Billboarding (Direct3D 9)</span></span>

<span data-ttu-id="79395-105">Beim Erstellen von 3D-Szenen kann eine Anwendung manchmal Leistungsvorteile erzielen, indem 2D-Objekte auf eine Weise gerendert werden, die Sie als 3D-Objekte eingibt.</span><span class="sxs-lookup"><span data-stu-id="79395-105">When creating 3D scenes, an application can sometimes gain performance advantages by rendering 2D objects in a way that makes them appear to be 3D objects.</span></span> <span data-ttu-id="79395-106">Dies ist die grundlegende Idee hinter der Methode des fakboardingverfahrens.</span><span class="sxs-lookup"><span data-stu-id="79395-106">This is the basic idea behind the technique of billboarding.</span></span>

<span data-ttu-id="79395-107">Ein Billboard im normalen Sinne des Worts ist ein Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="79395-107">A billboard in the normal sense of the word is a sign along a roadway.</span></span> <span data-ttu-id="79395-108">Microsoft Direct3D-Anwendungen können diese Art von Billboard erstellen und Rendering, indem Sie ein rechteckiges Solid definieren und eine Textur darauf anwenden.</span><span class="sxs-lookup"><span data-stu-id="79395-108">Microsoft Direct3D applications can create and render this type of billboard by defining a rectangular solid and applying a texture to it.</span></span> <span data-ttu-id="79395-109">Das Abgleichen von 3D-Grafiken ist eine Erweiterung dieser.</span><span class="sxs-lookup"><span data-stu-id="79395-109">Billboarding in the more specialized sense of 3D graphics is an extension of this.</span></span> <span data-ttu-id="79395-110">Das Ziel besteht darin, 2D-Objekte als 3D-Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="79395-110">The goal is to make 2D objects appear to be 3D.</span></span> <span data-ttu-id="79395-111">Die Technik besteht darin, eine Textur mit dem Bild des Objekts auf ein rechteckiges primitiv anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="79395-111">The technique is to apply a texture that contains the object's image to a rectangular primitive.</span></span> <span data-ttu-id="79395-112">Die primitive wird so gedreht, dass Sie immer dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="79395-112">The primitive is rotated so that it always faces the user.</span></span> <span data-ttu-id="79395-113">Es spielt keine Rolle, ob das Bild des Objekts nicht rechteckig ist.</span><span class="sxs-lookup"><span data-stu-id="79395-113">It doesn't matter if the object's image is not rectangular.</span></span> <span data-ttu-id="79395-114">Teile des Billboard können transparent gemacht werden, sodass die Teile des Billboard-Bilds, die Sie nicht sehen möchten, nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="79395-114">Portions of the billboard can be made transparent, so the parts of the billboard image that you don't want seen are not visible.</span></span>

<span data-ttu-id="79395-115">Viele Spiele verwenden die Abrechnungen für animierte Sprites.</span><span class="sxs-lookup"><span data-stu-id="79395-115">Many games employ billboarding for animated sprites.</span></span> <span data-ttu-id="79395-116">Wenn der Benutzer z. b. durch ein 3D-Maze bewegt wird, wird ihm möglicherweise Waffen oder Belohnungen angezeigt, die abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="79395-116">For instance, when the user is moving through a 3D maze, he or she may see weapons or rewards that can be picked up.</span></span> <span data-ttu-id="79395-117">Dabei handelt es sich in der Regel um 2D-Bilder, die auf einem rechteckigen primitiven</span><span class="sxs-lookup"><span data-stu-id="79395-117">These are typically 2D images textured on a rectangular primitive.</span></span> <span data-ttu-id="79395-118">Das Abgleichen von Abrechnungen wird häufig in Spielen zum Rendering von Bildern, Sträuchern und Clouds verwendet.</span><span class="sxs-lookup"><span data-stu-id="79395-118">Billboarding is often used in games to render images of trees, bushes, and clouds.</span></span>

<span data-ttu-id="79395-119">Wenn ein Bild auf ein Billboard angewendet wird, muss der rechteckige Primitive zuerst gedreht werden, damit das resultierende Bild dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="79395-119">When an image is applied to a billboard, the rectangular primitive must first be rotated so that the resulting image faces the user.</span></span> <span data-ttu-id="79395-120">Die Anwendung muss Sie dann in die Position übersetzen.</span><span class="sxs-lookup"><span data-stu-id="79395-120">Your application must then translate it into position.</span></span> <span data-ttu-id="79395-121">Die Anwendung kann dann eine Textur auf den primitiven anwenden.</span><span class="sxs-lookup"><span data-stu-id="79395-121">The application can then apply a texture to the primitive.</span></span>

<span data-ttu-id="79395-122">Das Abgleichen von Abrechnungen eignet sich am besten für symmetrische Objekte, insbesondere für symmetrische Objekte entlang der vertikalen Achse.</span><span class="sxs-lookup"><span data-stu-id="79395-122">Billboarding works best for symmetrical objects, especially objects that are symmetrical along the vertical axis.</span></span> <span data-ttu-id="79395-123">Außerdem ist es erforderlich, dass sich die Höhe des Standpunkts nicht zu stark vergrößert.</span><span class="sxs-lookup"><span data-stu-id="79395-123">It also requires that the altitude of the viewpoint doesn't increase too much.</span></span> <span data-ttu-id="79395-124">Wenn der Benutzer die in der obigen Ansicht aufgeführten Daten anzeigen darf, ist es leicht erkennbar, dass es sich um ein 2D-Objekt und nicht um 3D handelt.</span><span class="sxs-lookup"><span data-stu-id="79395-124">If the user is allowed to view the billboarded from above, it becomes readily apparent that the object is 2D rather than 3D.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79395-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79395-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79395-126">Alpha Beispiele</span><span class="sxs-lookup"><span data-stu-id="79395-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



