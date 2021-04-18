---
description: Berechnen von Parameter Werten
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Berechnen von Parameter Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341106"
---
# <a name="calculating-parameter-values"></a><span data-ttu-id="97618-103">Berechnen von Parameter Werten</span><span class="sxs-lookup"><span data-stu-id="97618-103">Calculating Parameter Values</span></span>

<span data-ttu-id="97618-104">Möglicherweise kann ein Eingabepuffer sehr groß sein.</span><span class="sxs-lookup"><span data-stu-id="97618-104">Potentially, an input buffer could be very large.</span></span> <span data-ttu-id="97618-105">Wenn der DMO den Puffer verarbeitet, werden die Parameter im Idealfall genau auf die Kurven im gesamten Datenstapel folgen.</span><span class="sxs-lookup"><span data-stu-id="97618-105">Ideally, when the DMO processes the buffer, the parameters will exactly follow their curves throughout the entire batch of data.</span></span> <span data-ttu-id="97618-106">Ein DMO hat jedoch gewisse Spielraum bei der Berechnung dieser Werte.</span><span class="sxs-lookup"><span data-stu-id="97618-106">However, a DMO has some leeway in how it calculates those values.</span></span>

-   <span data-ttu-id="97618-107">Der präzisere Ansatz besteht darin, den exakten Wert für jede atomarische Dateneinheit zu berechnen. beispielsweise jedes Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="97618-107">The most accurate approach is to calculate the exact value for every atomic unit of data; for example, each audio sample.</span></span> <span data-ttu-id="97618-108">Diese Vorgehensweise ist am Rechen intensivsten.</span><span class="sxs-lookup"><span data-stu-id="97618-108">This approach is the most computationally expensive.</span></span>
-   <span data-ttu-id="97618-109">Ein anderer Ansatz besteht darin, die Daten in kleinere Einheiten mit fester Größe, z. b. 100-Stichproben, aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="97618-109">Another approach is to slice the data into smaller units of some fixed size, such as 100 samples.</span></span> <span data-ttu-id="97618-110">Bei diesem Ansatz wird ein "Stair-Step"-Effekt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="97618-110">This approach creates a "stair-stepping" effect.</span></span> <span data-ttu-id="97618-111">Bei einigen Parametern ist das möglicherweise akzeptabel.</span><span class="sxs-lookup"><span data-stu-id="97618-111">For some parameters, that might be acceptable.</span></span> <span data-ttu-id="97618-112">In Audioeffekten könnte es akustische Artefakte erstellen.</span><span class="sxs-lookup"><span data-stu-id="97618-112">In audio effects, it might create audible artifacts.</span></span>
-   <span data-ttu-id="97618-113">Eine Gefährdung besteht darin, das vorherige Verfahren zu verwenden, aber innerhalb jedes Batches eine lineare interpolung des Parameter Werts für jede Stichprobe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="97618-113">A compromise is to use the previous technique, but within each batch, perform a linear interpolation of the parameter value for each sample.</span></span>

<span data-ttu-id="97618-114">Diese Probleme sind besonders wichtig für die Audioverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="97618-114">These issues are especially important for audio processing.</span></span> <span data-ttu-id="97618-115">Eine Sekunde Audioinformationen können 48.000 Audiobeispiele pro Kanal enthalten. Dies ist eine Vielzahl von Berechnungen, die durchgeführt werden müssen, aber das Ohr ist für Artefakte wie Aliasing sensibel.</span><span class="sxs-lookup"><span data-stu-id="97618-115">One second of audio might contain 48,000 audio samples per channel, which is a lot of calculations to perform, yet the ear is sensitive to artifacts such as aliasing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97618-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97618-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97618-117">Medien Parameter</span><span class="sxs-lookup"><span data-stu-id="97618-117">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



