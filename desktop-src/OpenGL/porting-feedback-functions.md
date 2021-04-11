---
title: Portieren von Feedback Funktionen
description: Mit Iris GL unterscheidet sich die Art und Weise, wie Feedback behandelt wird, abhängig vom Computer, auf dem IRIS GL ausgeführt wird.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- IRIS GL Porting, Feedback
- Portieren von IRIS GL, Feedback
- Portieren auf OpenGL von IRIS GL, Feedback
- OpenGL-Portierung von IRIS GL, Feedback
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207152"
---
# <a name="porting-feedback-functions"></a><span data-ttu-id="7653b-108">Portieren von Feedback Funktionen</span><span class="sxs-lookup"><span data-stu-id="7653b-108">Porting Feedback Functions</span></span>

<span data-ttu-id="7653b-109">Mit Iris GL unterscheidet sich die Art und Weise, wie Feedback behandelt wird, abhängig vom Computer, auf dem IRIS GL ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7653b-109">With IRIS GL, the way that feedback is handled differs depending on the computer running IRIS GL.</span></span> <span data-ttu-id="7653b-110">OpenGL vereinheitlicht die Feedback Funktionen, sodass Sie sich auf ein konsistentes Feedback zwischen verschiedenen Hardwareplattformen verlassen können.</span><span class="sxs-lookup"><span data-stu-id="7653b-110">OpenGL standardizes feedback functions so you can rely on consistent feedback among various hardware platforms.</span></span> <span data-ttu-id="7653b-111">In der folgenden Tabelle werden die-Feedback Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7653b-111">The following table lists the IRIS GL feedback functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="7653b-112">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="7653b-112">IRIS GL function</span></span> | <span data-ttu-id="7653b-113">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="7653b-113">OpenGL function</span></span>                                                                                            | <span data-ttu-id="7653b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7653b-114">Meaning</span></span>                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="7653b-115">**Backs**</span><span class="sxs-lookup"><span data-stu-id="7653b-115">**feedback**</span></span>     | <span data-ttu-id="7653b-116">[**glrendermode**](glrendermode.md) (GL- \_ Feedback)</span><span class="sxs-lookup"><span data-stu-id="7653b-116">[**glRenderMode**](glrendermode.md) ( GL\_FEEDBACK )</span></span>                                                      | <span data-ttu-id="7653b-117">Wechselt in den Feedback Modus.</span><span class="sxs-lookup"><span data-stu-id="7653b-117">Switches to feedback mode.</span></span>                    |
| <span data-ttu-id="7653b-118">**endfeedback**</span><span class="sxs-lookup"><span data-stu-id="7653b-118">**endfeedback**</span></span>  | <span data-ttu-id="7653b-119">[**glrendermode**](glrendermode.md) (GL- \_ Rendering)[**glfeedbackbuffer**](glfeedbackbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="7653b-119">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span></span><br/> | <span data-ttu-id="7653b-120">Wechselt in den Renderingmodus.</span><span class="sxs-lookup"><span data-stu-id="7653b-120">Switches to rendering mode.</span></span>                   |
| <span data-ttu-id="7653b-121">**Passthrough**</span><span class="sxs-lookup"><span data-stu-id="7653b-121">**passthrough**</span></span>  | [<span data-ttu-id="7653b-122">**glpassthrough**</span><span class="sxs-lookup"><span data-stu-id="7653b-122">**glPassThrough**</span></span>](glpassthrough.md)                                                                     | <span data-ttu-id="7653b-123">Platziert einen tokenmarker im Feedback Puffer.</span><span class="sxs-lookup"><span data-stu-id="7653b-123">Places a token marker in the feedback buffer.</span></span> |



 

 

 





