---
title: Gerätetypen
description: Gerätetypen
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712966"
---
# <a name="device-types"></a><span data-ttu-id="d258f-103">Gerätetypen</span><span class="sxs-lookup"><span data-stu-id="d258f-103">Device Types</span></span>

<span data-ttu-id="d258f-104">MCI erkennt einen grundlegenden Satz von *Gerätetypen*.</span><span class="sxs-lookup"><span data-stu-id="d258f-104">MCI recognizes a basic set of *device types*.</span></span> <span data-ttu-id="d258f-105">Bei einem Gerätetyp handelt es sich um einen Satz von MCI-Treibern, die einen gemeinsamen Befehlssatz verwenden und zur Steuerung von ähnlichen Multimedia-Geräten oder Datendateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d258f-105">A device type is a set of MCI drivers that share a common command set and are used to control similar multimedia devices or data files.</span></span> <span data-ttu-id="d258f-106">Viele MCI-Befehle, wie z. b. [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), erfordern, dass Sie einen Gerätetyp angeben.</span><span class="sxs-lookup"><span data-stu-id="d258f-106">Many MCI commands, such as [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)), require you to specify a device type.</span></span>

<span data-ttu-id="d258f-107">In der folgenden Tabelle sind die definierten Gerätetypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d258f-107">The following table lists the defined device types.</span></span> <span data-ttu-id="d258f-108">Die aktuelle Implementierung von MCI enthält Befehls Sätze für eine Teilmenge dieser Geräte.</span><span class="sxs-lookup"><span data-stu-id="d258f-108">The current implementation of MCI includes command sets for a subset of these devices.</span></span>



| <span data-ttu-id="d258f-109">Gerätetyp</span><span class="sxs-lookup"><span data-stu-id="d258f-109">Device type</span></span>      | <span data-ttu-id="d258f-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="d258f-110">Constant</span></span>                      | <span data-ttu-id="d258f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d258f-111">Description</span></span>                                      |
|------------------|-------------------------------|--------------------------------------------------|
| <span data-ttu-id="d258f-112">**CDAudio**</span><span class="sxs-lookup"><span data-stu-id="d258f-112">**cdaudio**</span></span>      | <span data-ttu-id="d258f-113">MCI \_ devtype \_ \_ -CD-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="d258f-113">MCI\_DEVTYPE\_CD\_AUDIO</span></span>       | <span data-ttu-id="d258f-114">CD-Audioplayer</span><span class="sxs-lookup"><span data-stu-id="d258f-114">CD audio player</span></span>                                  |
| <span data-ttu-id="d258f-115">**Hütte**</span><span class="sxs-lookup"><span data-stu-id="d258f-115">**dat**</span></span>          | <span data-ttu-id="d258f-116">MCI \_ devtype- \_ DAT</span><span class="sxs-lookup"><span data-stu-id="d258f-116">MCI\_DEVTYPE\_DAT</span></span>             | <span data-ttu-id="d258f-117">Digitaler audiobandplayer</span><span class="sxs-lookup"><span data-stu-id="d258f-117">Digital-audio tape player</span></span>                        |
| <span data-ttu-id="d258f-118">**Digitalvideo**</span><span class="sxs-lookup"><span data-stu-id="d258f-118">**digitalvideo**</span></span> | <span data-ttu-id="d258f-119">digitales MCI \_ devtype- \_ \_ Video</span><span class="sxs-lookup"><span data-stu-id="d258f-119">MCI\_DEVTYPE\_DIGITAL\_VIDEO</span></span>  | <span data-ttu-id="d258f-120">Digitales Video in einem Fenster (nicht GDI-basiert)</span><span class="sxs-lookup"><span data-stu-id="d258f-120">Digital video in a window (not GDI-based)</span></span>        |
| <span data-ttu-id="d258f-121">**außer**</span><span class="sxs-lookup"><span data-stu-id="d258f-121">**other**</span></span>        | <span data-ttu-id="d258f-122">MCI- \_ devtype \_ other</span><span class="sxs-lookup"><span data-stu-id="d258f-122">MCI\_DEVTYPE\_OTHER</span></span>           | <span data-ttu-id="d258f-123">Nicht definiertes MCI-Gerät</span><span class="sxs-lookup"><span data-stu-id="d258f-123">Undefined MCI device</span></span>                             |
| <span data-ttu-id="d258f-124">**Overlay**</span><span class="sxs-lookup"><span data-stu-id="d258f-124">**overlay**</span></span>      | <span data-ttu-id="d258f-125">MCI \_ devtype- \_ Overlay</span><span class="sxs-lookup"><span data-stu-id="d258f-125">MCI\_DEVTYPE\_OVERLAY</span></span>         | <span data-ttu-id="d258f-126">Overlay-Gerät (Analog Video in einem Fenster)</span><span class="sxs-lookup"><span data-stu-id="d258f-126">Overlay device (analog video in a window)</span></span>        |
| <span data-ttu-id="d258f-127">**scanner**</span><span class="sxs-lookup"><span data-stu-id="d258f-127">**scanner**</span></span>      | <span data-ttu-id="d258f-128">MCI \_ devtype- \_ Scanner</span><span class="sxs-lookup"><span data-stu-id="d258f-128">MCI\_DEVTYPE\_SCANNER</span></span>         | <span data-ttu-id="d258f-129">Bildscanner</span><span class="sxs-lookup"><span data-stu-id="d258f-129">Image scanner</span></span>                                    |
| <span data-ttu-id="d258f-130">**sequencer**</span><span class="sxs-lookup"><span data-stu-id="d258f-130">**sequencer**</span></span>    | <span data-ttu-id="d258f-131">MCI \_ devtype \_ Sequencer</span><span class="sxs-lookup"><span data-stu-id="d258f-131">MCI\_DEVTYPE\_SEQUENCER</span></span>       | <span data-ttu-id="d258f-132">MIDI-Sequencer</span><span class="sxs-lookup"><span data-stu-id="d258f-132">MIDI sequencer</span></span>                                   |
| <span data-ttu-id="d258f-133">**VCR**</span><span class="sxs-lookup"><span data-stu-id="d258f-133">**vcr**</span></span>          | <span data-ttu-id="d258f-134">MCI \_ devtype \_ VCR</span><span class="sxs-lookup"><span data-stu-id="d258f-134">MCI\_DEVTYPE\_VCR</span></span>             | <span data-ttu-id="d258f-135">Video-Kassettenrecorder oder Player</span><span class="sxs-lookup"><span data-stu-id="d258f-135">Video-cassette recorder or player</span></span>                |
| <span data-ttu-id="d258f-136">**Videodisk**</span><span class="sxs-lookup"><span data-stu-id="d258f-136">**videodisc**</span></span>    | <span data-ttu-id="d258f-137">MCI \_ devtype- \_ Videodisk</span><span class="sxs-lookup"><span data-stu-id="d258f-137">MCI\_DEVTYPE\_VIDEODISC</span></span>       | <span data-ttu-id="d258f-138">Videodisk-Player</span><span class="sxs-lookup"><span data-stu-id="d258f-138">Videodisc player</span></span>                                 |
| <span data-ttu-id="d258f-139">**waveaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="d258f-139">**waveaudio**</span></span>    | <span data-ttu-id="d258f-140">MCI \_ devtype \_ Waveform \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="d258f-140">MCI\_DEVTYPE\_WAVEFORM\_AUDIO</span></span> | <span data-ttu-id="d258f-141">Audiogerät, das digitalisierte Wellenform-Dateien wieder gibt</span><span class="sxs-lookup"><span data-stu-id="d258f-141">Audio device that plays digitized waveform files</span></span> |



 

<span data-ttu-id="d258f-142">In diesem Dokument sind die Namen der Gerätetypen fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="d258f-142">In this document, the names of device types are bold.</span></span> <span data-ttu-id="d258f-143">Gerätetyp Namen werden mit der Befehls Zeichenfolgen-Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="d258f-143">Device-type names are used with the command-string interface.</span></span> <span data-ttu-id="d258f-144">Gerätetyp Konstanten werden mit der befehlsnachrichten Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="d258f-144">Device-type constants are used with the command-message interface.</span></span>

 

 




