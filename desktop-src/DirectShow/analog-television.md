---
description: Analog Fernsehen
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Analog Fernsehen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124250"
---
# <a name="analog-television"></a><span data-ttu-id="b913b-103">Analog Fernsehen</span><span class="sxs-lookup"><span data-stu-id="b913b-103">Analog Television</span></span>

<span data-ttu-id="b913b-104">Das analoge Fernsehen unterscheidet sich auf verschiedene Arten von anderen Video Erfassungs Szenarien:</span><span class="sxs-lookup"><span data-stu-id="b913b-104">Analog television differs from other video capture scenarios in several ways:</span></span>

-   <span data-ttu-id="b913b-105">Die Tuner-Karte wird auf ein analoges Signal optimiert, das dann digitalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b913b-105">The tuner card tunes to an analog signal, which is then digitized.</span></span>
-   <span data-ttu-id="b913b-106">Audiodaten werden im analogen Signal übertragen.</span><span class="sxs-lookup"><span data-stu-id="b913b-106">Audio is carried in the analog signal.</span></span> <span data-ttu-id="b913b-107">Wie die Audiokarte die Audiokarte erreicht, hängt von der Hardware ab.</span><span class="sxs-lookup"><span data-stu-id="b913b-107">How the audio reaches the sound card varies depending on the hardware.</span></span>
-   <span data-ttu-id="b913b-108">Das Signal enthält möglicherweise zusätzliche Daten im vertikalen Auslassungs Intervall (VBI), wie z. b. gesperrte Untertitel (CC), World Standard Teletext (WST) und erweiterte Datendienste (XDS).</span><span class="sxs-lookup"><span data-stu-id="b913b-108">The signal may contain additional data in the vertical blanking interval (VBI), such as closed captions (CC), World Standard Teletext (WST), and extended data services (XDS).</span></span>

<span data-ttu-id="b913b-109">Das folgende Diagramm zeigt ein typisches Filter Diagramm für die Fernseh Vorschau.</span><span class="sxs-lookup"><span data-stu-id="b913b-109">The following diagram shows a typical filter graph for television preview.</span></span>

![Analog Fernseh Diagramm](images/vidcap06.png)

-   <span data-ttu-id="b913b-111">Der [TV-Tuner-](tv-tuner-filter.md) Filter steuert die Optimierung.</span><span class="sxs-lookup"><span data-stu-id="b913b-111">The [TV Tuner](tv-tuner-filter.md) filter controls tuning.</span></span>
-   <span data-ttu-id="b913b-112">Der [TV-Audiofilter](tv-audio-filter.md) steuert die Audiodecodierung.</span><span class="sxs-lookup"><span data-stu-id="b913b-112">The [TV Audio](tv-audio-filter.md) filter controls the audio decoding.</span></span>
-   <span data-ttu-id="b913b-113">Wenn die Tuner-Karte über mehr als eine physische Eingabe verfügt, kann die Anwendung mithilfe des [Querbalken Filters für analoge Video](analog-video-crossbar-filter.md) auswählen, welche Eingabe decodiert und gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b913b-113">If the tuner card has more than one physical input, the [Analog Video Crossbar](analog-video-crossbar-filter.md) filter enables the application to select which input is decoded and rendered.</span></span>
-   <span data-ttu-id="b913b-114">Der [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter liefert den digitalisierten Videostream.</span><span class="sxs-lookup"><span data-stu-id="b913b-114">The [WDM Video Capture](wdm-video-capture-filter.md) filter delivers the digitized video stream.</span></span>

<span data-ttu-id="b913b-115">Der Erfassungs Diagramm-Generator fügt automatisch alle erforderlichen Filter aus dem Erfassungs Filter ein.</span><span class="sxs-lookup"><span data-stu-id="b913b-115">The Capture Graph Builder automatically inserts any filters that are required upstream from the capture filter.</span></span>

<span data-ttu-id="b913b-116">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b913b-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="b913b-117">Optimierung des analogen Fernseh ERS</span><span class="sxs-lookup"><span data-stu-id="b913b-117">Analog Television Tuning</span></span>](analog-television-tuning.md)
-   [<span data-ttu-id="b913b-118">Analog zum Fernsehgerät</span><span class="sxs-lookup"><span data-stu-id="b913b-118">Analog Television Audio</span></span>](analog-television-audio.md)
-   [<span data-ttu-id="b913b-119">Untertitel und Teletext</span><span class="sxs-lookup"><span data-stu-id="b913b-119">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)

## <a name="related-topics"></a><span data-ttu-id="b913b-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b913b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b913b-121">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="b913b-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



