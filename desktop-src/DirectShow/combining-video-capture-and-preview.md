---
description: Kombinieren von Video Erfassung und Vorschau
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Kombinieren von Video Erfassung und Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481174"
---
# <a name="combining-video-capture-and-preview"></a><span data-ttu-id="32011-103">Kombinieren von Video Erfassung und Vorschau</span><span class="sxs-lookup"><span data-stu-id="32011-103">Combining Video Capture and Preview</span></span>

<span data-ttu-id="32011-104">In den vorherigen Abschnitten wird beschrieben, wie Videos in verschiedenen Dateiformaten aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="32011-104">The previous sections describe how to capture video to various file formats.</span></span> <span data-ttu-id="32011-105">Im Abschnitt [Vorschau Video](previewing-video.md) wird beschrieben, wie ein Live Vorschau Diagramm erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32011-105">The section [Previewing Video](previewing-video.md) describes how to build a live preview graph.</span></span> <span data-ttu-id="32011-106">Viele Anwendungen müssen jedoch beide gleichzeitig ausführen.</span><span class="sxs-lookup"><span data-stu-id="32011-106">However, many applications must do both at once.</span></span> <span data-ttu-id="32011-107">Um ein kombiniertes Vorschau-und Datei Schreib Diagramm zu erstellen, führen Sie einfach zwei Aufrufe von [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)aus:</span><span class="sxs-lookup"><span data-stu-id="32011-107">To build a combined preview and file-writing graph, simply make two calls to [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span></span>


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



<span data-ttu-id="32011-108">In diesem Code verbirgt der Erfassungs Diagramm-Generator einige Details:</span><span class="sxs-lookup"><span data-stu-id="32011-108">In this code, the Capture Graph Builder is hiding some details:</span></span>

-   <span data-ttu-id="32011-109">Wenn der Erfassungs Filter eine Vorschau-PIN oder eine Videoport-PIN sowie eine Aufzeichnungs-Pin aufweist, rendert die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode einfach beide Pins, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32011-109">If the capture filter has a preview pin or video port pin, plus a capture pin, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method simply renders both pins, as shown in the following illustration.</span></span>

    ![Erfassungs-und Vorschau Diagramm](images/vidcap04.png)

-   <span data-ttu-id="32011-111">Wenn der Filter nur über eine Erfassungs-Pin verfügt, verwendet der Erfassungs Diagramm-Generator den [Smart Tee](smart-tee-filter.md) -Filter, um den Erfassungsdaten Strom aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="32011-111">If the filter has only a capture pin, the Capture Graph Builder uses the [Smart Tee](smart-tee-filter.md) filter to split the capture stream.</span></span> <span data-ttu-id="32011-112">Die folgende Abbildung zeigt das Diagramm mit einem intelligenten Tee.</span><span class="sxs-lookup"><span data-stu-id="32011-112">The following illustration shows the graph with a Smart Tee.</span></span>

    ![Erfassung und Vorschau des Diagramms mit Smart Tee Filter](images/vidcap05.png)

<span data-ttu-id="32011-114">Der Smart Tee-Filter verfügt über eine Erfassungs-PIN und eine Vorschau-PIN.</span><span class="sxs-lookup"><span data-stu-id="32011-114">The Smart Tee filter has a capture pin and a preview pin.</span></span> <span data-ttu-id="32011-115">Er nimmt einen einzelnen Videostream aus dem Erfassungs Filter und teilt ihn in zwei Streams auf: einen für die Erfassung und einen für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="32011-115">It takes a single video stream from the capture filter and splits it into two streams, one for capture and one for preview.</span></span> <span data-ttu-id="32011-116">Um den Durchsatz auf der Erfassungs-Pin aufrechtzuerhalten, löscht die Vorschau-Pin Frames nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="32011-116">To maintain throughput on the capture pin, the preview pin drops frames as needed.</span></span> <span data-ttu-id="32011-117">Außerdem werden die Zeitstempel aus den einzelnen Stichproben entfernt, bevor Sie bereitgestellt werden, aus den im Thema [DirectShow-Video Erfassungs Filtern](directshow-video-capture-filters.md)beschriebenen Gründen.</span><span class="sxs-lookup"><span data-stu-id="32011-117">It also strips the time stamps from each sample before delivering it, for the reasons discussed in the topic [DirectShow Video Capture Filters](directshow-video-capture-filters.md).</span></span>

<span data-ttu-id="32011-118">Obwohl der intelligente Tee den Stream teilt, werden die Videodaten nicht physisch dupliziert.</span><span class="sxs-lookup"><span data-stu-id="32011-118">Although the Smart Tee splits the stream, it does not physically duplicate the video data.</span></span> <span data-ttu-id="32011-119">Stattdessen werden benutzerdefinierte Medien Beispiel Objekte verwendet, die die Puffer gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="32011-119">Instead, it uses custom media sample objects that share the buffers.</span></span> <span data-ttu-id="32011-120">Die Beispiele sind als "schreibgeschützt" gekennzeichnet, um sicherzustellen, dass downstreamfilter nicht auf die Daten schreiben.</span><span class="sxs-lookup"><span data-stu-id="32011-120">The samples are marked "read-only" to ensure that downstream filters do not write on the data.</span></span>

<span data-ttu-id="32011-121">Wenn das Erfassungs Diagramm über ein Vorschaufenster verfügt, kann es passieren, dass der Filter Graph-Manager das gesamte Diagramm, einschließlich des Erfassungsdaten Stroms, beendet:</span><span class="sxs-lookup"><span data-stu-id="32011-121">If your capture graph has a preview window, several things can cause the Filter Graph Manager to stop the entire graph, including the capture stream:</span></span>

-   <span data-ttu-id="32011-122">Sperren des Computers.</span><span class="sxs-lookup"><span data-stu-id="32011-122">Locking the computer.</span></span>
-   <span data-ttu-id="32011-123">Drücken von STRG + ALT + ENTF auf einem Computer, der Mitglied einer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="32011-123">Pressing CTRL+ALT+DELETE on a computer that is a member of a domain.</span></span>
-   <span data-ttu-id="32011-124">Ausführen einer Vollbild-Direct3D-Anwendung, z. b. eines Spiels oder Bildschirmschoners.</span><span class="sxs-lookup"><span data-stu-id="32011-124">Running a full-screen Direct3D application, such as a game or screen saver.</span></span>
-   <span data-ttu-id="32011-125">Wechseln von Monitoren oder Ändern der Bildschirmauflösung.</span><span class="sxs-lookup"><span data-stu-id="32011-125">Switching monitors or changing the display resolution.</span></span>
-   <span data-ttu-id="32011-126">Ausführen eines Programms, das dazu führt, dass Windows ein Dialogfeld für die Benutzerkontensteuerung (UAC) anzeigt.</span><span class="sxs-lookup"><span data-stu-id="32011-126">Running a program that causes Windows to display a User Account Control (UAC) dialog.</span></span> <span data-ttu-id="32011-127">(Windows Vista oder höher)</span><span class="sxs-lookup"><span data-stu-id="32011-127">(Windows Vista or later.)</span></span>
-   <span data-ttu-id="32011-128">Ausführen eines Vollbild-DOS-Fensters.</span><span class="sxs-lookup"><span data-stu-id="32011-128">Running a full-screen DOS window.</span></span>

<span data-ttu-id="32011-129">Diese Ereignisse können die Erfassungs Sitzung unterbrechen und möglicherweise zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="32011-129">Any of these events might interrupt the capture session, possibly causing data loss.</span></span> <span data-ttu-id="32011-130">(Dies geschieht intern: der Videorenderer verliert die Direct3D-oder DirectDraw-Ressourcen, die er benötigt.</span><span class="sxs-lookup"><span data-stu-id="32011-130">(Here is what happens internally: The video renderer loses the Direct3D or DirectDraw resources that it needs.</span></span> <span data-ttu-id="32011-131">Beim Wiederherstellen dieser Ressourcen muss der Videorenderer erneut eine Verbindung mit dem upstreamfilter herstellen, wodurch der Filter Graph-Manager das Diagramm beendet.)</span><span class="sxs-lookup"><span data-stu-id="32011-131">In the process of recovering those resources, the video renderer must reconnect with the upstream filter, causing the Filter Graph Manager to stop the graph.)</span></span>

<span data-ttu-id="32011-132">Es gibt zwei mögliche Lösungen für dieses Problem:</span><span class="sxs-lookup"><span data-stu-id="32011-132">Two possible solutions to this problem are the following:</span></span>

-   <span data-ttu-id="32011-133">Schließen Sie keinen Vorschau Datenstrom ein.</span><span class="sxs-lookup"><span data-stu-id="32011-133">Do not include a preview stream.</span></span> <span data-ttu-id="32011-134">Beachten Sie jedoch, dass die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode automatisch ein Vorschaufenster hinzufügt, wenn das Erfassungsgerät über eine Videoport-Pin verfügt.</span><span class="sxs-lookup"><span data-stu-id="32011-134">However, be aware that the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically adds a preview window when the capture device has a video port pin.</span></span> <span data-ttu-id="32011-135">Siehe [Video Port Pins in file Capture](video-port-pins-in-file-capture.md).</span><span class="sxs-lookup"><span data-stu-id="32011-135">See [Video Port Pins in File Capture](video-port-pins-in-file-capture.md).</span></span>
-   <span data-ttu-id="32011-136">Verwenden Sie die streampufferengine, um den Vorschau Datenstrom in einem anderen Prozess an ein Diagramm zu senden.</span><span class="sxs-lookup"><span data-stu-id="32011-136">Use the Stream Buffer Engine to send the preview stream to a graph in another process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32011-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32011-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32011-138">Aufzeichnen von Videos in einer Datei</span><span class="sxs-lookup"><span data-stu-id="32011-138">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



