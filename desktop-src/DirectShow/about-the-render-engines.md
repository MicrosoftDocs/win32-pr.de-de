---
description: Informationen zu den renderengines
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Informationen zu den renderengines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522235"
---
# <a name="about-the-render-engines"></a><span data-ttu-id="bcf53-103">Informationen zu den renderengines</span><span class="sxs-lookup"><span data-stu-id="bcf53-103">About the Render Engines</span></span>

<span data-ttu-id="bcf53-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="bcf53-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="bcf53-105">In diesem Artikel wird beschrieben, wie [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) (des) ein Video Bearbeitungs Projekt rendern.</span><span class="sxs-lookup"><span data-stu-id="bcf53-105">This article describes how [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project.</span></span>

<span data-ttu-id="bcf53-106">In des wird ein Projekt als Zeitachse dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bcf53-106">In DES, a project is represented as a timeline.</span></span> <span data-ttu-id="bcf53-107">Die Zeitachse ist nützlich, da Sie die gängigsten Aufgaben bei der Videobearbeitung vereinfacht, z. b. das Ändern von Quell Clips und das Hinzufügen von Video Effekten</span><span class="sxs-lookup"><span data-stu-id="bcf53-107">The timeline is useful because it simplifies the most common tasks in video editing, such as rearranging source clips and adding video effects.</span></span> <span data-ttu-id="bcf53-108">Die DirectShow-streamarchitektur erfordert dagegen ein Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="bcf53-108">The DirectShow stream architecture, on the other hand, requires a filter graph.</span></span> <span data-ttu-id="bcf53-109">Daher müssen Sie zum Rendering des Projekts eine Zeitachse in ein Filter Diagramm übersetzen.</span><span class="sxs-lookup"><span data-stu-id="bcf53-109">Thus, to render your project, you must translate a timeline into a filter graph.</span></span> <span data-ttu-id="bcf53-110">Die Komponente, die dies bewirkt, wird als *Rendering-Engine* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bcf53-110">The component that does this is called a *render engine*.</span></span> <span data-ttu-id="bcf53-111">DirectShow bietet zwei renderengines:</span><span class="sxs-lookup"><span data-stu-id="bcf53-111">DirectShow provides two render engines:</span></span>

-   <span data-ttu-id="bcf53-112">Grundlegende Rendering-Engine: erstellt ein Filter Diagramm, das eine nicht komprimierte Ausgabe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bcf53-112">Basic render engine: Builds a filter graph that delivers uncompressed output.</span></span>
-   <span data-ttu-id="bcf53-113">Smart-Rendering-Engine: erstellt ein Filter Diagramm, das eine komprimierte Ausgabe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bcf53-113">Smart render engine: Builds a filter graph that delivers compressed output.</span></span>

<span data-ttu-id="bcf53-114">Die Smart-Rendering-Engine verwendet die intelligente Neukomprimierung zur Verbesserung der Leistung.</span><span class="sxs-lookup"><span data-stu-id="bcf53-114">The smart render engine uses smart recompression to improve performance.</span></span> <span data-ttu-id="bcf53-115">Bei der intelligenten Neukomprimierung werden Quelldateien nur dann erneut komprimiert, wenn sich das ursprüngliche Dateiformat vom endgültigen Ausgabeformat unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="bcf53-115">With smart recompression, source files are recompressed only when the original file format differs from the final output format.</span></span> <span data-ttu-id="bcf53-116">Wenn die Formate Stimmen, wird die Quelle nie entpackt.</span><span class="sxs-lookup"><span data-stu-id="bcf53-116">If the formats match, the source is never decompressed.</span></span> <span data-ttu-id="bcf53-117">Die intelligente Neukomprimierung wird nur für die Video Komprimierung und nicht für die Audiokomprimierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcf53-117">Smart recompression is supported only for video compression, not for audio compression.</span></span>

<span data-ttu-id="bcf53-118">Verwenden Sie für die Vorschauversion die einfache Renderingengine.</span><span class="sxs-lookup"><span data-stu-id="bcf53-118">For preview, use the basic render engine.</span></span> <span data-ttu-id="bcf53-119">Die intelligente Renderingengine kann auch eine Vorschau anzeigen, aber weniger effizient, da Sie den komprimierten Datenstrom dekomprimieren muss.</span><span class="sxs-lookup"><span data-stu-id="bcf53-119">The smart render engine can also preview, but less efficiently because it has to decompress the compressed stream.</span></span> <span data-ttu-id="bcf53-120">Verwenden Sie zum Schreiben von Dateien die Smart-Rendering-Engine, wenn Sie eine intelligente Neukomprimierung wünschen.</span><span class="sxs-lookup"><span data-stu-id="bcf53-120">For writing files, use the smart render engine if you want smart recompression.</span></span> <span data-ttu-id="bcf53-121">Verwenden Sie andernfalls die einfache Renderingengine.</span><span class="sxs-lookup"><span data-stu-id="bcf53-121">Otherwise, use the basic render engine.</span></span> <span data-ttu-id="bcf53-122">Die intelligente Neukomprimierung kann den Zeitaufwand für das Schreiben der Datei erheblich verkürzen.</span><span class="sxs-lookup"><span data-stu-id="bcf53-122">Smart recompression can greatly reduce the time it takes to write the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bcf53-123">Verwenden Sie die Smart-Rendering-Engine nicht zum Lesen oder Schreiben von Windows Media-Dateien.</span><span class="sxs-lookup"><span data-stu-id="bcf53-123">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="bcf53-124">Beide renderingengines erstellen ein unsichtbares Fenster, das Nachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bcf53-124">Both render engines create an invisible window that processes messages.</span></span> <span data-ttu-id="bcf53-125">Der Thread, der die Renderingengine erstellt, muss über eine Nachrichten Schleife verfügen, um Nachrichten zu senden.</span><span class="sxs-lookup"><span data-stu-id="bcf53-125">The thread that creates the render engine must have a message loop, to dispatch messages.</span></span> <span data-ttu-id="bcf53-126">Außerdem darf der Thread erst beendet werden, wenn die Renderingengine und der Filter-Graph-Manager freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bcf53-126">Also, that thread must not exit until the Render Engine and the Filter Graph Manager are released.</span></span> <span data-ttu-id="bcf53-127">Andernfalls könnte die Anwendung einen Deadlock verursachen.</span><span class="sxs-lookup"><span data-stu-id="bcf53-127">Otherwise, the application might deadlock.</span></span>

 

<span data-ttu-id="bcf53-128">Erstellen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="bcf53-128">Constructing the Filter Graph</span></span>

<span data-ttu-id="bcf53-129">Das Filter Diagramm wird in zwei Phasen erstellt.</span><span class="sxs-lookup"><span data-stu-id="bcf53-129">The filter graph is built in two stages.</span></span> <span data-ttu-id="bcf53-130">In der ersten Phase erstellt die Renderengine ein "Front-End", bei dem es sich um ein partielles Filter Diagramm handelt.</span><span class="sxs-lookup"><span data-stu-id="bcf53-130">In the first stage, the render engine constructs a "front end," which is a partial filter graph.</span></span> <span data-ttu-id="bcf53-131">Das folgende Diagramm veranschaulicht ein typisches Front-End:</span><span class="sxs-lookup"><span data-stu-id="bcf53-131">The following diagram illustrates a typical front end:</span></span>

![Diagramm-Front-End Filtern](images/rendeng1.png)

<span data-ttu-id="bcf53-133">Die Subsysteme enthalten verschiedene spezialisierte Filter, die von der Rendering-Engine automatisch assembliert werden.</span><span class="sxs-lookup"><span data-stu-id="bcf53-133">The subsystems contain various specialized filters, which the render engine assembles automatically.</span></span> <span data-ttu-id="bcf53-134">Das Front-End enthält eine Ausgabe-PIN für jede Gruppe in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="bcf53-134">The front end contains one output pin for each group in the timeline.</span></span> <span data-ttu-id="bcf53-135">Die Ausgabe Pins liefern unkomprimierte Daten, wenn Sie die einfache Renderingengine verwenden, oder komprimierte Daten, wenn Sie die Smart-Rendering-Engine verwenden.</span><span class="sxs-lookup"><span data-stu-id="bcf53-135">The output pins deliver uncompressed data if you use the basic render engine, or compressed data if you use the smart render engine.</span></span>

<span data-ttu-id="bcf53-136">Im zweiten Schritt werden die Ausgabe Pins mit renderingfiltern verbunden.</span><span class="sxs-lookup"><span data-stu-id="bcf53-136">In the second step, the output pins are connected to rendering filters.</span></span> <span data-ttu-id="bcf53-137">In der Vorschau sind Renderfilter Video-und audiorenderer.</span><span class="sxs-lookup"><span data-stu-id="bcf53-137">For preview, the rendering filters are video and audio renderers.</span></span> <span data-ttu-id="bcf53-138">Beim Schreiben von Dateien sind die renderingfilter Multiplexer-Filter (MUX) und dateiwriter-Filter.</span><span class="sxs-lookup"><span data-stu-id="bcf53-138">For file writing, the rendering filters are multiplexer (mux) filters and file-writer filters.</span></span>

![Vervollständigen des Filter Diagramms](images/rendeng2.png)

## <a name="related-topics"></a><span data-ttu-id="bcf53-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bcf53-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcf53-141">Anzeigen einer Vorschau eines Projekts</span><span class="sxs-lookup"><span data-stu-id="bcf53-141">Previewing a Project</span></span>](previewing-a-project.md)
</dt> <dt>

[<span data-ttu-id="bcf53-142">Schreiben eines Projekts in eine Datei</span><span class="sxs-lookup"><span data-stu-id="bcf53-142">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



