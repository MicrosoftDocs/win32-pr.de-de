---
description: Hinzufügen von Ausgabe Knoten mit topoedit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Hinzufügen von Ausgabe Knoten mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347751"
---
# <a name="adding-output-nodes-with-topoedit"></a><span data-ttu-id="63bb5-103">Hinzufügen von Ausgabe Knoten mit topoedit</span><span class="sxs-lookup"><span data-stu-id="63bb5-103">Adding Output Nodes with TopoEdit</span></span>

<span data-ttu-id="63bb5-104">In einer Topologie stellt ein Ausgabe Knoten eine Medien Senke dar, die Mediendaten von einem Transformations Knoten empfängt und für die Wiedergabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="63bb5-104">In a topology, an output node represents a media sink that receives media data from a transform node and presents it for playback.</span></span> <span data-ttu-id="63bb5-105">Der Typ des Ausgabe Knotens hängt vom Medientyp des Quell Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="63bb5-105">The type of output node depends on the media type of the source node.</span></span>

<span data-ttu-id="63bb5-106">Die folgende Tabelle zeigt den Menübefehl bzw. den Symbolleisten Befehl zum Hinzufügen eines Ausgabe Knotens zur Topologie.</span><span class="sxs-lookup"><span data-stu-id="63bb5-106">The following table shows the menu/toolbar command for adding an output node to the topology.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="63bb5-107">Quell Medientyp</span><span class="sxs-lookup"><span data-stu-id="63bb5-107">Source media type</span></span></th>
<th><span data-ttu-id="63bb5-108">Menü/Symbolleisten Befehl</span><span class="sxs-lookup"><span data-stu-id="63bb5-108">Menu/Toolbar Command</span></span></th>
<th><span data-ttu-id="63bb5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63bb5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63bb5-110">Audiodatenstrom</span><span class="sxs-lookup"><span data-stu-id="63bb5-110">Audio stream</span></span></td>
<td><span data-ttu-id="63bb5-111">Klicken Sie im Menü <strong>Topologie</strong> auf <strong>SAR hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="63bb5-111">On the <strong>Topology</strong> menu, click <strong>Add SAR</strong>.</span></span></td>
<td><span data-ttu-id="63bb5-112">Erstellt einen Ausgabe Knoten für den streamingaudiorenderer (SAR), der einen Audiostream über ein Audiogerät (z. b. eine Soundkarte) wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="63bb5-112">Creates an output node for the Streaming Audio Renderer (SAR) that plays an audio stream through an audio device such as a sound card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63bb5-113">Videostream</span><span class="sxs-lookup"><span data-stu-id="63bb5-113">Video stream</span></span></td>
<td><span data-ttu-id="63bb5-114">Klicken Sie im Menü <strong>Topologie</strong> auf <strong>EVR hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="63bb5-114">On the <strong>Topology</strong> menu, click <strong>Add EVR</strong>.</span></span></td>
<td><span data-ttu-id="63bb5-115">Erstellt einen Ausgabe Knoten für den erweiterten Videorenderer (EVR), der Frames für einen Videostream anzeigt.</span><span class="sxs-lookup"><span data-stu-id="63bb5-115">Creates an output node for the enhanced video renderer (EVR) that displays frames for a video stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63bb5-116">Benutzerdefinierte Medien Senke</span><span class="sxs-lookup"><span data-stu-id="63bb5-116">Custom media sink</span></span></td>
<td><ol>
<li><span data-ttu-id="63bb5-117">Klicken Sie im Menü <strong>Topologie</strong> auf <strong>benutzerdefinierte Senke hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="63bb5-117">On the <strong>Topology</strong> menu, click <strong>Add Custom Sink</strong>.</span></span><br/> <span data-ttu-id="63bb5-118">Das Dialogfeld <strong>benutzerdefinierte GUID eingeben</strong> wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="63bb5-118">The <strong>Input Custom GUID</strong> dialog box opens.</span></span><br/></li>
<li><p><span data-ttu-id="63bb5-119">Geben Sie im Feld <strong>GUID:</strong> die GUID der benutzerdefinierten Senke ein, die Sie der Topologie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="63bb5-119">In the <strong>GUID:</strong> field, enter the GUID of your custom sink that you want to add to the topology.</span></span><br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="63bb5-120">Topoedit erwartet die GUID im Format &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; .</span><span class="sxs-lookup"><span data-stu-id="63bb5-120">TopoEdit expects the GUID in the format &quot;{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}&quot;.</span></span> <span data-ttu-id="63bb5-121">Andernfalls kann der Knoten nicht hinzugefügt werden, und es wird eine &quot; ungültige GUID- &quot; Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="63bb5-121">Otherwise, it fails to add the node and displays an &quot;Invalid GUID&quot; error message.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="63bb5-122">Klicken Sie auf <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="63bb5-122">Click <strong>OK</strong>.</span></span><br/></li>
</ol></td>
<td><span data-ttu-id="63bb5-123">Erstellt einen Ausgabe Knoten für die streamsenke für eine benutzerdefinierte Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="63bb5-123">Creates an output node for the stream sink for a custom media source.</span></span><br/> <span data-ttu-id="63bb5-124">Die benutzerdefinierte Senke muss <strong>cokreateinstance</strong> unterstützen, damit die Senke mit einer CLSID angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="63bb5-124">The custom sink must support <strong>CoCreateInstance</strong> so that the sink can be specified with a CLSID.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="63bb5-125">Topoedit erstellt den angegebenen Ausgabe Knoten.</span><span class="sxs-lookup"><span data-stu-id="63bb5-125">TopoEdit creates the specified output node.</span></span> <span data-ttu-id="63bb5-126">Im Bereich **Topologie** wird der Ausgabe Knoten als grünes Feld angezeigt, in dem der Name der Datenstrom Senke angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="63bb5-126">The **Topology Pane** shows the output node as a green box that shows the name of the stream sink.</span></span>

<span data-ttu-id="63bb5-127">Informationen zum programmgesteuerten Hinzufügen von Ausgabe Knoten mithilfe Media Foundation APIs finden Sie unter [Erstellen von Ausgabe Knoten](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="63bb5-127">For information about adding output nodes programmatically by using Media Foundation APIs, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="63bb5-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63bb5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63bb5-129">Entwickeln von Topologien mithilfe von topoedit</span><span class="sxs-lookup"><span data-stu-id="63bb5-129">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="63bb5-130">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="63bb5-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> <dt>

[<span data-ttu-id="63bb5-131">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="63bb5-131">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="63bb5-132">Topoedit</span><span class="sxs-lookup"><span data-stu-id="63bb5-132">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




