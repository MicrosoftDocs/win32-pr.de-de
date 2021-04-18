---
description: Das Seiten kippen ist in Multimedia-, Animations-und Spielsoftware ein wichtiger Punkt. Dies entspricht der Art und Weise, wie Sie Animationen mit einem Papierblatt durchführen können.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Seiten kippen und zurück Pufferung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345582"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a><span data-ttu-id="24cd7-103">Seiten kippen und zurück Pufferung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="24cd7-103">Page Flipping and Back Buffering (Direct3D 9)</span></span>

<span data-ttu-id="24cd7-104">Das Seiten kippen ist in Multimedia-, Animations-und Spielsoftware ein wichtiger Punkt. Dies entspricht der Art und Weise, wie Sie Animationen mit einem Papierblatt durchführen können.</span><span class="sxs-lookup"><span data-stu-id="24cd7-104">Page flipping is key in multimedia, animation, and game software; it is analogous to the way you can do animation with a pad of paper.</span></span> <span data-ttu-id="24cd7-105">Auf jeder Seite ändert der Künstler die Abbildung leicht, sodass das Zeichnen beim schnellen kippen zwischen den Blättern animiert erscheint.</span><span class="sxs-lookup"><span data-stu-id="24cd7-105">On each page, the artist changes the figure slightly, so that when you flip rapidly between sheets, the drawing appears animated.</span></span>

<span data-ttu-id="24cd7-106">Das Seiten kippen in Software ähnelt diesem Prozess.</span><span class="sxs-lookup"><span data-stu-id="24cd7-106">Page flipping in software is similar to this process.</span></span> <span data-ttu-id="24cd7-107">Direct3D implementiert die Seiten flippingfunktion über eine SwapChain, bei der es sich um eine Eigenschaft des Geräts handelt.</span><span class="sxs-lookup"><span data-stu-id="24cd7-107">Direct3D implements page flipping functionality through a swap chain, which is a property of the device.</span></span> <span data-ttu-id="24cd7-108">Zuerst richten Sie eine Reihe von Direct3D-Puffern ein, die so auf den Bildschirm kippen, wie das Papier des Künstlers auf die nächste Seite gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="24cd7-108">Initially, you set up a series of Direct3D buffers that flip to the screen in the way that the artist's paper flips to the next page.</span></span> <span data-ttu-id="24cd7-109">Der erste Puffer wird als Farben-Front-Puffer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="24cd7-109">The first buffer is referred to as the color front buffer.</span></span> <span data-ttu-id="24cd7-110">Die Puffer dahinter werden als backpuffer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="24cd7-110">The buffers behind it are called back buffers.</span></span> <span data-ttu-id="24cd7-111">Die Anwendung schreibt in einen Hintergrund Puffer und flippt dann den Farben-Front-Puffer, sodass der Hintergrund Puffer auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="24cd7-111">Your application writes to a back buffer and then flips the color front buffer so that the back buffer appears on screen.</span></span> <span data-ttu-id="24cd7-112">Während das System das Abbild anzeigt, schreibt ihre Software erneut in einen Hintergrund Puffer.</span><span class="sxs-lookup"><span data-stu-id="24cd7-112">While the system displays the image, your software is again writing to a back buffer.</span></span> <span data-ttu-id="24cd7-113">Der Prozess wird so lange fortgesetzt, wie Sie animieren, sodass Sie Bilder effizient animieren können.</span><span class="sxs-lookup"><span data-stu-id="24cd7-113">The process continues as long as you are animating, enabling you to animate images efficiently.</span></span>

<span data-ttu-id="24cd7-114">Direct3D erleichtert das Einrichten von Seiten flippingschemas, von einem einfachen, doppelt gepufferten Schema (einem Farb-Front-Puffer mit einem Hintergrund Puffer) bis hin zu komplexeren Schemas mit zusätzlichen backpuffern.</span><span class="sxs-lookup"><span data-stu-id="24cd7-114">Direct3D makes it easy to set up page flipping schemes - from a simple double-buffered scheme (a color front buffer with one back buffer) to more sophisticated schemes with additional back buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24cd7-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24cd7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24cd7-116">Direct3D-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="24cd7-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="24cd7-117">Was ist eine austauschkette? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="24cd7-117">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



