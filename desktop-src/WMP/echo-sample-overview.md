---
title: Übersicht über das Echo Beispiel
description: Übersicht über das Echo Beispiel
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Windows Media Player-Plug-ins, Übersicht über ECHO Beispiele
- Plug-ins, Echo Sample Overview
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Overview
- DSP-Plug-ins, Übersicht über ECHO Beispiele
- Echo DSP-Plug-in-Beispiel, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341255"
---
# <a name="echo-sample-overview"></a><span data-ttu-id="76774-108">Übersicht über das Echo Beispiel</span><span class="sxs-lookup"><span data-stu-id="76774-108">Echo Sample Overview</span></span>

<span data-ttu-id="76774-109">Dieser Leitfaden erstellt ein Windows Media Player DSP-Plug-in, das während der Wiedergabe einen Echo Effekt in PCM-Audiodaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="76774-109">This guide builds a Windows Media Player DSP plug-in that creates an echo effect in PCM audio during playback.</span></span> <span data-ttu-id="76774-110">Die Ziele für das Plug-in lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="76774-110">The goals for the plug-in are as follows:</span></span>

-   <span data-ttu-id="76774-111">Das Plug-in verarbeitet nur 8-Bit-oder 16-Bit-PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="76774-111">The plug-in processes 8-bit or 16-bit PCM audio only.</span></span>
-   <span data-ttu-id="76774-112">Sie unterstützt eine Verzögerungszeit zwischen 10 Millisekunden (MS) und 2000 ms (2 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="76774-112">It supports a delay time between 10 milliseconds (ms) and 2000 ms (2 seconds).</span></span> <span data-ttu-id="76774-113">Dies steht für die meisten Anwendungen für einen praktischen Bereich.</span><span class="sxs-lookup"><span data-stu-id="76774-113">This represents a practical range for most applications.</span></span>
-   <span data-ttu-id="76774-114">Sie unterstützt das Mischen des ursprünglichen Signals mit dem Verzögerungs Signal.</span><span class="sxs-lookup"><span data-stu-id="76774-114">It supports mixing of the original signal with the delay signal.</span></span>
-   <span data-ttu-id="76774-115">Sie stellt eine Implementierung der Eigenschaften Seite bereit, die es dem Benutzer ermöglicht, einen Wert für die Verzögerungszeit und einen Wert für den Prozentsatz des Verzögerungs Signals in Relation zur gesamten audiosignalstufe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="76774-115">It provides a property page implementation that allows the user to provide a value for the delay time and a value for the percentage of delay signal relative to the overall audio signal level.</span></span>
-   <span data-ttu-id="76774-116">Der Code wird erstellt, indem der Plug-in-Beispiel für den Windows Media Player-Plug-in-Assistent geändert wird.</span><span class="sxs-lookup"><span data-stu-id="76774-116">The code is created by modifying the Windows Media Player Plug-in Wizard audio DSP plug-in sample.</span></span>

<span data-ttu-id="76774-117">Das Echo-Beispiel ist nicht im Windows Media Player SDK enthalten. Es handelt sich um ein Beispiel, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="76774-117">The Echo sample is not included with the Windows Media Player SDK; it is a sample that you create.</span></span> <span data-ttu-id="76774-118">Um das Echo-Beispiel zu erstellen, müssen Sie mit dem Standard Projekt im Assistenten für Windows-Media Player-Plug-in beginnen.</span><span class="sxs-lookup"><span data-stu-id="76774-118">To create the Echo sample, you must start with the default project from the Windows Media Player Plug-in Wizard.</span></span> <span data-ttu-id="76774-119">Sie können das Projekt beliebig benennen. in dieser Dokumentation wird davon ausgegangen, dass das Projekt Echo lautet.</span><span class="sxs-lookup"><span data-stu-id="76774-119">You can name the project whatever you like; this documentation assumes the project is named Echo.</span></span> <span data-ttu-id="76774-120">Ausführliche Informationen zur Verwendung des Assistenten finden Sie unter [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="76774-120">For details about using the wizard, see [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span></span>

<span data-ttu-id="76774-121">Der folgende Abschnitt enthält eine Übersicht über die Erstellung eines ECHO Effekts durch das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="76774-121">The following section provides an overview of how the sample creates an echo effect:</span></span>

-   [<span data-ttu-id="76774-122">Funktionsweise des Echo-Beispiels</span><span class="sxs-lookup"><span data-stu-id="76774-122">How the Echo Sample Works</span></span>](how-the-echo-sample-works.md)

## <a name="related-topics"></a><span data-ttu-id="76774-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76774-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76774-124">**Das Echo-Beispiel**</span><span class="sxs-lookup"><span data-stu-id="76774-124">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




