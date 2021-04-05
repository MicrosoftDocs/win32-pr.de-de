---
description: Verwenden der Video Anzeige Steuerelemente
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Verwenden der Video Anzeige Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753825"
---
# <a name="using-the-video-display-controls"></a><span data-ttu-id="d729c-103">Verwenden der Video Anzeige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d729c-103">Using the Video Display Controls</span></span>

<span data-ttu-id="d729c-104">Die [**IMF videodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle steuert, wie der erweiterte Videorenderer (EVR) ein Video in einem Anwendungsfenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d729c-104">The [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface controls how the enhanced video renderer (EVR) displays video inside an application window.</span></span> <span data-ttu-id="d729c-105">Diese Schnittstelle kann entweder in DirectShow oder Media Foundation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d729c-105">This interface can be used in either DirectShow or Media Foundation.</span></span> <span data-ttu-id="d729c-106">Intern werden die Videoanzeige Steuerelemente vom Standard Presenter von EVR bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d729c-106">Internally, the video display controls are provided by the EVR's default presenter.</span></span> <span data-ttu-id="d729c-107">Wenn Sie einen benutzerdefinierten Presenter schreiben, können Sie die gleiche Schnittstelle bereitstellen oder eine benutzerdefinierte Schnittstelle definieren.</span><span class="sxs-lookup"><span data-stu-id="d729c-107">If you write a custom presenter, you can provide the same interface or define a custom interface.</span></span>

<span data-ttu-id="d729c-108">Die korrekte Methode, einen Zeiger auf die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle zu erhalten, hängt davon ab, ob Sie die DirectShow-Version von EVR oder die Media Foundation Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="d729c-108">The correct way to get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface depends on whether you are using the DirectShow version of the EVR or the Media Foundation version.</span></span> <span data-ttu-id="d729c-109">Für den Media Foundation EVR hängt es auch davon ab, ob Sie den EVR direkt verwenden oder über die Medien Sitzung verwenden (was eher typisch ist).</span><span class="sxs-lookup"><span data-stu-id="d729c-109">For the Media Foundation EVR, it also depends on whether you are using the EVR directly or using it through the Media Session (which is more typical).</span></span>

<span data-ttu-id="d729c-110">Gehen Sie folgendermaßen vor, um einen Zeiger auf die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d729c-110">To get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface, do the following:</span></span>

1.  <span data-ttu-id="d729c-111">Einen Zeiger auf die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="d729c-111">Get a pointer to the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>

    -   <span data-ttu-id="d729c-112">Wenn Sie den DirectShow-EVR-Filter verwenden, können Sie **QueryInterface** für den Filter aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d729c-112">If you are using the DirectShow EVR filter, call **QueryInterface** on the filter.</span></span>

    -   <span data-ttu-id="d729c-113">Wenn Sie die EVR-Medien Senke direkt verwenden, können Sie **QueryInterface** in der Medien Senke aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d729c-113">If you are using the EVR media sink directly, call **QueryInterface** on the media sink.</span></span>

    -   <span data-ttu-id="d729c-114">Wenn Sie die Medien Sitzung verwenden, können Sie **QueryInterface** in der Medien Sitzung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d729c-114">If you are using the Media Session, call **QueryInterface** on the Media Session.</span></span>

2.  <span data-ttu-id="d729c-115">Wenn Sie die Medien Sitzung verwenden, warten Sie, bis die Medien Sitzung das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) mit dem Statuswert MF \_ topostatus Ready sendet \_ .</span><span class="sxs-lookup"><span data-stu-id="d729c-115">If you are using the Media Session, wait for the Media Session to send the [MESessionTopologyStatus](mesessiontopologystatus.md) event with a status value of MF\_TOPOSTATUS\_READY.</span></span> <span data-ttu-id="d729c-116">(Überspringen Sie andernfalls diesen Schritt.)</span><span class="sxs-lookup"><span data-stu-id="d729c-116">(Skip this step otherwise.)</span></span>

3.  <span data-ttu-id="d729c-117">Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) zum Abrufen der [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d729c-117">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span> <span data-ttu-id="d729c-118">Der Dienst Bezeichner ist der Video-Rendering-Dienst von Mr \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d729c-118">The service identifier is MR\_VIDEO\_RENDER\_SERVICE.</span></span>

<span data-ttu-id="d729c-119">Sie können die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle verwenden, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="d729c-119">You can use the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="d729c-120">Legen Sie das clippingfenster fest.</span><span class="sxs-lookup"><span data-stu-id="d729c-120">Set the clipping window.</span></span>

-   <span data-ttu-id="d729c-121">Legen Sie die Quell-und Ziel Rechtecke fest.</span><span class="sxs-lookup"><span data-stu-id="d729c-121">Set the source and destination rectangles.</span></span>

-   <span data-ttu-id="d729c-122">Aktualisieren Sie das Videofenster als Reaktion auf Fenster Meldungen.</span><span class="sxs-lookup"><span data-stu-id="d729c-122">Update the video window in response to window messages.</span></span>

-   <span data-ttu-id="d729c-123">Aktiviert oder deaktiviert den Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="d729c-123">Enable or disable full-screen mode.</span></span>

## <a name="clipping-window"></a><span data-ttu-id="d729c-124">Clipping-Fenster</span><span class="sxs-lookup"><span data-stu-id="d729c-124">Clipping Window</span></span>

<span data-ttu-id="d729c-125">Die Anwendung muss ein Fenster bereitstellen, in dem der EVR das Video zeichnet.</span><span class="sxs-lookup"><span data-stu-id="d729c-125">The application must provide a window where the EVR draws the video.</span></span> <span data-ttu-id="d729c-126">Um das clippingfenster festzulegen, müssen Sie [**imfvideodisplaycontrol:: setvideowindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) mit einem Handle für das Anwendungsfenster aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d729c-126">To set the clipping window, call [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) with a handle to the application window.</span></span>

<span data-ttu-id="d729c-127">Dieser Schritt ist nicht erforderlich, wenn Sie die EVR-Medien Senke über das Aktivierungs Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="d729c-127">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="d729c-128">Mithilfe des Fenster Handles, das Sie in der [**MF createvideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion angegeben haben, ruft das Aktivierungs Objekt automatisch [**setvideowindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)auf.</span><span class="sxs-lookup"><span data-stu-id="d729c-128">The activation object automatically calls [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), using the window handle that you provided in the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span>

## <a name="source-and-destination-rectangles"></a><span data-ttu-id="d729c-129">Quell-und Ziel Rechtecke</span><span class="sxs-lookup"><span data-stu-id="d729c-129">Source and Destination Rectangles</span></span>

<span data-ttu-id="d729c-130">Während der Wiedergabe nimmt der Presenter einen Teil des zusammengesetzten Video Bilds an und zeichnet ihn in einem Bereich des Videofensters.</span><span class="sxs-lookup"><span data-stu-id="d729c-130">During playback, the presenter takes a portion of the composited video image and draws it onto an area of the video window.</span></span> <span data-ttu-id="d729c-131">Der Teil des zusammengesetzten Bilds ist das *Quell Rechteck*, und der Bereich des Videofensters ist das *Ziel Rechteck*.</span><span class="sxs-lookup"><span data-stu-id="d729c-131">The portion of the composited image is the *source rectangle*, and the area of the video window is the *destination rectangle*.</span></span>

<span data-ttu-id="d729c-132">Das Quell Rechteck wird mithilfe normalisierter Koordinaten definiert, wobei der Punkt (0,0, 0,0) der oberen linken Ecke des Videos entspricht und (1,0, 1,0) der unteren rechten Ecke des Videos entspricht.</span><span class="sxs-lookup"><span data-stu-id="d729c-132">The source rectangle is defined using normalized coordinates where the point (0.0, 0.0) corresponds to the upper left corner of the video, and (1.0, 1.0) corresponds to the lower right corner of the video.</span></span> <span data-ttu-id="d729c-133">Das Quell Rechteck kann eine beliebige Region innerhalb dieses Rechtecks sein.</span><span class="sxs-lookup"><span data-stu-id="d729c-133">The source rectangle can be any region within this rectangle.</span></span> <span data-ttu-id="d729c-134">Das Ziel Rechteck wird in Pixel relativ zum Client Bereich des Fensters angegeben.</span><span class="sxs-lookup"><span data-stu-id="d729c-134">The destination rectangle is specified in pixels, relative to the client area of the window.</span></span> <span data-ttu-id="d729c-135">Das standardmäßige Quell Rechteck ist das gesamte Bild, und das standardmäßige Ziel Rechteck ist ein leeres Rechteck.</span><span class="sxs-lookup"><span data-stu-id="d729c-135">The default source rectangle is the entire image, and the default destination rectangle is an empty rectangle.</span></span>

<span data-ttu-id="d729c-136">Um die Quell-und Ziel Rechtecke festzulegen, müssen Sie [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d729c-136">To set the source and destination rectangles, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="d729c-137">Dieser Schritt ist nicht erforderlich, wenn Sie die EVR-Medien Senke über das Aktivierungs Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="d729c-137">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="d729c-138">Das Aktivierungs Objekt legt das Ziel Rechteck automatisch auf den gesamten Client Bereich des Fensters fest.</span><span class="sxs-lookup"><span data-stu-id="d729c-138">The activation object automatically sets the destination rectangle equal to the entire client area of the window.</span></span> <span data-ttu-id="d729c-139">Sie sollten jedoch [**setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) aufrufen, wenn Sie das Quell Rechteck ändern oder ein anderes Ziel Rechteck festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="d729c-139">However, you should call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) if you want to change the source rectangle or set a different destination rectangle.</span></span>

## <a name="window-messages"></a><span data-ttu-id="d729c-140">Fenster Meldungen</span><span class="sxs-lookup"><span data-stu-id="d729c-140">Window Messages</span></span>

<span data-ttu-id="d729c-141">Während der Wiedergabe sollte Ihre Anwendung wie folgt auf bestimmte Fenster Meldungen reagieren:</span><span class="sxs-lookup"><span data-stu-id="d729c-141">During playback, your application should respond to certain window messages, as follows:</span></span>

-   <span data-ttu-id="d729c-142">WM \_ Paint: nennen Sie [**imfvideodisplaycontrol:: repaintvideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) , um das Video neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d729c-142">WM\_PAINT: Call [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) to repaint the video.</span></span> <span data-ttu-id="d729c-143">Vermeiden Sie außerdem das Zeichnen über das Ziel Rechteck, während das Video abgespielt wird, da dies zu einem Flimmern führen kann.</span><span class="sxs-lookup"><span data-stu-id="d729c-143">Also, avoid painting over the destination rectangle while video is playing, because this can cause flickering.</span></span>

-   <span data-ttu-id="d729c-144">WM- \_ Größe: Sie müssen möglicherweise [**setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) aufrufen, um die Größe des Ziel Rechtecks zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d729c-144">WM\_SIZE: You might need to call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) to resize the destination rectangle.</span></span>

<span data-ttu-id="d729c-145">Anders als der Filter für Video Mischungs-Renderer (VMR) in DirectShow müssen Sie den EVR nicht benachrichtigen, wenn Sie eine WM \_ Display Change-Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="d729c-145">Unlike the Video Mixing Renderer (VMR) filter in DirectShow, you do not have to notify the EVR when you receive a WM\_DISPLAYCHANGE message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d729c-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d729c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d729c-147">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="d729c-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



