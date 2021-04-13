---
description: Informationen über die Sequencer-Quelle
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Informationen über die Sequencer-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526612"
---
# <a name="about-the-sequencer-source"></a><span data-ttu-id="44e06-103">Informationen über die Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="44e06-103">About the Sequencer Source</span></span>

<span data-ttu-id="44e06-104">Mithilfe der Sequencer-Quelle kann eine Anwendung eine Auflistung von [Medienquellen](media-sources.md) sequenziell wiedergeben, wobei nahtlose Übergänge zwischen den Quellen möglich sind.</span><span class="sxs-lookup"><span data-stu-id="44e06-104">The sequencer source enables an application to play a collection of [Media Sources](media-sources.md) sequentially, with seamless transitions between the sources.</span></span> <span data-ttu-id="44e06-105">Die Sequencer-Quelle kann für die folgenden Szenarien verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="44e06-105">The sequencer source can be used for the following scenarios:</span></span>

-   <span data-ttu-id="44e06-106">Erstellen Sie eine Wiedergabeliste, die nahtlos von einer Medienquelle zum nächsten wechselt.</span><span class="sxs-lookup"><span data-stu-id="44e06-106">Create a playlist that switches seamlessly from one media source to the next.</span></span>
-   <span data-ttu-id="44e06-107">Wiedergabe von Streams aus mehreren Quellen gleichzeitig; Beispielsweise können Sie die Audiodatei aus einer Datei mit dem Video aus einer anderen Datei abspielen.</span><span class="sxs-lookup"><span data-stu-id="44e06-107">Play streams from multiple sources simultaneously; for example, play the audio from one file with the video from another.</span></span>
-   <span data-ttu-id="44e06-108">Wechsel zwischen Streams in unterschiedlichen Medienquellen in aufeinander folgenden Wiedergabelisten Einträgen Beispielsweise kann eine Wiedergabeliste Einträge aufweisen, die dieselbe Videoquelle gemeinsam verwenden, während jeder Eintrag eine andere Audioquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="44e06-108">Switch between streams in different media sources in consecutive playlist entries; for example, a playlist can have entries that share the same video source while each entry contains a different audio source.</span></span>

<span data-ttu-id="44e06-109">Für jedes Element einer Wiedergabeliste erstellt die Anwendung eine separate Topologie.</span><span class="sxs-lookup"><span data-stu-id="44e06-109">For each element of a playlist, the application creates a separate topology.</span></span> <span data-ttu-id="44e06-110">Die Medienquellen in diesen Topologien werden als *native Quellen* bezeichnet, um Sie von der Sequencer-Quelle zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="44e06-110">The media sources in these topologies are referred to as *native sources*, to distinguish them from the sequencer source.</span></span> <span data-ttu-id="44e06-111">Während der Wiedergabe wird die gesamte Sequenz von Topologien als *Darstellung* bezeichnet, und jede Topologie innerhalb der Sequenz wird als *Segment* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="44e06-111">During playback, the entire sequence of topologies is called a *presentation*, and each topology within the sequence is called a *segment*.</span></span>

<span data-ttu-id="44e06-112">Die Wiedergabe wird von der [Medien Sitzung](media-session.md)gesteuert, die Transport Steuerelemente bereitstellt, z. b. Wiedergabe, anhalten und anhalten.</span><span class="sxs-lookup"><span data-stu-id="44e06-112">Playback is controlled by the [Media Session](media-session.md), which provides transport controls, such as play, pause, and stop.</span></span> <span data-ttu-id="44e06-113">Die Medien Sitzung verwaltet auch die Präsentationszeit und sendet Ereignisse an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44e06-113">The Media Session also manages the presentation time and sends events to the application.</span></span> <span data-ttu-id="44e06-114">(Ereignisse aus der Sequencer-Quelle werden über die Medien Sitzung an die Anwendung weitergeleitet.)</span><span class="sxs-lookup"><span data-stu-id="44e06-114">(Events from the sequencer source are forwarded to the application through the Media Session.)</span></span>

<span data-ttu-id="44e06-115">Um eine Wiedergabeliste zu erstellen, erstellt die Anwendung eine oder mehrere Wiedergabe Topologien und fügt Sie in der gewünschten Wiedergabe Reihenfolge an der Sequencer-Quelle in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="44e06-115">To create a playlist, the application creates one or more playback topologies and queues them on the sequencer source in the desired order of playback.</span></span> <span data-ttu-id="44e06-116">Intern ändert die Sequencer-Quelle die Topologien so, dass die Quellknoten anstelle der systemeigenen Quelle auf die Sequencer-Quelle zeigen.</span><span class="sxs-lookup"><span data-stu-id="44e06-116">Internally, the sequencer source modifies the topologies so that the source nodes point to the sequencer source instead of the native source.</span></span> <span data-ttu-id="44e06-117">Die Anwendung sendet diese geänderten Topologien anstelle der ursprünglichen Topologien an die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="44e06-117">The application sends these modified topologies, rather than the original topologies, to the Media Session.</span></span> <span data-ttu-id="44e06-118">Dadurch kann die Sequencer-Quelle die systemeigenen Quellen aggregieren und mit der Medien Sitzung kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="44e06-118">This enables the sequencer source to aggregate the native sources and to communicate with the Media Session.</span></span>

<span data-ttu-id="44e06-119">Um nahtlose Übergänge zwischen Segmenten zu erreichen, werden die einzelnen Segmente durch die Sequencer-Quelle vorab überschritten.</span><span class="sxs-lookup"><span data-stu-id="44e06-119">To achieve seamless transitions between segments, the sequencer source prerolls each segment.</span></span> <span data-ttu-id="44e06-120">Während ein Segment abgespielt wird und bevor es an der Zeit ist, das folgende Segment wiederzugeben, löst die Sequencer-Quelle ein [menewpresentation](menewpresentation.md) -Ereignis aus, das einen Präsentations Deskriptor enthält.</span><span class="sxs-lookup"><span data-stu-id="44e06-120">While one segment is playing, and before it is time to play the following segment, the sequencer source fires an [MENewPresentation](menewpresentation.md) event that contains a presentation descriptor.</span></span> <span data-ttu-id="44e06-121">Die Anwendung verwendet diesen Präsentations Deskriptor, um die Topologie für das nächste Segment in der Präsentation zu erhalten, und fügt die Topologie in die Medien Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="44e06-121">The application uses this presentation descriptor to get the topology for the next segment in the presentation, and queues the topology on the Media Session.</span></span>

<span data-ttu-id="44e06-122">Die folgende Abbildung zeigt den Datenfluss für Wiedergabelisten Einträge über die Sequencer-Quelle.</span><span class="sxs-lookup"><span data-stu-id="44e06-122">The following illustration shows the data flow for playlist entries through the sequencer source.</span></span> <span data-ttu-id="44e06-123">Die Anwendung verwendet den quellresolver zum Erstellen der systemeigenen Quellen, erstellt Topologien für die einzelnen Segmente und fügt die Topologien in der Sequencer-Quelle in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="44e06-123">The application uses the source resolver to create the native sources, builds topologies for each segment, and queues the topologies on the sequencer source.</span></span>

![Diagramm, das den Datenfluss von imfmediasession-, imfsequencersource-und Wiedergabelisten Segmenten anzeigt, die zu imfmediasource führen](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a><span data-ttu-id="44e06-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44e06-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44e06-126">Erstellen einer Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="44e06-126">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="44e06-127">Topologien</span><span class="sxs-lookup"><span data-stu-id="44e06-127">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="44e06-128">Verwenden der Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="44e06-128">Using the Sequencer Source</span></span>](using-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="44e06-129">Sequencer-Quelle</span><span class="sxs-lookup"><span data-stu-id="44e06-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



