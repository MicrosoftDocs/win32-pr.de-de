---
description: MPEG-2-Unterstützung in DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: MPEG-2-Unterstützung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522195"
---
# <a name="mpeg-2-support-in-directshow"></a><span data-ttu-id="716bb-103">MPEG-2-Unterstützung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="716bb-103">MPEG-2 Support in DirectShow</span></span>

<span data-ttu-id="716bb-104">In diesem Abschnitt werden die Komponenten beschrieben, die Sie verwenden können, um MPEG-2-Inhalte in DirectShow wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="716bb-104">This section describes the components that you can use to play MPEG-2 content in DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="716bb-105">Obwohl DVD-Videos auf MPEG-2 basieren, wird in diesem Abschnitt weder die DVD-Wiedergabe noch die Navigation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="716bb-105">Although DVD video is based on MPEG-2, this section does not describe DVD playback or navigation.</span></span> <span data-ttu-id="716bb-106">Weitere Informationen zu DVD in DirectShow finden Sie unter [DVD-Anwendungen](dvd-applications.md).</span><span class="sxs-lookup"><span data-stu-id="716bb-106">For information about DVD in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="716bb-107">MPEG-2-Daten können aus einer lokalen Datei oder aus einer Live Quelle, z. b. einem Netzwerk Broadcast oder einem D-VHS-Gerät, stammen.</span><span class="sxs-lookup"><span data-stu-id="716bb-107">MPEG-2 data can come from a local file, or from a live source, such as a network broadcast or D-VHS device.</span></span> <span data-ttu-id="716bb-108">Die Dateiwiedergabe wird als *Pullmodus* bezeichnet, da der Parserfilter Daten aus der Datei in das Filter Diagramm zieht.</span><span class="sxs-lookup"><span data-stu-id="716bb-108">File playback is called *pull mode* because the parser filter pulls data from the file into the filter graph.</span></span> <span data-ttu-id="716bb-109">Live Quellen werden als *Pushmodus* bezeichnet, da der Quell Filterdaten per Push in das Diagramm überträgt.</span><span class="sxs-lookup"><span data-stu-id="716bb-109">Live sources are called *push mode* because the source filter pushes data into the graph.</span></span>

<span data-ttu-id="716bb-110">DirectShow stellt zwei Filter bereit, mit denen MPEG-2-Systemdaten Ströme analysiert werden können:</span><span class="sxs-lookup"><span data-stu-id="716bb-110">DirectShow provides two filters that can parse MPEG-2 system streams:</span></span>

-   <span data-ttu-id="716bb-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): dieser Filter unterstützt den Pushmodus für Programmstreams und Transportdaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="716bb-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): This filter supports push mode for program streams and transport streams.</span></span> <span data-ttu-id="716bb-112">In Windows XP und höher unterstützt es auch den Pullmodus für Programmstreams.</span><span class="sxs-lookup"><span data-stu-id="716bb-112">In Windows XP and later, it also supports pull mode for program streams.</span></span>
-   <span data-ttu-id="716bb-113">[MPEG-2-Splitter](mpeg-2-splitter.md): dieser Filter unterstützt den Pullmodus für Programmstreams auf downlevelplattformen.</span><span class="sxs-lookup"><span data-stu-id="716bb-113">[MPEG-2 Splitter](mpeg-2-splitter.md): This filter supports pull mode for program streams on downlevel platforms.</span></span> <span data-ttu-id="716bb-114">Dieser Filter ist in Windows XP und höher veraltet.</span><span class="sxs-lookup"><span data-stu-id="716bb-114">This filter is deprecated in Windows XP and later.</span></span>

<span data-ttu-id="716bb-115">Wenn Sie den "MPEG-2 demux"-oder "MPEG-2"-Splitter verwenden möchten, müssen Sie über DirectShow-kompatible MPEG-2-Audiodateien und-Video-Decoder verfügen, die die in "packetisiert"-</span><span class="sxs-lookup"><span data-stu-id="716bb-115">To use the MPEG-2 demux or MPEG-2 splitter, you must have DirectShow-compatible MPEG-2 audio and video decoders that accept packetized elementary streams (PES).</span></span>

<span data-ttu-id="716bb-116">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="716bb-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="716bb-117">Übersicht über MPEG-2-Systeme</span><span class="sxs-lookup"><span data-stu-id="716bb-117">Overview of MPEG-2 Systems</span></span>](overview-of-mpeg-2-systems.md)
-   [<span data-ttu-id="716bb-118">Verwenden von MPEG-2 Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="716bb-118">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
-   [<span data-ttu-id="716bb-119">Verwenden des MPEG-2-Splitters</span><span class="sxs-lookup"><span data-stu-id="716bb-119">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
-   [<span data-ttu-id="716bb-120">MPEG-Beispiel Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="716bb-120">MPEG Sample Properties</span></span>](mpeg-sample-properties.md)

## <a name="related-topics"></a><span data-ttu-id="716bb-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="716bb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="716bb-122">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="716bb-122">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 



