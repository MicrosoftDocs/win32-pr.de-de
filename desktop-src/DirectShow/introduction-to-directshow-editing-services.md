---
description: Einführung in DirectShow-Bearbeitungs Dienste
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Einführung in DirectShow-Bearbeitungs Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481614"
---
# <a name="introduction-to-directshow-editing-services"></a><span data-ttu-id="2b57d-103">Einführung in DirectShow-Bearbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="2b57d-103">Introduction to DirectShow Editing Services</span></span>

<span data-ttu-id="2b57d-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="2b57d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="2b57d-105">Der Kern von DirectShow ist eine leistungsstarke Architektur für die Verarbeitung von Streamingmedien.</span><span class="sxs-lookup"><span data-stu-id="2b57d-105">The core of DirectShow is a powerful architecture for handling streaming media.</span></span> <span data-ttu-id="2b57d-106">Eine Anwendung kann Sie zum Wiedergeben von multimediarewendungen verwenden, die in einer Vielzahl von Formaten erstellt wurden, ohne dass der Entwickler sich Gedanken über die Dateikomprimierung und andere mühsame Details machen muss.</span><span class="sxs-lookup"><span data-stu-id="2b57d-106">An application can use it to play multimedia content authored in a wide variety of formats, without the developer needing to worry about file compression and other tedious details.</span></span> <span data-ttu-id="2b57d-107">Vor [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) fehlte in DirectShow jedoch die für die nichtlineare Bearbeitung benötigte Flexibilität.</span><span class="sxs-lookup"><span data-stu-id="2b57d-107">Prior to [DirectShow Editing Services](directshow-editing-services.md) (DES), however, DirectShow lacked the flexibility needed for nonlinear editing.</span></span>

<span data-ttu-id="2b57d-108">Angenommen, Sie möchten z. b. eine Videosequenz erstellen, die aus 4 Sekunden aus Quelle a besteht, gefolgt von 10 Sekunden von Quelle B und mit 5 Sekunden aus Quelle C. Dies kann sehr einfach durch die zentrale DirectShow-API erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="2b57d-108">For example, suppose you wanted to create a video sequence consisting of 4 seconds from source A, followed by 10 seconds from source B, and ending with 5 seconds from source C. You could accomplish that much fairly easily using only the core DirectShow API.</span></span>

<span data-ttu-id="2b57d-109">Aber was ist, wenn Sie entschieden haben, dass Quelle C vor Quelle B und nicht nach die Sequenz sollte 8 Sekunden aus Quelle A, nicht 4, verwenden. und dass die gesamte Produktion eine separate Audiospur benötigt, die im Hintergrund gespielt wird?</span><span class="sxs-lookup"><span data-stu-id="2b57d-109">But what if you decided that source C should come before source B, not after; that the sequence should use 8 seconds from source A, not 4; and that the entire production needed a separate audio track playing in the background?</span></span> <span data-ttu-id="2b57d-110">Auch kleinere Änderungen wie diese können schwierig zu implementieren sein.</span><span class="sxs-lookup"><span data-stu-id="2b57d-110">Even minor changes such as these could be difficult to implement.</span></span> <span data-ttu-id="2b57d-111">Das soeben beschriebene Szenario ist jedoch ein triviales Bearbeitungs Projekt in des – Sie können es mit einigen Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2b57d-111">But the scenario just described is a trivial editing project in DES—you can do it with a handful of method calls.</span></span>

<span data-ttu-id="2b57d-112">Im folgenden finden Sie einige der Features, die von den DirectShow-Funktionen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="2b57d-112">Here are some of the features that DES brings to DirectShow:</span></span>

-   <span data-ttu-id="2b57d-113">Ein Zeitachsen Modell, das Video-und Audiospuren in den in der Liste eingefügten Schichten organisiert, sodass die endgültige Produktion leicht bearbeitet werden kann</span><span class="sxs-lookup"><span data-stu-id="2b57d-113">A timeline model that organizes video and audio tracks into nested layers, making it easy to manipulate the final production</span></span>
-   <span data-ttu-id="2b57d-114">Die Möglichkeit, im Handumdrehen ein Videoprojekt anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="2b57d-114">The ability to preview a video project on the fly</span></span>
-   <span data-ttu-id="2b57d-115">Projekt Persistenz durch ein XML-basiertes Format</span><span class="sxs-lookup"><span data-stu-id="2b57d-115">Project persistence through an XML-based format</span></span>
-   <span data-ttu-id="2b57d-116">Unterstützung für Video-und Audioeffekte sowie Übergänge zwischen Videospuren (z. b. "Fades" und "Wipes")</span><span class="sxs-lookup"><span data-stu-id="2b57d-116">Support for video and audio effects, as well as transitions between video tracks (such as fades and wipes)</span></span>
-   <span data-ttu-id="2b57d-117">Über 100 Standard-Wipes, wie von der Motion Picture-und TV Engineers (SMPTE) definiert</span><span class="sxs-lookup"><span data-stu-id="2b57d-117">Over 100 standard wipes, as defined by the Society of Motion Picture and Television Engineers (SMPTE)</span></span>
-   <span data-ttu-id="2b57d-118">Schlüssel Erstellung basierend auf Hue, Leuchtkraft, RGB-Wert oder Alpha-Wert</span><span class="sxs-lookup"><span data-stu-id="2b57d-118">Keying based on hue, luminance, RGB value, or alpha value</span></span>
-   <span data-ttu-id="2b57d-119">Automatische Konvertierung von Frameraten und audiosamplings, sodass in einer Produktionsumgebung heterogene Quellen verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="2b57d-119">Automatic conversion of frame rates and audio sampling rates, enabling a production to use heterogeneous sources</span></span>
-   <span data-ttu-id="2b57d-120">Ändern der Größe oder des schneidende eines Videos</span><span class="sxs-lookup"><span data-stu-id="2b57d-120">Resizing or cropping of video</span></span>

<span data-ttu-id="2b57d-121">Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="2b57d-121">Limitations:</span></span>

-   <span data-ttu-id="2b57d-122">DES unterstützt keine MPEG-2-oder H. 264-Videoquellen.</span><span class="sxs-lookup"><span data-stu-id="2b57d-122">DES does not support MPEG-2 or H.264 video sources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b57d-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b57d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b57d-124">DirectShow-Bearbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="2b57d-124">DirectShow Editing Services</span></span>](directshow-editing-services.md)
</dt> </dl>

 

 



