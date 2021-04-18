---
description: Das Zeitachsen Modell
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Das Zeitachsen Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560360"
---
# <a name="the-timeline-model"></a><span data-ttu-id="f9d1d-103">Das Zeitachsen Modell</span><span class="sxs-lookup"><span data-stu-id="f9d1d-103">The Timeline Model</span></span>

<span data-ttu-id="f9d1d-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="f9d1d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f9d1d-105">Eine *Zeitachse* ist ein Objekt, das von [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) verwendet wird, um ein Video Bearbeitungs Projekt darzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-105">A *timeline* is an object that [DirectShow Editing Services](directshow-editing-services.md) (DES) uses to represent a video editing project.</span></span> <span data-ttu-id="f9d1d-106">Ein Bearbeitungs Projekt wird als Auflistung von Quell Clips gestartet, die aus Videodateien, Audiodateien oder noch Bilddateien entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-106">An editing project starts as a collection of source clips, taken from video files, sound files, or still image files.</span></span> <span data-ttu-id="f9d1d-107">Eine lineare Sequenz von Clips bildet eine *Spur*. In DirectShow-Bearbeitungs Diensten werden Audiodateien und Videos in separaten Spuren abgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-107">A linear sequence of clips forms a *track*. In DirectShow Editing Services (DES), audio and video are placed in separate tracks.</span></span>

<span data-ttu-id="f9d1d-108">Spuren können auch geschichtet werden.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-108">Tracks can also be layered.</span></span> <span data-ttu-id="f9d1d-109">Mehrere Audiospuren werden miteinander gemischt und können Audioeffekte enthalten, wie z. b. "Fades" oder "Reverb".</span><span class="sxs-lookup"><span data-stu-id="f9d1d-109">Multiple audio tracks are mixed together, and might include audio effects, such as fades or reverb.</span></span> <span data-ttu-id="f9d1d-110">Zum Erstellen von Übergängen werden mehrere Videospuren verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-110">Multiple video tracks are used to create transitions.</span></span> <span data-ttu-id="f9d1d-111">Beispielsweise können Sie eine Löschung von einem Clip zu einem anderen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-111">For example, you can create a wipe from one clip to another.</span></span> <span data-ttu-id="f9d1d-112">Ein weiteres Beispiel ist ein Chroma-Schlüssel, in dem der Hintergrund eines Clips abgeblendet und durch eine andere Spur ersetzt wird. (Das Wettervorhersage vor einem Satelite-Image ist ein Beispiel für die Chroma-Schlüssel Erstellung.)</span><span class="sxs-lookup"><span data-stu-id="f9d1d-112">Another example is a chroma key, in which the background of one clip is keyed out and replaced by a different track. (The weather forecaster in front of a satelite image is an example of chroma keying.)</span></span>

<span data-ttu-id="f9d1d-113">DES verwendet eine Baumstruktur zur Darstellung einer Bearbeitung:</span><span class="sxs-lookup"><span data-stu-id="f9d1d-113">DES uses a tree structure to represent an editing:</span></span>

-   <span data-ttu-id="f9d1d-114">Audiodateien und Videoclips bilden die Blattknoten oder *Quell* Objekte.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-114">Audio and video clips form the leaf nodes, or *source* objects.</span></span>
-   <span data-ttu-id="f9d1d-115">Eine Auflistung von Quellen mit einem einheitlichen Medientyp (Audiodatei oder Video) ist eine *Spur*.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-115">A collection of sources with a uniform media type (audio or video) is a *track*.</span></span>
-   <span data-ttu-id="f9d1d-116">Eine Auflistung von Spuren ist eine *Komposition*.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-116">A collection of tracks is a *composition*.</span></span> <span data-ttu-id="f9d1d-117">Eine Komposition wird als zusammengesetzte aller darin enthaltenen Spuren gerendert.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-117">A composition is rendered as the composite of all the tracks it contains.</span></span> <span data-ttu-id="f9d1d-118">Kompositionen können andere Kompositionen enthalten, die komplexe Anordnungen von Spuren ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-118">Compositions can contain other compositions, which allows for complex arrangements of tracks.</span></span>
-   <span data-ttu-id="f9d1d-119">Eine Auflistung von Kompositionen und Nachverfolgen der obersten Ebene (alle, die denselben Medientyp darstellen) ist eine *Gruppe*.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-119">A top-level collection of compositions and tracks (all representing the same media type) is a *group*.</span></span>
-   <span data-ttu-id="f9d1d-120">Ein Satz von einer oder mehreren Gruppen bildet eine *Zeitachse*.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-120">A set of one or more groups forms a *timeline*.</span></span> <span data-ttu-id="f9d1d-121">Die Zeitachse ist der Stamm Knoten in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-121">The timeline is the root node in the tree.</span></span>

<span data-ttu-id="f9d1d-122">Eine Zeitachse muss mindestens eine Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-122">A timeline must contain at least one group.</span></span> <span data-ttu-id="f9d1d-123">Jede Gruppe stellt einen einzelnen Datenstrom in der endgültigen Produktion dar.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-123">Each group represents a single stream in the final production.</span></span> <span data-ttu-id="f9d1d-124">Ein typisches Projekt umfasst eine Videogruppe und eine Audiogruppe.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-124">A typical project includes one video group and one audio group.</span></span> <span data-ttu-id="f9d1d-125">Die Komposition ist optional. Sie sind vorhanden, um bei Bedarf mehr Struktur bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-125">Compositions are optional; they exist to provide more structure if needed.</span></span>

<span data-ttu-id="f9d1d-126">Die folgende Abbildung zeigt die Beziehungen zwischen untergeordneten und übergeordneten Elementen, die eine Zeitachse bilden:</span><span class="sxs-lookup"><span data-stu-id="f9d1d-126">The following illustration shows the child-parent relations that make up a timeline:</span></span>

![Knoten Struktur](images/timeline1.png)

<span data-ttu-id="f9d1d-128">Das folgende Beispiel zeigt eine Zeitachse als Temporale Sequenz:</span><span class="sxs-lookup"><span data-stu-id="f9d1d-128">The following shows a timeline as a temporal sequence:</span></span>

![Zeitachsen Abbildung](images/timeline2.png)

<span data-ttu-id="f9d1d-130">Der Pfeil oben stellt die Richtung der Zeitachse dar, beginnend ab der Zeit NULL.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-130">The arrow at the top represents the direction of the timeline, starting from time zero.</span></span> <span data-ttu-id="f9d1d-131">In der Videogruppe hat Track 1 eine höhere Priorität als Track 0.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-131">Within the video group, track 1 has a higher priority than track 0.</span></span> <span data-ttu-id="f9d1d-132">Die Quell Objekte in Track 1 verschleiern diese in der Nachverfolgung 0.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-132">The source objects in track 1 obscure those in track 0.</span></span> <span data-ttu-id="f9d1d-133">Wenn Track 1 leer ist, wird Nachverfolgung 0 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-133">Where track 1 is empty, track 0 "shows through."</span></span> <span data-ttu-id="f9d1d-134">Wie bereits erwähnt, werden Audiospuren einfach gemischt.</span><span class="sxs-lookup"><span data-stu-id="f9d1d-134">As mentioned earlier, audio tracks are simply mixed together.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9d1d-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9d1d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9d1d-136">Einführung in DirectShow-Bearbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="f9d1d-136">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="f9d1d-137">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="f9d1d-137">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



