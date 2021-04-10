---
title: Ausführen von Auswahl und Feedback
description: Ausführen von Auswahl und Feedback
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, Auswahl
- OpenGL, Feedback
- OpenGL, Rendering
- Auswahlmodus OpenGL
- Feedback Modus OpenGL
- Renderingmodus OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310039"
---
# <a name="performing-selection-and-feedback"></a><span data-ttu-id="2c465-109">Ausführen von Auswahl und Feedback</span><span class="sxs-lookup"><span data-stu-id="2c465-109">Performing Selection and Feedback</span></span>

<span data-ttu-id="2c465-110">Auswahl, Feedback und Rendering sind sich gegenseitig ausschließende Betriebsmodi.</span><span class="sxs-lookup"><span data-stu-id="2c465-110">Selection, feedback, and rendering are mutually exclusive modes of operation.</span></span> <span data-ttu-id="2c465-111">Rendering ist der normale Standardmodus, in dem Fragmente durch rasterization erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c465-111">Rendering is the normal, default mode during which fragments are produced by rasterization.</span></span>

<span data-ttu-id="2c465-112">Im Auswahl-und Feedback Modus werden keine Fragmente erzeugt. Daher findet keine Frame Puffer-Änderung statt.</span><span class="sxs-lookup"><span data-stu-id="2c465-112">In selection and feedback modes, no fragments are produced; therefore, no framebuffer modification occurs.</span></span> <span data-ttu-id="2c465-113">Im Auswahlmodus können Sie feststellen, welche primitiven in einem Fensterbereich gezeichnet werden. im Feedback Modus werden Informationen über primitive, die gerengt werden, an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c465-113">In selection mode, you can determine which primitives will be drawn into some region of a window; in feedback mode, information about primitives that will be rasterized is fed back to the application.</span></span>

<span data-ttu-id="2c465-114">Mit [**glrendermode**](glrendermode.md)wählen Sie zwischen diesen drei Modi aus.</span><span class="sxs-lookup"><span data-stu-id="2c465-114">You select among these three modes with [**glRenderMode**](glrendermode.md).</span></span>

-   [<span data-ttu-id="2c465-115">Auswahl</span><span class="sxs-lookup"><span data-stu-id="2c465-115">Selection</span></span>](selection.md)
-   [<span data-ttu-id="2c465-116">Feedback</span><span class="sxs-lookup"><span data-stu-id="2c465-116">Feedback</span></span>](feedback.md)
-   [<span data-ttu-id="2c465-117">Auswahl-und Feedback Referenz</span><span class="sxs-lookup"><span data-stu-id="2c465-117">Selection and Feedback Reference</span></span>](selection-and-feedback-reference.md)

 

 




