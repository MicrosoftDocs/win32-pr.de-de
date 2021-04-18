---
description: Verwalten von Video Bearbeitungs Projekten
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Verwalten von Video Bearbeitungs Projekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344912"
---
# <a name="managing-video-editing-projects"></a><span data-ttu-id="c1de8-103">Verwalten von Video Bearbeitungs Projekten</span><span class="sxs-lookup"><span data-stu-id="c1de8-103">Managing Video Editing Projects</span></span>

<span data-ttu-id="c1de8-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="c1de8-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c1de8-105">Die folgenden Tipps helfen Ihnen beim Verwalten von Projekten in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="c1de8-105">The following tips will help you to manage projects in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="c1de8-106">Änderungen an der Zeitachse</span><span class="sxs-lookup"><span data-stu-id="c1de8-106">Changes to the Timeline</span></span>

-   <span data-ttu-id="c1de8-107">Wenn Sie die Zeitachse nach dem Erstellen des Filter Diagramms ändern, müssen Sie " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md) " erneut ausführen, um das Front-End wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c1de8-107">If you change the timeline after you build the filter graph, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) again to rebuild the front end.</span></span> <span data-ttu-id="c1de8-108">Normalerweise wirkt sich dies nicht auf den Rest des Diagramms aus.</span><span class="sxs-lookup"><span data-stu-id="c1de8-108">Usually, this does not affect the rest of the graph.</span></span> <span data-ttu-id="c1de8-109">Gelegentlich muss die Renderingengine jedoch das gesamte Diagramm löschen, bevor es das Front-End neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1de8-109">Occasionally, however, the render engine needs to delete the entire graph before it rebuilds the front end.</span></span> <span data-ttu-id="c1de8-110">(Dies ist z. b. der Fall, wenn Sie eine Gruppe hinzufügen oder entfernen.) Die **connectfrontend** -Methode gibt "S \_ Warn \_ outputreset" zurück, um zu signalisieren, dass Sie das Diagramm gelöscht hat.</span><span class="sxs-lookup"><span data-stu-id="c1de8-110">(For example, this happens if you add or remove a group.) The **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET to signal that it deleted the graph.</span></span> <span data-ttu-id="c1de8-111">Wenn dies der Fall ist, muss die Anwendung den Renderingabschnitt des Diagramms neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1de8-111">If this happens, your application must rebuild the rendering section of the graph.</span></span>
-   <span data-ttu-id="c1de8-112">Um alle Objekte vollständig aus der Zeitachse zu entfernen, müssen Sie die [**iamtimeline:: clearallgroups**](iamtimeline-clearallgroups.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c1de8-112">To remove all objects completely from the timeline, call the [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) method.</span></span>

<span data-ttu-id="c1de8-113">**Bereinigung**</span><span class="sxs-lookup"><span data-stu-id="c1de8-113">**Cleanup**</span></span>

-   <span data-ttu-id="c1de8-114">Wenn Sie mit der Verwendung einer Rendering-Engine fertig sind, müssen Sie die Methode " [**irienderengine:: scrapit**](irenderengine-scrapit.md) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c1de8-114">When you are finished using a render engine, call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="c1de8-115">Stellen Sie wie bei jedem COM-Objekt sicher, dass Sie jeden Schnittstellen Zeiger freigeben, wenn Sie ihn nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1de8-115">As with any COM object, be sure to release every interface pointer when you are finished using it.</span></span>
-   <span data-ttu-id="c1de8-116">Die Renderingengine behält keinen Verweis Zähler auf der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="c1de8-116">The render engine does not keep a reference count on the timeline.</span></span> <span data-ttu-id="c1de8-117">Veröffentlichen Sie die Zeitachse nicht, bevor Sie Sie verwenden, und fordern Sie zuerst in der Renderingengine zuerst " **scrapit** " an.</span><span class="sxs-lookup"><span data-stu-id="c1de8-117">Do not release the timeline before you are done using it, and always call **ScrapIt** on the render engine first.</span></span>
-   <span data-ttu-id="c1de8-118">Wenn Sie alle Verweise auf eine Zeitachse freigeben, sollten Sie keines der Objekte in dieser Zeitachse verwenden, auch wenn Sie Verweis Zähler für Sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1de8-118">If you release all references to a timeline, do not use any of the objects in that timeline, even if you are holding reference counts on them.</span></span>

<span data-ttu-id="c1de8-119">**Mehrere Zeitachsen Instanzen**</span><span class="sxs-lookup"><span data-stu-id="c1de8-119">**Multiple Timeline Instances**</span></span>

-   <span data-ttu-id="c1de8-120">Verschieben Sie keine Zeitachsen Objekte Zwischenzeit Achsen.</span><span class="sxs-lookup"><span data-stu-id="c1de8-120">Do not move timeline objects between timelines.</span></span> <span data-ttu-id="c1de8-121">Jedes Objekt in einer Zeitachse muss von dieser Zeitachse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c1de8-121">Every object in a timeline must be created by that timeline.</span></span> <span data-ttu-id="c1de8-122">Die Zeitachse enthält einen internen Cache mit Informationen zu den Objekten, die Sie erstellt. das Verschieben von Zeitachsen Objekten kann den Cache stören.</span><span class="sxs-lookup"><span data-stu-id="c1de8-122">The timeline holds an internal cache with information about the objects that it creates; moving timeline objects can disrupt the cache.</span></span>
-   <span data-ttu-id="c1de8-123">Verwenden Sie niemals dieselbe Instanz eines rendermoduls mit mehr als einer Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="c1de8-123">Never use the same instance of a render engine with more than one timeline.</span></span> <span data-ttu-id="c1de8-124">Die Renderingengine enthält einen Cache mit Informationen über die Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="c1de8-124">The render engine holds a cache with information about the timeline.</span></span> <span data-ttu-id="c1de8-125">Mehrere Zeitachsen stören den Cache und verursachen unvorhersehbare Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="c1de8-125">Multiple timelines will disrupt the cache and cause unpredictable results.</span></span> <span data-ttu-id="c1de8-126">Wenn Sie zwei aktive Zeitachsen benötigen, erstellen Sie separate Instanzen von renderengines für jede Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="c1de8-126">If you need two active timelines, make separate instances of render engines for each timeline.</span></span>
-   <span data-ttu-id="c1de8-127">Eine Zeitachse kann mehr als eine Renderingengine verwenden, aber nicht gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="c1de8-127">A timeline can use more than one render engine, but not at the same time.</span></span> <span data-ttu-id="c1de8-128">Löschen Sie die alte Rendering-Engine, bevor Sie eine andere Renderengine verwenden</span><span class="sxs-lookup"><span data-stu-id="c1de8-128">Delete the old render engine before using another render engine.</span></span> <span data-ttu-id="c1de8-129">(Dies würden Sie in der Regel tun, wenn Sie von der Verwendung der grundlegenden Renderingengine für die Vorschauversion zum intelligenten Renderingmodul zum Schreiben von Dateien wechseln</span><span class="sxs-lookup"><span data-stu-id="c1de8-129">(You would typically do this when you switch from using the basic render engine for preview to the smart render engine for file writing.)</span></span>

<span data-ttu-id="c1de8-130">**Persistenz**</span><span class="sxs-lookup"><span data-stu-id="c1de8-130">**Persistence**</span></span>

-   <span data-ttu-id="c1de8-131">Das Filter Diagramm ist nicht persistent, wenn Sie das Projekt in einer XML-Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="c1de8-131">The filter graph is not persistent when you save the project to an XML file.</span></span> <span data-ttu-id="c1de8-132">Daher verlieren Sie alle Informationen im Zusammenhang mit der intelligenten Neukomprimierung, dem Komprimierungs Format oder den Komprimierungs Parametern.</span><span class="sxs-lookup"><span data-stu-id="c1de8-132">Therefore, you lose any information relating to smart recompression, compression format, or compression parameters.</span></span> <span data-ttu-id="c1de8-133">Die Anwendung kann diese Parameter nach dem Laden eines Projekts wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="c1de8-133">It is up to the application to restore these parameters after it loads a project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1de8-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1de8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1de8-135">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="c1de8-135">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



