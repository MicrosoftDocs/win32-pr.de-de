---
description: Architektur der DirectShow-Bearbeitungs Dienste
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Architektur der DirectShow-Bearbeitungs Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345981"
---
# <a name="directshow-editing-services-architecture"></a><span data-ttu-id="0de98-103">Architektur der DirectShow-Bearbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="0de98-103">DirectShow Editing Services Architecture</span></span>

<span data-ttu-id="0de98-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="0de98-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0de98-105">In der folgenden Abbildung ist die Architektur von [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (de) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0de98-105">The following illustration shows the architecture of [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

![Architektur der DirectShow-Bearbeitungs Dienste](images/architecture.png)

-   <span data-ttu-id="0de98-107">Timeline: stellt eine Videoproduktion als eine Auflistung von Quell Clips,-Übergängen und-Effekten dar, die in einer Reihe von untergeordneten Titeln angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0de98-107">Timeline: Represents a video production as a collection of source clips, transitions, and effects, organized into a set of nested tracks.</span></span> <span data-ttu-id="0de98-108">Weitere Informationen finden Sie [im Zeitachsen Modell](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="0de98-108">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>
-   <span data-ttu-id="0de98-109">XML-Parser: analysiert die Zeitachse und generiert eine Ausgabedatei, oder liest eine Eingabedatei und generiert eine Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="0de98-109">XML Parser: Parses the timeline and generates an output file, or reads an input file and generates a timeline.</span></span> <span data-ttu-id="0de98-110">DES unterstützt ein XML-basiertes Persistenzformat.</span><span class="sxs-lookup"><span data-stu-id="0de98-110">DES supports an XML-based persistence format.</span></span>
-   <span data-ttu-id="0de98-111">Rendering-Engine: übersetzt die Zeitachse in ein Formular, das als Streamingmedien gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0de98-111">Render engine: Translates the timeline into a form that can be rendered as streaming media.</span></span> <span data-ttu-id="0de98-112">Standardmäßig erzeugt die Renderingengine ein DirectShow-Filter Diagramm (siehe nächster Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="0de98-112">By default, the render engine produces a DirectShow filter graph (see next section).</span></span>
-   <span data-ttu-id="0de98-113">Medienlocator: verwaltet einen Cache von Speicherorten von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="0de98-113">Media locator: Maintains a cache of locations of media elements.</span></span> <span data-ttu-id="0de98-114">Wenn der Versuch, ein Medien Element zu öffnen, fehlschlägt, verwendet des den Cache, um das-Element zu suchen, basierend auf einem erfolgreichen Öffnungs Verlauf.</span><span class="sxs-lookup"><span data-stu-id="0de98-114">When an attempt to open a media element fails, DES uses the cache to locate the element, based on a history of successful opens.</span></span>

<span data-ttu-id="0de98-115">Die Zeitachse ist eine abstrakte Beschreibung eines Video Bearbeitungs Projekts.</span><span class="sxs-lookup"><span data-stu-id="0de98-115">The timeline is an abstract description of a video editing project.</span></span> <span data-ttu-id="0de98-116">Sie gibt die im Projekt verwendeten Quell Ausschnitte, Start-und Endzeiten, Effekte und Übergänge usw. an.</span><span class="sxs-lookup"><span data-stu-id="0de98-116">It specifies the source clips used in the project, start and stop times, effects and transitions, and so forth.</span></span> <span data-ttu-id="0de98-117">Die Zeitachse stellt jedoch nicht die Video-und Audiostreams dar.</span><span class="sxs-lookup"><span data-stu-id="0de98-117">The timeline does not render the video and audio streams, however.</span></span> <span data-ttu-id="0de98-118">Stattdessen übersetzt die Renderengine die Zeitachse für die Vorschau oder die Dateiausgabe in ein Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="0de98-118">Instead, the render engine translates the timeline into a filter graph, for either preview or file output.</span></span> <span data-ttu-id="0de98-119">Eine Anwendung bearbeitet die Zeitachse, anstatt das Filter Diagramm direkt zu bearbeiten, was mühsam und fehleranfällig wäre.</span><span class="sxs-lookup"><span data-stu-id="0de98-119">An application manipulates the timeline rather than directly manipulating the filter graph, which would be cumbersome and error prone.</span></span>

<span data-ttu-id="0de98-120">In der folgenden Tabelle sind die Hauptaufgaben aufgeführt, die eine typische Video Bearbeitungs Anwendung ausführt, sowie die Schnittstellen, die die einzelnen Aufgaben unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0de98-120">The following table lists the main tasks that a typical video editing application performs, along with the interfaces that support each task.</span></span> <span data-ttu-id="0de98-121">In späteren Abschnitten werden diese Aufgaben und die-Schnittstellen ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0de98-121">Later sections describe these tasks and the interfaces in more detail.</span></span>



| <span data-ttu-id="0de98-122">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0de98-122">Task</span></span>                                     | <span data-ttu-id="0de98-123">Schnittstelle (n)</span><span class="sxs-lookup"><span data-stu-id="0de98-123">Interface(s)</span></span>                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de98-124">Erstellen oder ändern Sie eine Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="0de98-124">Construct or modify a timeline.</span></span>          | <span data-ttu-id="0de98-125">[**Iamtimeline**](iamtimeline.md) und die anderen **iamtimelinexxxx** -Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0de98-125">[**IAMTimeline**](iamtimeline.md) and the other **IAMTimelineXXXX** interfaces</span></span>          |
| <span data-ttu-id="0de98-126">Speichern und Laden von Projektdateien.</span><span class="sxs-lookup"><span data-stu-id="0de98-126">Save and load project files.</span></span>             | [<span data-ttu-id="0de98-127">**IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="0de98-127">**IXml2Dex**</span></span>](ixml2dex.md)                                                             |
| <span data-ttu-id="0de98-128">Anzeigen einer Vorschau eines Projekts oder schreiben in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="0de98-128">Preview a project or write it to a file.</span></span> | <span data-ttu-id="0de98-129">" [**Unenderengine**](irenderengine.md)", " [ **ismartrenderengine** "](ismartrenderengine.md)</span><span class="sxs-lookup"><span data-stu-id="0de98-129">[**IRenderEngine**](irenderengine.md), [**ISmartRenderEngine**](ismartrenderengine.md)</span></span> |



 

<span data-ttu-id="0de98-130">Außerdem kann eine Anwendung einige oder alle der folgenden sekundären Tasks ausführen.</span><span class="sxs-lookup"><span data-stu-id="0de98-130">In addition, an application might perform some or all of the following secondary tasks.</span></span>



| <span data-ttu-id="0de98-131">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0de98-131">Task</span></span>                                                                                           | <span data-ttu-id="0de98-132">Schnittstelle (n)</span><span class="sxs-lookup"><span data-stu-id="0de98-132">Interface(s)</span></span>                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0de98-133">Abrufen von Informationen zu Mediendateien</span><span class="sxs-lookup"><span data-stu-id="0de98-133">Obtain information about media files.</span></span> <span data-ttu-id="0de98-134">(Anzahl der Streams, Format und Dauer jedes Streams.)</span><span class="sxs-lookup"><span data-stu-id="0de98-134">(Number of streams; format and duration of each stream.)</span></span> | [<span data-ttu-id="0de98-135">**Imediadet**</span><span class="sxs-lookup"><span data-stu-id="0de98-135">**IMediaDet**</span></span>](imediadet.md)                                               |
| <span data-ttu-id="0de98-136">Legen Sie Eigenschaften für Übergänge und Effekte fest.</span><span class="sxs-lookup"><span data-stu-id="0de98-136">Set properties on transitions and effects.</span></span>                                                     | [<span data-ttu-id="0de98-137">**Ipropertysetter**</span><span class="sxs-lookup"><span data-stu-id="0de98-137">**IPropertySetter**</span></span>](ipropertysetter.md)                                   |
| <span data-ttu-id="0de98-138">Benachrichtigung erhalten, wenn während des Renderings Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="0de98-138">Receive notification when errors occur during rendering.</span></span>                                       | <span data-ttu-id="0de98-139">[**Iamseterrorlog**](iamseterrorlog.md), [ **iamerrorlog**](iamerrorlog.md)</span><span class="sxs-lookup"><span data-stu-id="0de98-139">[**IAMSetErrorLog**](iamseterrorlog.md), [**IAMErrorLog**](iamerrorlog.md)</span></span> |
| <span data-ttu-id="0de98-140">Abrufen von Poster-Frames.</span><span class="sxs-lookup"><span data-stu-id="0de98-140">Retrieve poster frames.</span></span>                                                                        | <span data-ttu-id="0de98-141">[**Imediadet**](imediadet.md), [ **isamplegrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="0de98-141">[**IMediaDet**](imediadet.md), [**ISampleGrabber**](isamplegrabber.md)</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="0de98-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0de98-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0de98-143">Einführung in DirectShow-Bearbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="0de98-143">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



