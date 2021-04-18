---
description: Übertragung von DV von Datei auf Band
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Übertragung von DV von Datei auf Band
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352246"
---
# <a name="transmit-dv-from-file-to-tape"></a><span data-ttu-id="fda67-103">Übertragung von DV von Datei auf Band</span><span class="sxs-lookup"><span data-stu-id="fda67-103">Transmit DV from File to Tape</span></span>

<span data-ttu-id="fda67-104">Die Übertragung von der DV-AVI-Datei an das VTR-Band ist etwas komplizierter, da Dateien-1 oder Typ-2 eingeben können.</span><span class="sxs-lookup"><span data-stu-id="fda67-104">Transmit from DV AVI file to VTR tape is complicated somewhat by the fact that files can type-1 or type-2.</span></span> <span data-ttu-id="fda67-105">Gehen Sie folgendermaßen vor, um eine DV-Datei an das Band zu übertragen:</span><span class="sxs-lookup"><span data-stu-id="fda67-105">To transmit a DV file to tape, do the following:</span></span>

1.  <span data-ttu-id="fda67-106">Erstellen Sie eine Instanz des [msdv-Treiber](msdv-driver.md) Filters.</span><span class="sxs-lookup"><span data-stu-id="fda67-106">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="fda67-107">Weitere Informationen finden Sie unter [Auswählen eines Erfassungs Geräts](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="fda67-107">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="fda67-108">Stellen Sie sicher, dass sich das Gerät im VTR-Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="fda67-108">Make sure the device is in VTR mode.</span></span> <span data-ttu-id="fda67-109">Andernfalls können Sie nicht auf Band übertragen. Siehe [Geräte Modus](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="fda67-109">Otherwise, you cannot transmit to tape.See [Device Mode](device-mode.md).</span></span>
3.  <span data-ttu-id="fda67-110">Initialisieren Sie den Erfassungs Diagramm-Generator, wie unter [Informationen zum Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fda67-110">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
4.  <span data-ttu-id="fda67-111">Erstellen Sie das Diagramm.</span><span class="sxs-lookup"><span data-stu-id="fda67-111">Build the graph.</span></span> <span data-ttu-id="fda67-112">Die Diagramm Konfiguration hängt vom DV-Dateityp ab:</span><span class="sxs-lookup"><span data-stu-id="fda67-112">The graph configuration depends on the DV file type:</span></span>
    -   [<span data-ttu-id="fda67-113">Übertragen von Datei vom Typ "-1"</span><span class="sxs-lookup"><span data-stu-id="fda67-113">Transmit from Type-1 File</span></span>](transmit-from-type-1-file.md)
    -   [<span data-ttu-id="fda67-114">Übertragen von Typ-2-Datei</span><span class="sxs-lookup"><span data-stu-id="fda67-114">Transmit from Type-2 File</span></span>](transmit-from-type-2-file.md)
5.  <span data-ttu-id="fda67-115">Versetzen Sie das Gerät in den Modus zum Anhalten des Einsatzes, wie unter [Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fda67-115">Put the device into record-pause mode, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>
6.  <span data-ttu-id="fda67-116">Halten Sie das Filter Diagramm an.</span><span class="sxs-lookup"><span data-stu-id="fda67-116">Pause the filter graph.</span></span> <span data-ttu-id="fda67-117">Während das Filter Diagramm angehalten wird, sendet es einen kontinuierlichen Stream, der den ersten Frame des Videos wiederholt.</span><span class="sxs-lookup"><span data-stu-id="fda67-117">While the filter graph is paused, it sends a continuous stream that repeats the first frame of video.</span></span>
7.  <span data-ttu-id="fda67-118">Um mit der Übertragung zu beginnen, versetzen Sie das Gerät in den Aufzeichnungsmodus und führen dann das Filter Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="fda67-118">To start transmitting, put the device into record mode and then run the filter graph.</span></span> <span data-ttu-id="fda67-119">Das Gerät nimmt eine bestimmte Zeitspanne an, bis die Aufzeichnungs Kopfzeile aufzeichnen kann. warten Sie also ungefähr zwei Sekunden, bevor Sie das Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="fda67-119">It takes the device a certain amount of time until the recording head is able to record, so wait for about two seconds before running the graph.</span></span> <span data-ttu-id="fda67-120">Dies führt möglicherweise zu einigen doppelten Frames am Anfang des Bands, stellt jedoch sicher, dass keine Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="fda67-120">This might result in a few duplicated frames at the beginning of the tape, but it ensures that no data is lost.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fda67-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fda67-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fda67-122">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="fda67-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



