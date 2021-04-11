---
title: Pixel Besitz Test
description: Der Pixel Besitz Test bestimmt, ob der aktuelle OpenGL-Kontext das Pixel im Frame Puffer besitzt, das einem bestimmten Fragment entspricht.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- OpenGL-Verarbeitungs Pipeline, Pixel Besitz Test
- Pixel Besitz Test OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310336"
---
# <a name="pixel-ownership-test"></a><span data-ttu-id="526d4-105">Pixel Besitz Test</span><span class="sxs-lookup"><span data-stu-id="526d4-105">Pixel Ownership Test</span></span>

<span data-ttu-id="526d4-106">Der Pixel Besitz Test bestimmt, ob der aktuelle OpenGL-Kontext das Pixel im Frame Puffer besitzt, das einem bestimmten Fragment entspricht.</span><span class="sxs-lookup"><span data-stu-id="526d4-106">The pixel ownership test determines whether the current OpenGL context owns the pixel in the framebuffer corresponding to a particular fragment.</span></span> <span data-ttu-id="526d4-107">Wenn dies der Fall ist, geht das Fragment mit dem nächsten Test fort.</span><span class="sxs-lookup"><span data-stu-id="526d4-107">If so, the fragment proceeds to the next test.</span></span> <span data-ttu-id="526d4-108">Wenn dies nicht der Fall ist, bestimmt das Fenstersystem, ob das Fragment verworfen wird, oder ob weitere fragmentvorgänge mit diesem Fragment ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="526d4-108">If not, the window system determines whether the fragment is discarded or whether any further fragment operations will be performed with that fragment.</span></span> <span data-ttu-id="526d4-109">Mit diesem Test steuert das Fenstersystem das Verhalten, wenn z. b. ein OpenGL-Fenster verdeckt ist.</span><span class="sxs-lookup"><span data-stu-id="526d4-109">With this test, the window system controls behavior when, for example, an OpenGL window is obscured.</span></span>

 

 




