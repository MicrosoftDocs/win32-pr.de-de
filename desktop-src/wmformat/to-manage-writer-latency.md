---
title: So verwalten Sie die Schreib Latenz
description: So verwalten Sie die Schreib Latenz
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF), Verwalten von Writer-Latenz
- ASF (Advanced Systems Format), Verwalten der Schreib Latenz
- Advanced Systems Format (ASF), Writer-Latenz
- ASF (Advanced Systems Format), Writer-Latenz
- Writer-Latenz
- latency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337415"
---
# <a name="to-manage-writer-latency"></a><span data-ttu-id="d5437-109">So verwalten Sie die Schreib Latenz</span><span class="sxs-lookup"><span data-stu-id="d5437-109">To Manage Writer Latency</span></span>

<span data-ttu-id="d5437-110">Es dauert eine Weile, bis der Writer Beispiele verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d5437-110">It takes time for the writer to process samples.</span></span> <span data-ttu-id="d5437-111">Die Zeitspanne zwischen dem übergeben einer Eingabe Stichprobe und dem Schreiben eines Ausgabe Beispiels wird als Latenz des Writers bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d5437-111">The amount of time between passing an input sample and the writing of an output sample is called the latency of the writer.</span></span> <span data-ttu-id="d5437-112">Eine Reihe von Faktoren tragen zur Schreib Latenz bei, und Sie können Sie auf verschiedene Weise verringern.</span><span class="sxs-lookup"><span data-stu-id="d5437-112">A number of factors contribute to writer latency, and you can reduce it in several ways.</span></span>

<span data-ttu-id="d5437-113">Der offensichtlichste Faktor bei der Writer-Latenz ist die Zeit, die zum Komprimieren eines Beispiels benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d5437-113">The most obvious factor involved in writer latency is the time it takes to compress a sample.</span></span> <span data-ttu-id="d5437-114">In den meisten Fällen haben Sie nur wenige oder keine Kontrolle über diese.</span><span class="sxs-lookup"><span data-stu-id="d5437-114">Under most circumstances, you will have little or no control over this.</span></span> <span data-ttu-id="d5437-115">Wenn die Bandbreite kein großes Problem ist, können Sie die Latenz verringern, indem Sie weniger Komprimierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5437-115">If bandwidth is not a big concern, you can reduce latency by using less compression.</span></span> <span data-ttu-id="d5437-116">Natürlich können Sie die geringste Latenz erzielen, indem Sie bereits komprimierte Beispiele übergeben.</span><span class="sxs-lookup"><span data-stu-id="d5437-116">Of course, you can achieve the least latency by passing samples that are already compressed.</span></span>

<span data-ttu-id="d5437-117">Der nächste Faktor und eine, über die Sie normalerweise steuern, ist die Reihenfolge, in der die Beispiele an den Reader übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5437-117">The next factor, and one over which you usually do have control, is the order in which samples are passed to the reader.</span></span> <span data-ttu-id="d5437-118">Sie können eine bessere Latenz erzielen, indem Sie Beispiele in der Reihenfolge der Präsentationszeit übergeben und sicherstellen, dass die Eingabe Beispiele zwischen allen Eingabedaten strömen gut synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d5437-118">You can achieve better latency by passing samples in order of presentation time, and by ensuring that the input samples are well synchronized between all input streams.</span></span> <span data-ttu-id="d5437-119">Je größer die Diskrepanz in den Präsentations Zeiten zwischen den Beispielen für verschiedene Streams, desto mehr Latenz ergibt sich.</span><span class="sxs-lookup"><span data-stu-id="d5437-119">The greater the discrepancy in presentation times between the samples for different streams, the more latency will result.</span></span> <span data-ttu-id="d5437-120">Sie können einen maximalen Wert für die Abweichung zwischen den Eingabe Beispielen festlegen, indem Sie [**iwmschreiteradvanced:: setsynctolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d5437-120">You can set a maximum for the discrepancy between input samples by calling [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5437-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d5437-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5437-122">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="d5437-122">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




