---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, Fragmente
- OpenGL-Verarbeitungs Pipeline, Fragmente
- Fragmente OpenGL
- Framebuffers, Fragmente, die Pixel ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337375"
---
# <a name="fragments"></a><span data-ttu-id="ecfc4-107">Fragments</span><span class="sxs-lookup"><span data-stu-id="ecfc4-107">Fragments</span></span>

<span data-ttu-id="ecfc4-108">Ein von Rasterung erstelltes Fragment ändert das entsprechende Pixel im Frame Puffer nur dann, wenn es die folgenden Tests übergibt:</span><span class="sxs-lookup"><span data-stu-id="ecfc4-108">A fragment produced by rasterization modifies the corresponding pixel in the framebuffer only if it passes the following tests:</span></span>

-   [<span data-ttu-id="ecfc4-109">Pixel Besitz Test</span><span class="sxs-lookup"><span data-stu-id="ecfc4-109">Pixel ownership test</span></span>](pixel-ownership-test.md)
-   [<span data-ttu-id="ecfc4-110">Scissor-Test</span><span class="sxs-lookup"><span data-stu-id="ecfc4-110">Scissor test</span></span>](scissor-test.md)
-   [<span data-ttu-id="ecfc4-111">Alpha-Test</span><span class="sxs-lookup"><span data-stu-id="ecfc4-111">Alpha test</span></span>](alpha-test.md)
-   [<span data-ttu-id="ecfc4-112">Schablone-Test</span><span class="sxs-lookup"><span data-stu-id="ecfc4-112">Stencil test</span></span>](stencil-test.md)
-   [<span data-ttu-id="ecfc4-113">Tiefen Puffer Test</span><span class="sxs-lookup"><span data-stu-id="ecfc4-113">Depth-buffer test</span></span>](depth-buffer-test.md)

<span data-ttu-id="ecfc4-114">Wenn Sie den Wert übergibt, können die Daten des Fragments die vorhandenen Frame Puffer-Werte ersetzen, oder Sie können Sie mit vorhandenen Daten im Frame Puffer kombinieren, abhängig vom Zustand bestimmter Modi.</span><span class="sxs-lookup"><span data-stu-id="ecfc4-114">If it passes, the fragment's data can replace the existing framebuffer values, or you can combine it with existing data in the framebuffer, depending on the state of certain modes.</span></span> <span data-ttu-id="ecfc4-115">Sie können das Fragment mit Daten im Frame Puffer kombinieren, indem Sie Folgendes durchführen:</span><span class="sxs-lookup"><span data-stu-id="ecfc4-115">You can combine the fragment with data in the framebuffer by:</span></span>

-   [<span data-ttu-id="ecfc4-116">Bänder</span><span class="sxs-lookup"><span data-stu-id="ecfc4-116">Blending</span></span>](blending.md)
-   [<span data-ttu-id="ecfc4-117">Dithering</span><span class="sxs-lookup"><span data-stu-id="ecfc4-117">Dithering</span></span>](dithering.md)
-   [<span data-ttu-id="ecfc4-118">Logische Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ecfc4-118">Logical operations</span></span>](logical-operations.md)

 

 




