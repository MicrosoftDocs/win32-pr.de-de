---
description: Informationen zur Raten Kontrolle
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Informationen zur Raten Kontrolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346306"
---
# <a name="about-rate-control"></a><span data-ttu-id="b64b4-103">Informationen zur Raten Kontrolle</span><span class="sxs-lookup"><span data-stu-id="b64b4-103">About Rate Control</span></span>

<span data-ttu-id="b64b4-104">In Media Foundation wird die *Wiedergabe Rate* als Verhältnis zwischen der aktuellen Wiedergabe Rate und der normalen Wiedergabe Rate ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="b64b4-104">In Media Foundation, the *playback rate* is expressed as the ratio of the current playback rate to the normal playback rate.</span></span> <span data-ttu-id="b64b4-105">Beispielsweise ist die Rate 2,0 doppelt so hoch, dass 0,5 eine halbe normale Geschwindigkeit ist.</span><span class="sxs-lookup"><span data-stu-id="b64b4-105">For example, a rate of 2.0 is twice normal speed, and 0.5 is half normal speed.</span></span> <span data-ttu-id="b64b4-106">Negative Werte geben die umgekehrte Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="b64b4-106">Negative values indicate reverse playback.</span></span> <span data-ttu-id="b64b4-107">Die Wiedergabe Rate von-2,0 wird mit der doppelten Geschwindigkeit der normalen Geschwindigkeit rückwärts durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b64b4-107">A playback rate of -2.0 plays backward through the stream at twice the normal speed.</span></span> <span data-ttu-id="b64b4-108">Eine Rate von NULL bewirkt, dass ein Frame gerendert wird. Danach wird die Präsentationszeit nicht Fortschritt.</span><span class="sxs-lookup"><span data-stu-id="b64b4-108">A rate of zero causes one frame to be rendered; after that, the presentation clock does not advance.</span></span> <span data-ttu-id="b64b4-109">Um einen weiteren Frame mit der Rate 0 zu erhalten, muss die Anwendung an einer neuen Position suchen.</span><span class="sxs-lookup"><span data-stu-id="b64b4-109">To get another frame at the rate of zero, the application must seek to a new position.</span></span>

<span data-ttu-id="b64b4-110">Anwendungen verwenden die folgenden Schnittstellen zum Steuern der Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="b64b4-110">Applications use the following interfaces to control the playback rate.</span></span>

-   <span data-ttu-id="b64b4-111">[**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="b64b4-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="b64b4-112">Wird verwendet, um die schnellsten und langsamsten Wiedergabe Raten zu ermitteln, die möglich sind.</span><span class="sxs-lookup"><span data-stu-id="b64b4-112">Used to find out the fastest and slowest playback rates that are possible.</span></span>
-   <span data-ttu-id="b64b4-113">[**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span><span class="sxs-lookup"><span data-stu-id="b64b4-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="b64b4-114">Wird verwendet, um die Wiedergabe Rate zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b64b4-114">Used to change the playback rate.</span></span>

<span data-ttu-id="b64b4-115">Um diese beiden Schnittstellen abzurufen, nennen Sie [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) für die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b64b4-115">To get these two interfaces, call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the Media Session.</span></span> <span data-ttu-id="b64b4-116">Der Dienst Bezeichner ist der MF- \_ Raten \_ Steuerungs \_ Dienst.</span><span class="sxs-lookup"><span data-stu-id="b64b4-116">The service identifier is MF\_RATE\_CONTROL\_SERVICE.</span></span>

<span data-ttu-id="b64b4-117">Mithilfe des Raten Steuerungs Dienstanbieter kann eine Anwendung die schnelle Vorwärts-und Rückwärts Wiedergabe implementieren.</span><span class="sxs-lookup"><span data-stu-id="b64b4-117">By using the rate control service, an application can implement fast forward and reverse playback.</span></span>

## <a name="thinning"></a><span data-ttu-id="b64b4-118">Wird dünner</span><span class="sxs-lookup"><span data-stu-id="b64b4-118">Thinning</span></span>

<span data-ttu-id="b64b4-119">Die *Verdünnung* ist ein beliebiger Prozess, bei dem die Anzahl der Stichproben in einem Stream verringert wird, um die allgemeine Bitrate zu verringern.</span><span class="sxs-lookup"><span data-stu-id="b64b4-119">*Thinning* is any process that reduces the number of samples in a stream, to reduce the overall bit rate.</span></span> <span data-ttu-id="b64b4-120">Bei Video wird die Verdünnung in der Regel durch Löschen der Delta Frames und Bereitstellung der Keyframes erreicht.</span><span class="sxs-lookup"><span data-stu-id="b64b4-120">For video, thinning is generally accomplished by dropping the delta frames and delivering only the key frames.</span></span> <span data-ttu-id="b64b4-121">Häufig kann die Pipeline schnellere Wiedergabe Raten mithilfe der dünnen Wiedergabe unterstützen, da die Datenrate geringer ist, da Delta Frames nicht decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="b64b4-121">Often the pipeline can support faster playback rates using thinned playback, because the data rate is lower because delta frames are not decoded.</span></span>

<span data-ttu-id="b64b4-122">Beim dünken werden die Zeitstempel oder die Dauer der Stichproben nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="b64b4-122">Thinning does not change the time stamps or durations on the samples.</span></span> <span data-ttu-id="b64b4-123">Wenn die nominale Rate des Videodaten Stroms z. b. 25 Frames pro Sekunde beträgt, wird die Dauer jedes Frames weiterhin als 40 Millisekunden gekennzeichnet, auch wenn die Medienquelle alle Delta Frames löscht.</span><span class="sxs-lookup"><span data-stu-id="b64b4-123">For example, if the nominal rate of the video stream is 25 frames per second, the duration of each frame is still marked as 40 milliseconds, even if the media source is dropping all of the delta frames.</span></span> <span data-ttu-id="b64b4-124">Dies bedeutet, dass zwischen dem Ende eines Frames und dem Beginn der nächsten ein Zeitunterschied besteht.</span><span class="sxs-lookup"><span data-stu-id="b64b4-124">That means there will be a time gap between the end of one frame and the start of the next.</span></span>

## <a name="scrubbing"></a><span data-ttu-id="b64b4-125">Scrubbing (Bereinigung)</span><span class="sxs-lookup"><span data-stu-id="b64b4-125">Scrubbing</span></span>

<span data-ttu-id="b64b4-126">*Scrubbing* ist der Prozess der sofortigen Suche nach bestimmten Punkten im Stream durch Interaktion mit einer Scrollleiste, einer Zeitachse oder einer anderen visuellen Darstellung der Zeit.</span><span class="sxs-lookup"><span data-stu-id="b64b4-126">*Scrubbing* is the process of instantaneously seeking to specific points in the stream by interacting with a scrollbar, timeline, or other visual representation of time.</span></span> <span data-ttu-id="b64b4-127">Die Bezeichnung ergibt sich aus dem Zeitpunkt der Band-zu-Band-bandspieler, wenn eine Bewegung hin und her herumrollt, um zu ermitteln, ob der Wiedergabe Kopf mit dem Band bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="b64b4-127">The term comes from the era of reel-to-reel tape players when rocking a reel back and forth to locate a section was like scrubbing the playback head with the tape.</span></span>

<span data-ttu-id="b64b4-128">Das Scrubbing wird in Media Foundation implementiert, indem die Wiedergabe Rate auf NULL festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b64b4-128">Scrubbing is implemented in Media Foundation by setting the playback rate to zero.</span></span> <span data-ttu-id="b64b4-129">Weitere Informationen finden Sie unter Vorgehens [Weise beim Ausführen von Scrubbing](how-to-perform-scrubbing.md).</span><span class="sxs-lookup"><span data-stu-id="b64b4-129">For more information, see [How to Perform Scrubbing](how-to-perform-scrubbing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b64b4-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b64b4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b64b4-131">Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="b64b4-131">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="b64b4-132">Suchen, schnelles vorwärts und umgekehrtes spielen</span><span class="sxs-lookup"><span data-stu-id="b64b4-132">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[<span data-ttu-id="b64b4-133">Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b64b4-133">Service Interfaces</span></span>](service-interfaces.md)
</dt> </dl>

 

 



