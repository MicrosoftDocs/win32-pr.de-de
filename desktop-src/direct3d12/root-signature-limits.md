---
title: Stamm Signatur Limits
description: Bei der Stamm Signatur handelt es sich um Primzahlen, und es sind strikte Grenzwerte und Kosten zu beachten.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104146"
---
# <a name="root-signature-limits"></a><span data-ttu-id="00fc2-103">Stamm Signatur Limits</span><span class="sxs-lookup"><span data-stu-id="00fc2-103">Root Signature Limits</span></span>

<span data-ttu-id="00fc2-104">Bei der Stamm Signatur handelt es sich um Primzahlen, und es sind strikte Grenzwerte und Kosten zu beachten.</span><span class="sxs-lookup"><span data-stu-id="00fc2-104">The root signature is prime real estate, and there are strict limits and costs to consider.</span></span>

-   [<span data-ttu-id="00fc2-105">Arbeitsspeicher Grenzwerte und-Kosten</span><span class="sxs-lookup"><span data-stu-id="00fc2-105">Memory limits and costs</span></span>](#memory-limits-and-costs)
-   [<span data-ttu-id="00fc2-106">Leistungskosten</span><span class="sxs-lookup"><span data-stu-id="00fc2-106">Performance costs</span></span>](#performance-costs)
-   [<span data-ttu-id="00fc2-107">Statische Samplern</span><span class="sxs-lookup"><span data-stu-id="00fc2-107">Static samplers</span></span>](#static-samplers)
-   [<span data-ttu-id="00fc2-108">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="00fc2-108">Related topics</span></span>](#related-topics)

## <a name="memory-limits-and-costs"></a><span data-ttu-id="00fc2-109">Arbeitsspeicher Grenzwerte und-Kosten</span><span class="sxs-lookup"><span data-stu-id="00fc2-109">Memory limits and costs</span></span>

<span data-ttu-id="00fc2-110">Die maximale Größe einer Stamm Signatur beträgt 64 DWORDs.</span><span class="sxs-lookup"><span data-stu-id="00fc2-110">The maximum size of a root signature is 64 DWORDs.</span></span>

<span data-ttu-id="00fc2-111">Diese maximale Größe wird ausgewählt, um den Missbrauch der Stamm Signatur als Möglichkeit zum Speichern von Massendaten zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="00fc2-111">This maximum size is chosen to prevent abuse of the root signature as a way of storing bulk data.</span></span> <span data-ttu-id="00fc2-112">Jeder Eintrag in der Stamm Signatur hat eine Kosten für dieses 64 DWORD-Limit:</span><span class="sxs-lookup"><span data-stu-id="00fc2-112">Each entry in the root signature has a cost towards this 64 DWORD limit:</span></span>

-   <span data-ttu-id="00fc2-113">Deskriptortabellen Kosten jeweils 1 DWORD.</span><span class="sxs-lookup"><span data-stu-id="00fc2-113">Descriptor tables cost 1 DWORD each.</span></span>
-   <span data-ttu-id="00fc2-114">Stamm konstanten Kosten jeweils 1 DWORD, da es sich um 32-Bit-Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="00fc2-114">Root constants cost 1 DWORD each, since they are 32-bit values.</span></span>
-   <span data-ttu-id="00fc2-115">Stamm Deskriptoren (64-Bit-GPU-virtuelle Adressen) Kosten 2 DWords jeweils.</span><span class="sxs-lookup"><span data-stu-id="00fc2-115">Root descriptors (64-bit GPU virtual addresses) cost 2 DWORDs each.</span></span>

<span data-ttu-id="00fc2-116">Statische Samplern haben keine Kosten in der Größe der Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="00fc2-116">Static samplers do not have any cost in the size of the root signature.</span></span>

## <a name="performance-costs"></a><span data-ttu-id="00fc2-117">Leistungskosten</span><span class="sxs-lookup"><span data-stu-id="00fc2-117">Performance costs</span></span>

<span data-ttu-id="00fc2-118">Die Leistungseinbußen (im Hinblick auf dereferenzierungsstufen) sind für eine Stamm Konstante (1 für einen Stamm Deskriptor und 2 für eine Deskriptortabelle) gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="00fc2-118">The performance cost (in terms of levels of indirection) are zero for a root constant, 1 for a root descriptor, and 2 for a descriptor table.</span></span> <span data-ttu-id="00fc2-119">Wenn eine Stamm Signatur groß ist und aus dem schnellsten Arbeitsspeicher zu einem etwas langsameren Arbeitsspeicher fließt (was auf Hardware auftreten kann), fügen Sie den Leistungskosten für die überfließenden Elemente am Ende der Stamm Signatur 1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="00fc2-119">If a root signature is large and overflows out of the fastest memory into slightly slower memory (which can happen on some hardware), then add 1 to the performance cost for the overflowing items at the end of the root signature.</span></span>

<span data-ttu-id="00fc2-120">Ein Überlauf kann auf Hardware auftreten, die z. b. eine festgelegte Größe von 16 DWords für das Root-Argument Raum aufweisen könnte.</span><span class="sxs-lookup"><span data-stu-id="00fc2-120">An overflow can occur on hardware that might have, for example, a fixed size of 16 DWORDs for root argument space.</span></span> <span data-ttu-id="00fc2-121">Diese Beschränkung wird möglicherweise um 1 reduziert, wenn der Eingabe Assembler verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00fc2-121">This limit might be further reduced by one if the Input Assembler is used.</span></span> <span data-ttu-id="00fc2-122">In diesem Fall gibt es einen Überlauf in etwas langsameren Arbeitsspeicher, wenn die Stamm Signatur für den 15-oder 16-ten DWORD-Speicher zu groß ist.</span><span class="sxs-lookup"><span data-stu-id="00fc2-122">In this case there is overflow into slightly slower memory if the root signature is too large for the 15 or 16 DWORD native memory.</span></span> <span data-ttu-id="00fc2-123">In anderer Hardware gibt es keinen systeminternen Stamm Argument Speicher (d. h., die Überlauf Situation tritt nie auf).</span><span class="sxs-lookup"><span data-stu-id="00fc2-123">In other hardware there is no fixed native root argument memory (so the overflow situation never occurs).</span></span>

<span data-ttu-id="00fc2-124">Wenn sich ein root-Argument ändert, muss der Treiber für alle Hardware eine Version aller root-Argumente verwalten (im Gegensatz zu anderen speichern, wie z. b. deskriptorheaps und Puffer Ressourcen, die nicht vom Treiber versioniert werden).</span><span class="sxs-lookup"><span data-stu-id="00fc2-124">For all hardware, if any root argument changes, the driver must maintain a version of all the root arguments (unlike other storage such as descriptor heaps and buffer resources, which are not versioned by the driver).</span></span> <span data-ttu-id="00fc2-125">Bei der Hardware, bei der eine Überlauf Situation auftritt, muss nur der systemeigene oder Überlauf Bereich mit Versions Angabe versehen werden, je nachdem, wo die Änderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="00fc2-125">In hardware that an overflow situation occurs, only the native or overflow area needs to be versioned, depending on where the change occurred.</span></span> <span data-ttu-id="00fc2-126">Der Umfang der Versionsverwaltung sollte offensichtlich auf das erforderliche Minimum beschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="00fc2-126">The amount of versioning should obviously be kept to the necessary minimum.</span></span>

<span data-ttu-id="00fc2-127">Im Allgemeinen sollten Sie die folgenden Richtlinien beachten:</span><span class="sxs-lookup"><span data-stu-id="00fc2-127">Generally, consider the following guidelines:</span></span>

-   <span data-ttu-id="00fc2-128">Verwenden Sie bei Bedarf eine kleine Stamm Signatur, aber ausgleichen Sie dies mit der Flexibilität einer größeren Stamm Signatur.</span><span class="sxs-lookup"><span data-stu-id="00fc2-128">Use a small a root signature as necessary, though balance this with the flexibility of a larger root signature.</span></span>
-   <span data-ttu-id="00fc2-129">Anordnen von Parametern in einer großen Stamm Signatur, sodass die Parameter wahrscheinlich häufig geändert werden oder wenn eine geringe Zugriffs Latenz für einen bestimmten Parameter wichtig ist, treten zuerst auf.</span><span class="sxs-lookup"><span data-stu-id="00fc2-129">Arrange parameters in a large root signature so that the parameters most likely to change often, or if low access latency for a given parameter is important, occur first.</span></span>
-   <span data-ttu-id="00fc2-130">Verwenden Sie ggf. Stamm Konstanten oder Stamm Konstanten-Puffer Sichten, um konstante Puffer Sichten in einem deskriptorheap zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="00fc2-130">If convenient, use root constants or root constant buffer views over putting constant buffer views in a descriptor heap.</span></span>

## <a name="static-samplers"></a><span data-ttu-id="00fc2-131">Statische Samplern</span><span class="sxs-lookup"><span data-stu-id="00fc2-131">Static samplers</span></span>

<span data-ttu-id="00fc2-132">Statische Samplern (Samplern, bei denen der Zustand vollständig definiert und unveränderlich ist) sind Teil der Stamm Signaturen, werden jedoch nicht in Bezug auf das 64 DWORD-Limit gezählt.</span><span class="sxs-lookup"><span data-stu-id="00fc2-132">Static samplers (samplers where the state is fully defined and immutable) are part of root signatures, but do not count towards the 64 DWORD limit.</span></span> <span data-ttu-id="00fc2-133">Wenn ein Sampler als statisch definiert werden kann, ist es nicht erforderlich, dass der Sampler Teil eines deskriptorheaps ist.</span><span class="sxs-lookup"><span data-stu-id="00fc2-133">If a sampler can be defined as static, there is no need for the sampler to be part of a descriptor heap.</span></span>

<span data-ttu-id="00fc2-134">Es gibt keine Leistungseinbußen bei der Verwendung statischer Samplern, und eine Stamm Signatur kann eine Mischung aus statischen Samplern (gespeichert in der Stamm Signatur oder in reserviertem Speicherplatz auf Hardware) und dynamischen Samplern (die in einem Sampler-deskriptorheap gespeichert sind) enthalten.</span><span class="sxs-lookup"><span data-stu-id="00fc2-134">There is no performance cost to using static samplers, and a root signature can contain a mix of static samplers (stored in the root signature, or in reserved space on some hardware) and dynamic samplers (stored in a sampler descriptor heap).</span></span> <span data-ttu-id="00fc2-135">Samplern in einem deskriptorheap können dynamisch zugewiesen und indiziert werden, welche statischen Samplern nicht.</span><span class="sxs-lookup"><span data-stu-id="00fc2-135">Samplers in a descriptor heap can be dynamically assigned and indexed, which static samplers cannot.</span></span>

<span data-ttu-id="00fc2-136">Statische samplz können als Teil der Stamm Signatur in HLSL-Shadern geschrieben werden (Weitere Informationen finden Sie unter Angeben von Stamm [Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)).</span><span class="sxs-lookup"><span data-stu-id="00fc2-136">Static samplers can be written as part of the root signature in HLSL shaders (refer to [Specifying Root Signatures in HLSL](specifying-root-signatures-in-hlsl.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00fc2-137">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="00fc2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00fc2-138">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="00fc2-138">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




