---
description: Aufbauen einer Wiedergabe Topologie mit topoedit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Aufbauen einer Wiedergabe Topologie mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106354888"
---
# <a name="building-a-playback-topology-with-topoedit"></a><span data-ttu-id="41f69-103">Aufbauen einer Wiedergabe Topologie mit topoedit</span><span class="sxs-lookup"><span data-stu-id="41f69-103">Building a Playback Topology with TopoEdit</span></span>

<span data-ttu-id="41f69-104">Topoedit kann eine Wiedergabe Topologie für eine lokale Mediendatei erstellen, indem die Quell-, Transformations-und Ausgabe Knoten automatisch hinzugefügt und verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="41f69-104">TopoEdit can build a playback topology for a local media file by automatically adding and connecting the source, transform, and output nodes.</span></span> <span data-ttu-id="41f69-105">Die Topologie wird von topoedit nicht automatisch aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="41f69-105">TopoEdit does not automatically resolve the topology.</span></span> <span data-ttu-id="41f69-106">Um die Topologie wiederzugeben, beheben Sie Sie, und verwenden Sie dann die Transport Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="41f69-106">To play the topology, resolve it and then use the transport controls.</span></span>

## <a name="to-build-and-play-a-topology-for-a-media-file"></a><span data-ttu-id="41f69-107">So erstellen und wiedergeben Sie eine Topologie für eine Mediendatei</span><span class="sxs-lookup"><span data-stu-id="41f69-107">To build and play a topology for a media file</span></span>

1.  <span data-ttu-id="41f69-108">Klicken Sie im Menü **Datei** auf **Datei Rendering**.</span><span class="sxs-lookup"><span data-stu-id="41f69-108">On the **File** menu, click **Render File**.</span></span>

    <span data-ttu-id="41f69-109">Dadurch wird das Dialogfeld **Medienquelle auswählen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="41f69-109">This opens the **Select Media Source** dialog box.</span></span>

2.  <span data-ttu-id="41f69-110">Navigieren Sie zu dem Ordner, in dem sich die Mediendatei befindet.</span><span class="sxs-lookup"><span data-stu-id="41f69-110">Navigate to the folder where the media file is located.</span></span>
3.  <span data-ttu-id="41f69-111">Geben Sie im Feld **Dateiname:** den Namen der Datei ein.</span><span class="sxs-lookup"><span data-stu-id="41f69-111">In the **File name:** field, enter the name of the file.</span></span>
4.  <span data-ttu-id="41f69-112">Klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="41f69-112">Click **Open**.</span></span>

    <span data-ttu-id="41f69-113">Der Bereich " **Topologie** " zeigt die verbundene Topologie.</span><span class="sxs-lookup"><span data-stu-id="41f69-113">The **Topology Pane** shows the connected topology.</span></span> <span data-ttu-id="41f69-114">Intern führt topoedit die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="41f69-114">Internally, TopoEdit performs the following tasks:</span></span>

    -   <span data-ttu-id="41f69-115">Listet die Streams in der Mediendatei auf und erstellt die Quellknoten.</span><span class="sxs-lookup"><span data-stu-id="41f69-115">Enumerates the streams in the media file and creates the source nodes.</span></span>
    -   <span data-ttu-id="41f69-116">Fügt in Abhängigkeit vom Medientyp der Quellknoten Transformations Knoten hinzu, z. b. Decoders.</span><span class="sxs-lookup"><span data-stu-id="41f69-116">Depending on the media type of the source nodes, adds transform nodes, such as decoders.</span></span>
    -   <span data-ttu-id="41f69-117">Fügt die Senke des streamingaudiorenderers (SAR) für den Audiostream und die EVR-Senke (Enhanced Video Renderer) für den Videostream hinzu.</span><span class="sxs-lookup"><span data-stu-id="41f69-117">Adds the Streaming Audio Renderer (SAR) sink for audio stream and the enhanced video renderer (EVR) sink for the video stream.</span></span>
    -   <span data-ttu-id="41f69-118">Verbindet die Knoten Eingaben und die Knoten Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="41f69-118">Connects the node inputs and the node outputs.</span></span>

5.  <span data-ttu-id="41f69-119">Klicken Sie im Menü **Topologie** auf **Topologie auflösen**.</span><span class="sxs-lookup"><span data-stu-id="41f69-119">On the **Topology** menu, click **Resolve Topology**.</span></span>
6.  <span data-ttu-id="41f69-120">Klicken Sie auf der Symbolleiste auf die Schaltfläche wieder **Gabe** , um die Topologie wiederzugeben</span><span class="sxs-lookup"><span data-stu-id="41f69-120">Click the **Play** button on the toolbar to play the topology.</span></span> Die folgende Abbildung zeigt die **Wiedergabe** Schaltfläche :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a><span data-ttu-id="41f69-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41f69-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f69-123">Wiedergabe Steuerelemente in topoedit</span><span class="sxs-lookup"><span data-stu-id="41f69-123">Playback Controls in TopoEdit</span></span>](playback-controls-in-topoedit.md)
</dt> <dt>

[<span data-ttu-id="41f69-124">Auflösen einer Topologie mit topoedit</span><span class="sxs-lookup"><span data-stu-id="41f69-124">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[<span data-ttu-id="41f69-125">Topoedit</span><span class="sxs-lookup"><span data-stu-id="41f69-125">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



