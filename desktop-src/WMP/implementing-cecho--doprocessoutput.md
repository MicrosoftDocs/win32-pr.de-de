---
title: Implementieren von Cecho DoProcess Output
description: Implementieren von Cecho DoProcess Output
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037596"
---
# <a name="implementing-cechodoprocessoutput"></a><span data-ttu-id="56c57-108">Implementieren von Cecho::D oprocess Output</span><span class="sxs-lookup"><span data-stu-id="56c57-108">Implementing CEcho::DoProcessOutput</span></span>

<span data-ttu-id="56c57-109">Die Methode " **DoProcess Output** " führt die digitale Signalverarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="56c57-109">The **DoProcessOutput** method performs the digital signal processing.</span></span> <span data-ttu-id="56c57-110">Dies ist die Methode, die die Änderungen an den Daten vornimmt, die von Windows Media Player bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="56c57-110">This is the method that makes the changes to the data provided by Windows Media Player.</span></span> <span data-ttu-id="56c57-111">Dies sind die Ergebnisse dieser Methode, die Sie als Echo Effekt hören, wenn Ihr Echo Sample-Plug-in fertig ist.</span><span class="sxs-lookup"><span data-stu-id="56c57-111">It is the results of this method that you will hear as an echo effect when your Echo sample plug-in is complete.</span></span>

<span data-ttu-id="56c57-112">In diesem Beispiel verarbeitet das Plug-in nur 8-Bit-oder 16-Bit-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="56c57-112">For this sample, the plug-in will only process 8-bit or 16-bit audio.</span></span> <span data-ttu-id="56c57-113">Sie müssen einige Änderungen am Beispielcode des Plug-in-Assistenten vornehmen, um die Abschnitte zu entfernen, in denen ein höheres bidirektionalton verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="56c57-113">You will need to make some changes to the plug-in wizard sample code to remove the sections that process higher bit depth audio.</span></span> <span data-ttu-id="56c57-114">Es lohnt sich jedoch, diese Abschnitte zu untersuchen, da Sie sich entscheiden können, eine eigene Echo Implementierung für diese Formate hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="56c57-114">It is worthwhile to study these sections, however, because you may decide to add your own echo implementation for those formats.</span></span>

<span data-ttu-id="56c57-115">In den folgenden Abschnitten werden die Änderungen beschrieben, die Sie am Code vornehmen müssen:</span><span class="sxs-lookup"><span data-stu-id="56c57-115">The following sections detail the changes you need to make to the code:</span></span>

-   [<span data-ttu-id="56c57-116">Entfernen des Codes für die Verarbeitung von mehr als 16 Bits</span><span class="sxs-lookup"><span data-stu-id="56c57-116">Removing the Code to Process Greater than 16 Bits</span></span>](removing-the-code-to-process-greater-than-16-bits.md)
-   [<span data-ttu-id="56c57-117">Verarbeiten der Audiodaten</span><span class="sxs-lookup"><span data-stu-id="56c57-117">Processing the Audio Data</span></span>](processing-the-audio-data.md)
-   [<span data-ttu-id="56c57-118">Variablen zum Durchführen der Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="56c57-118">Variables to Perform Processing</span></span>](variables-to-perform-processing.md)
-   [<span data-ttu-id="56c57-119">Erstellen des Echo Effekts</span><span class="sxs-lookup"><span data-stu-id="56c57-119">Creating the Echo Effect</span></span>](creating-the-echo-effect.md)

## <a name="related-topics"></a><span data-ttu-id="56c57-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56c57-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56c57-121">**Das Echo-Beispiel**</span><span class="sxs-lookup"><span data-stu-id="56c57-121">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




