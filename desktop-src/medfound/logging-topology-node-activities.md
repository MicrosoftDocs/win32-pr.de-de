---
description: Protokollieren von topologieknotenaktivitäten
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: Protokollieren von topologieknotenaktivitäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ca83d0513b97d053e27388bd0f2a418dfb253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041876"
---
# <a name="logging-topology-node-activities"></a><span data-ttu-id="78758-103">Protokollieren von topologieknotenaktivitäten</span><span class="sxs-lookup"><span data-stu-id="78758-103">Logging Topology Node Activities</span></span>

<span data-ttu-id="78758-104">Topoedit bietet die Option zum Erfassen von Protokollierungs Informationen für einen Transformations Knoten oder einen Ausgabe Knoten einer Topologie.</span><span class="sxs-lookup"><span data-stu-id="78758-104">TopoEdit provides the option for collecting logging information for a transform node or an output node of a topology.</span></span>

## <a name="to-setup-logging"></a><span data-ttu-id="78758-105">Einrichten der Protokollierung</span><span class="sxs-lookup"><span data-stu-id="78758-105">To setup logging</span></span>

1.  <span data-ttu-id="78758-106">Wählen Sie im Bereich **Topologie** einen Transformations Knoten oder einen Ausgabe Knoten aus, indem Sie darauf klicken.</span><span class="sxs-lookup"><span data-stu-id="78758-106">On the **Topology Pane**, select a transform node or an output node by clicking it.</span></span>

2.  <span data-ttu-id="78758-107">Klicken Sie **im Menü** Extras auf **ausgewählten Knoten Spy**.</span><span class="sxs-lookup"><span data-stu-id="78758-107">From the **Tools** menu, click **Spy Selected Node**.</span></span>

<span data-ttu-id="78758-108">Während der topologiebildung werden alle Methodenaufrufe für den ausgewählten Knoten in einer Textdatei protokolliert.</span><span class="sxs-lookup"><span data-stu-id="78758-108">During topology building, all method calls on the selected node are logged to a text file.</span></span> <span data-ttu-id="78758-109">Diese wird in dem Ordner gespeichert, in dem sich die Mediendatei befindet.</span><span class="sxs-lookup"><span data-stu-id="78758-109">This is saved in the folder where the media file is located.</span></span> <span data-ttu-id="78758-110">Die Protokolldatei wird mit dem Knoten Namen und dem eindeutigen Knoten Bezeichner für die Topologie gespeichert.</span><span class="sxs-lookup"><span data-stu-id="78758-110">The log file is saved with the node name and the unique topology node identifier.</span></span> <span data-ttu-id="78758-111">Dadurch wird sichergestellt, dass kein anderer Knoten in das Protokoll schreibt.</span><span class="sxs-lookup"><span data-stu-id="78758-111">This ensures that no other node writes to the log.</span></span> <span data-ttu-id="78758-112">Um den Bezeichner Programm gesteuert abzurufen, nennen Sie [**imftopologynode:: gettoponodeid**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="78758-112">To get the identifier programmatically, call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span>

<span data-ttu-id="78758-113">Im folgenden finden Sie einen Auszug aus einer Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="78758-113">The following is an excerpt from a log file.</span></span>

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a><span data-ttu-id="78758-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78758-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78758-115">Topoedit</span><span class="sxs-lookup"><span data-stu-id="78758-115">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



