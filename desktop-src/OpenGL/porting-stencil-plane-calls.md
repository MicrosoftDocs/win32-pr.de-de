---
title: Portieren von Schablonen der Schablone
description: In OpenGL weisen Sie Schablone-Ebenen zu, indem Sie das entsprechende Pixel Format mit dem OpenGL-Format "", "
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- IRIS GL portieren, Schablone-Ebenen
- Portieren von IRIS GL, Schablone-Ebenen
- Portieren auf OpenGL von IRIS GL, Schablone-Ebenen
- OpenGL-Portierung von IRIS GL, Schablone-Ebenen
- Schablone-Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310540"
---
# <a name="porting-stencil-plane-calls"></a><span data-ttu-id="9bee2-108">Portieren von Schablonen der Schablone</span><span class="sxs-lookup"><span data-stu-id="9bee2-108">Porting Stencil Plane Calls</span></span>

<span data-ttu-id="9bee2-109">In OpenGL weisen Sie Schablone-Ebenen zu, indem Sie das entsprechende Pixel Format mit dem **OpenGL-** [**Format "**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)", "</span><span class="sxs-lookup"><span data-stu-id="9bee2-109">In OpenGL, you allocate stencil planes by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span> <span data-ttu-id="9bee2-110">Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9bee2-110">functions.</span></span> <span data-ttu-id="9bee2-111">In der folgenden Tabelle sind die Funktionen von IRIS GL aufgeführt, die sich auf die Schablone-Ebenen und ihre entsprechenden OpenGL-Funktionen auswirken.</span><span class="sxs-lookup"><span data-stu-id="9bee2-111">The following table lists IRIS GL functions that affect the stencil planes and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="9bee2-112">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="9bee2-112">IRIS GL function</span></span>             | <span data-ttu-id="9bee2-113">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="9bee2-113">OpenGL function</span></span>                                         | <span data-ttu-id="9bee2-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9bee2-114">Meaning</span></span>                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="9bee2-115">**Schablone**</span><span class="sxs-lookup"><span data-stu-id="9bee2-115">**stensize**</span></span>                 | <span data-ttu-id="9bee2-116">**Auswahl Pixel Format**</span><span class="sxs-lookup"><span data-stu-id="9bee2-116">**ChoosePixelFormat**</span></span>                                   |                                                        |
| <span data-ttu-id="9bee2-117">**Schablone**( **true**,...)</span><span class="sxs-lookup"><span data-stu-id="9bee2-117">**stencil**( **TRUE**, ... )</span></span> | <span data-ttu-id="9bee2-118">[**glEnable**](glenable.md) (GL- \_ Schablone- \_ Test)</span><span class="sxs-lookup"><span data-stu-id="9bee2-118">[**glEnable**](glenable.md) ( GL\_STENCIL\_TEST )</span></span>      | <span data-ttu-id="9bee2-119">Aktiviert Schablonen Tests.</span><span class="sxs-lookup"><span data-stu-id="9bee2-119">Enables stencil tests.</span></span>                                 |
| <span data-ttu-id="9bee2-120">**Schablone**</span><span class="sxs-lookup"><span data-stu-id="9bee2-120">**stencil**</span></span>                  | [<span data-ttu-id="9bee2-121">**glstencilop**</span><span class="sxs-lookup"><span data-stu-id="9bee2-121">**glStencilOp**</span></span>](glstencilop.md)                      | <span data-ttu-id="9bee2-122">Legt Schablone-Test Aktionen fest.</span><span class="sxs-lookup"><span data-stu-id="9bee2-122">Sets stencil test actions.</span></span>                             |
| <span data-ttu-id="9bee2-123">**Schablone**(... Func,...)</span><span class="sxs-lookup"><span data-stu-id="9bee2-123">**stencil**(... func, ... )</span></span>  | [<span data-ttu-id="9bee2-124">**glstencilfunc**</span><span class="sxs-lookup"><span data-stu-id="9bee2-124">**glStencilFunc**</span></span>](glstencilfunc.md)                  | <span data-ttu-id="9bee2-125">Legt die Funktion und den Verweis Wert für das Testen der Schablone fest.</span><span class="sxs-lookup"><span data-stu-id="9bee2-125">Sets function and reference value for stencil testing.</span></span> |
| <span data-ttu-id="9bee2-126">**sschreibfrage**</span><span class="sxs-lookup"><span data-stu-id="9bee2-126">**swritemask**</span></span>               | [<span data-ttu-id="9bee2-127">**glstencilmask**</span><span class="sxs-lookup"><span data-stu-id="9bee2-127">**glStencilMask**</span></span>](glstencilmask.md)                  | <span data-ttu-id="9bee2-128">Gibt an, welche Schablonen Bits geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="9bee2-128">Specifies which stencil bits can be written.</span></span>           |
|                              | [<span data-ttu-id="9bee2-129">**glclearstencil**</span><span class="sxs-lookup"><span data-stu-id="9bee2-129">**glClearStencil**</span></span>](glclearstencil.md)                | <span data-ttu-id="9bee2-130">Gibt den eindeutigen Wert für den Schablonen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="9bee2-130">Specifies the clear value for the stencil buffer.</span></span>      |
| <span data-ttu-id="9bee2-131">**sClear**</span><span class="sxs-lookup"><span data-stu-id="9bee2-131">**sclear**</span></span>                   | <span data-ttu-id="9bee2-132">[**glClear**](glclear.md) (GL- \_ Schablone- \_ Puffer \_ Bit)</span><span class="sxs-lookup"><span data-stu-id="9bee2-132">[**glClear**](glclear.md) ( GL\_STENCIL\_BUFFER\_BIT )</span></span> |                                                        |



 

<span data-ttu-id="9bee2-133">Schablone: Vergleichsfunktionen und Schablonen Durchlauf-/Fehlervorgänge sind fast Äquivalent in OpenGL und IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="9bee2-133">Stencil-comparison functions and stencil pass/fail operations are nearly equivalent in OpenGL and IRIS GL.</span></span> <span data-ttu-id="9bee2-134">Die Iris GL Stencil-funktionsflags werden mit SF vorangestellt. die OpenGL-Flags mit GL.</span><span class="sxs-lookup"><span data-stu-id="9bee2-134">The IRIS GL stencil-function flags are prefaced with SF; the OpenGL flags with GL.</span></span> <span data-ttu-id="9bee2-135">Bei Iris GL Pass/Fail-Vorgangs Flags wird "St;" vorangestellt. die OpenGL-Flags mit GL.</span><span class="sxs-lookup"><span data-stu-id="9bee2-135">IRIS GL pass/fail operation flags are prefaced with ST; the OpenGL flags with GL.</span></span>

 

 




