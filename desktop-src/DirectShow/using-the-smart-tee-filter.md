---
description: Verwenden des Smart Tee-Filters
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Verwenden des Smart Tee-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373141"
---
# <a name="using-the-smart-tee-filter"></a><span data-ttu-id="80092-103">Verwenden des Smart Tee-Filters</span><span class="sxs-lookup"><span data-stu-id="80092-103">Using the Smart Tee Filter</span></span>

<span data-ttu-id="80092-104">Wenn für einen Erfassungs Filter separate Erfassungs-und Vorschau Pins verfügbar sind, können Sie von einem Erfassungs Filter erfassen, während Sie die Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="80092-104">If a capture filter has separate capture and preview pins, you can capture from one while previewing from the other.</span></span> <span data-ttu-id="80092-105">Wenn der Filter jedoch keine Vorschau-Pin hat, können Sie das gleiche tun, indem Sie den [Smart Tee](smart-tee-filter.md) -Filter in das Diagramm einschließen.</span><span class="sxs-lookup"><span data-stu-id="80092-105">But if the filter has no preview pin, you can do the same thing by including the [Smart Tee](smart-tee-filter.md) filter in the graph.</span></span> <span data-ttu-id="80092-106">Dieser Filter teilt die Daten aus dem Erfassungs-PIN in zwei identische Datenströme auf, einen für Capture und einen für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="80092-106">This filter splits data from the capture pin into two identical streams, one for capture and one for preview.</span></span> <span data-ttu-id="80092-107">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="80092-107">The following diagram illustrates this process.</span></span>

![Diagramm mit Smart Tee-Filter erfassen](images/vidcap05.png)

<span data-ttu-id="80092-109">Die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode fügt ggf. automatisch den intelligenten Tee-Filter ein.</span><span class="sxs-lookup"><span data-stu-id="80092-109">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Smart Tee Filter if it is required.</span></span> <span data-ttu-id="80092-110">Wenn Sie jedoch **igraphbuilder** -Methoden verwenden, um das Diagramm zu erstellen, und nicht **RenderStream**, müssen Sie möglicherweise den Smart Tee-Filter einfügen.</span><span class="sxs-lookup"><span data-stu-id="80092-110">However, if you use **IGraphBuilder** methods to build your graph, and not **RenderStream**, you may need to insert the Smart Tee filter.</span></span>

<span data-ttu-id="80092-111">Überprüfen Sie vor dem Rendering von Pins im Erfassungs Filter, ob der Filter eine Vorschau-PIN oder eine Videoport-Pin aufweist.</span><span class="sxs-lookup"><span data-stu-id="80092-111">Before you render pins on the capture filter, check whether the filter has a preview pin or a video port pin.</span></span> <span data-ttu-id="80092-112">Wenn dies nicht der Fall ist und Sie eine Vorschau anzeigen möchten, fügen Sie dem Diagramm den intelligenten Tee-Filter hinzu, und verbinden Sie ihn mit der Erfassungs-PIN im Erfassungs Filter.</span><span class="sxs-lookup"><span data-stu-id="80092-112">If it does not, and you wish to preview, add the Smart Tee filter to the graph and connect it to the capture pin on the capture filter.</span></span>

> [!Note]  
> <span data-ttu-id="80092-113">Sie können eine textport-PIN (VP) als eine Art von Vorschau-Pin behandeln, sodass ein Filter mit einer VP-Pin keinen intelligenten Tee-Filter benötigt.</span><span class="sxs-lookup"><span data-stu-id="80092-113">You can treat a video port (VP) pin as a kind of preview pin, so a filter with a VP pin does not need a Smart Tee filter.</span></span> <span data-ttu-id="80092-114">Allerdings haben VP Pins einige andere besondere Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="80092-114">However, VP pins have some other special requirements.</span></span> <span data-ttu-id="80092-115">Weitere Informationen finden Sie unter [Video Port Pins](video-port-pins.md).</span><span class="sxs-lookup"><span data-stu-id="80092-115">For more information, see [Video Port Pins](video-port-pins.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="80092-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80092-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80092-117">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="80092-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="80092-118">Kombinieren von Video Erfassung und Vorschau</span><span class="sxs-lookup"><span data-stu-id="80092-118">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="80092-119">Arbeiten mit PIN-Kategorien</span><span class="sxs-lookup"><span data-stu-id="80092-119">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 



