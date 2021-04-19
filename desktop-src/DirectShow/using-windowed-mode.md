---
description: Verwenden des Fenstermodus
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Verwenden des Fenstermodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368855"
---
# <a name="using-windowed-mode"></a><span data-ttu-id="bdf7d-103">Verwenden des Fenstermodus</span><span class="sxs-lookup"><span data-stu-id="bdf7d-103">Using Windowed Mode</span></span>

> [!Note]  
> <span data-ttu-id="bdf7d-104">Der Legacy- [Videorenderer-Filter](video-renderer-filter.md) verwendet immer den Fenstermodus.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-104">The legacy [Video Renderer Filter](video-renderer-filter.md) always uses windowed mode.</span></span> <span data-ttu-id="bdf7d-105">Der VMR-7-und der VMR-9-Filter verwenden standardmäßig den Fenstermodus, unterstützen aber auch den fensterlosen Modus.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-105">The VMR-7 and VMR-9 filters use windowed mode by default, but also support windowless mode.</span></span>

 

<span data-ttu-id="bdf7d-106">Im Fenstermodus erstellt der Videorenderer ein eigenes Fenster, in dem die Video Frames gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-106">In windowed mode, the video renderer creates its own window where it paints the video frames.</span></span> <span data-ttu-id="bdf7d-107">Wenn Sie nicht anders angeben, ist dieses Fenster ein Fenster der obersten Ebene mit seinen eigenen Rahmen und Titelleiste.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-107">Unless you specify otherwise, this window is a top-level window with its own borders and title bar.</span></span> <span data-ttu-id="bdf7d-108">In den meisten Fällen fügen Sie jedoch das Videofenster an ein Anwendungsfenster an, damit das Video in die Benutzeroberfläche der Anwendung integriert ist.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-108">Most of the time, however, you will attach the video window to an application window, so that the video is integrated into your application UI.</span></span> <span data-ttu-id="bdf7d-109">Gehen Sie dazu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="bdf7d-109">This requires the following steps:</span></span>

1.  <span data-ttu-id="bdf7d-110">Abfrage für **IVideoWindow**.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-110">Query for **IVideoWindow**.</span></span>
2.  <span data-ttu-id="bdf7d-111">Legen Sie das übergeordnete Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-111">Set the parent window.</span></span>
3.  <span data-ttu-id="bdf7d-112">Legen Sie neue Fenster Stile fest.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-112">Set new window styles.</span></span>
4.  <span data-ttu-id="bdf7d-113">Positionieren Sie das Videofenster im Fenster Besitzer.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-113">Position the video window inside the owner window.</span></span>
5.  <span data-ttu-id="bdf7d-114">Benachrichtigen Sie das Videofenster über das \_ Verschieben von Nachrichten von WM.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-114">Notify the video window of WM\_MOVE messages.</span></span>

<span data-ttu-id="bdf7d-115">**Abfrage für IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="bdf7d-115">**Query for IVideoWindow**</span></span>

<span data-ttu-id="bdf7d-116">Fragen Sie vor der Wiedergabe den Filter Graph-Manager nach der **IVideoWindow** -Schnittstelle ab:</span><span class="sxs-lookup"><span data-stu-id="bdf7d-116">Before starting playback, query the Filter Graph Manager for the **IVideoWindow** interface:</span></span>


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



<span data-ttu-id="bdf7d-117">**Übergeordnetes Fenster festlegen**</span><span class="sxs-lookup"><span data-stu-id="bdf7d-117">**Set the Parent Window**</span></span>

<span data-ttu-id="bdf7d-118">Um das übergeordnete Fenster festzulegen, müssen Sie die [**:p UT- \_ Besitzer**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) Methode mit einem Handle für das Anwendungsfenster aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-118">To set the parent window, call the [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) method with a handle to your application window.</span></span> <span data-ttu-id="bdf7d-119">Diese Methode nimmt eine Variable vom Typ [**oahwnd**](oahwnd.md)auf, deshalb wandeln Sie den Handle in diesen Typ um:</span><span class="sxs-lookup"><span data-stu-id="bdf7d-119">This method takes a variable of type [**OAHWND**](oahwnd.md), so cast the handle to this type:</span></span>


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



<span data-ttu-id="bdf7d-120">**Neue Fenster Stile festlegen**</span><span class="sxs-lookup"><span data-stu-id="bdf7d-120">**Set New Window Styles**</span></span>

<span data-ttu-id="bdf7d-121">Ändern Sie den Stil des Videofensters, indem Sie die Methode [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) aufrufen:</span><span class="sxs-lookup"><span data-stu-id="bdf7d-121">Change the style of the video window by calling the [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) method:</span></span>


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



<span data-ttu-id="bdf7d-122">Mit dem untergeordneten WS \_ -Flag wird das Fenster als untergeordnetes Fenster festgelegt, und das WS \_ clipneben-Flag verhindert, dass das Fenster innerhalb des Client Bereichs eines anderen untergeordneten Fensters gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-122">The WS\_CHILD flag sets the window to be a child window, and the WS\_CLIPSIBLINGS flag prevents the window from drawing inside the client area of another child window.</span></span>

<span data-ttu-id="bdf7d-123">**Positionieren des Video Fensters**</span><span class="sxs-lookup"><span data-stu-id="bdf7d-123">**Position the Video Window**</span></span>

<span data-ttu-id="bdf7d-124">Um die Position des Videos relativ zum Client Bereich des Anwendungsfensters festzulegen, müssen Sie die [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-124">To set the position of the video relative to the application window's client area, call the [**IVideoWindow::SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) method.</span></span> <span data-ttu-id="bdf7d-125">Diese Methode nimmt ein Rechteck an, das den linken Rand, den oberen Rand, die Breite und die Höhe des Videofensters angibt.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-125">This method takes a rectangle that specifies the left edge, top edge, width, and height of the video window.</span></span> <span data-ttu-id="bdf7d-126">Mit dem folgenden Code wird z. b. das Videofenster so gestreckt, dass es dem gesamten Client Bereich des übergeordneten Fensters entspricht:</span><span class="sxs-lookup"><span data-stu-id="bdf7d-126">For example, the following code stretches the video window to fit the entire client area of the parent window:</span></span>


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



<span data-ttu-id="bdf7d-127">Um die systemeigene Größe des Videos abzurufen, müssen Sie die [**ibasicvideo:: getvideosize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) -Methode für den Filter Graph-Manager aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-127">To get the native size of the video, call the [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) method on the Filter Graph Manager.</span></span> <span data-ttu-id="bdf7d-128">Sie können diese Informationen verwenden, um das Video zu skalieren und das richtige Seitenverhältnis beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-128">You can use that information to scale the video and keep the correct aspect ratio.</span></span>

<span data-ttu-id="bdf7d-129">**Antworten auf WM-Verschiebungs \_ Meldungen**</span><span class="sxs-lookup"><span data-stu-id="bdf7d-129">**Respond to WM\_MOVE Messages**</span></span>

<span data-ttu-id="bdf7d-130">Um die optimale Leistung zu erzielen, sollten Sie den Videorenderer Benachrichtigen, wenn das Fenster bewegt wird, während das Diagramm angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-130">For best performance, you should notify the video renderer whenever the window moves while the graph is paused.</span></span> <span data-ttu-id="bdf7d-131">Um die WM-Verschiebungs Nachricht weiterzuleiten, wenden Sie die [**IVideoWindow:: notifyownermessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) -Methode an \_ :</span><span class="sxs-lookup"><span data-stu-id="bdf7d-131">Call the [**IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) method to forward the WM\_MOVE message:</span></span>


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



<span data-ttu-id="bdf7d-132">Wenn der Renderer eine Hardware Überlagerung verwendet, bewirkt diese Benachrichtigung, dass der Renderer die Überlagerungs Position aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-132">If the renderer is using a hardware overlay, this notification causes the renderer to update the overlay position.</span></span> <span data-ttu-id="bdf7d-133">(VMR-9 verwendet keine Überlagerungen, daher müssen Sie diese Methode nicht aufzurufen, wenn Sie VMR-9 verwenden.)</span><span class="sxs-lookup"><span data-stu-id="bdf7d-133">(The VMR-9 does not use overlays, so you do not need to call this method if you are using the VMR-9.)</span></span>

<span data-ttu-id="bdf7d-134">**Bereinigen**</span><span class="sxs-lookup"><span data-stu-id="bdf7d-134">**Clean Up**</span></span>

<span data-ttu-id="bdf7d-135">Bevor die Anwendung beendet wird, beenden Sie das Diagramm, und setzen Sie den Besitzer des Videofensters auf **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-135">Before the application exits, stop the graph and reset the video window's owner to **NULL**.</span></span> <span data-ttu-id="bdf7d-136">Andernfalls werden möglicherweise Fenster Meldungen an das falsche Fenster gesendet, was wahrscheinlich zu Fehlern führt.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-136">Otherwise, window messages might be sent to the wrong window, which is likely to cause errors.</span></span> <span data-ttu-id="bdf7d-137">Außerdem können Sie das Videofenster ausblenden, oder Sie sehen, dass auf dem Bildschirm vorübergehend ein Video Bild flimmern angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="bdf7d-137">Also, hide video window, or else you might see a video image flicker on the screen momentarily:</span></span>


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> <span data-ttu-id="bdf7d-138">Wenn das übergeordnete Element des Videofensters ein untergeordnetes Element des Haupt Anwendungsfensters ist (d. h., wenn das Videofenster einem untergeordneten Element untergeordnet ist), sollten Sie das Videofenster mithilfe von **cokreateinstance** erstellen und dem Diagramm hinzufügen, anstatt den Filter Diagramm-Manager bei [intelligenter Verbindung](intelligent-connect.md)hinzufügen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-138">If the parent of the video window is a child of your main application window (in other words, if the video window is a child of a child), you should create the video window using **CoCreateInstance** and add it to the graph, instead of letting the Filter Graph Manager add the video renderer during [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="bdf7d-139">Dadurch wird sichergestellt, dass das Videofenster und das untergeordnete Fenster gleichzeitig neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-139">This ensures that the video window and your child window are repainted at the same time.</span></span> <span data-ttu-id="bdf7d-140">Andernfalls wird das untergeordnete Fenster möglicherweise über das Videofenster gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-140">Otherwise, the child window may paint over the video window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bdf7d-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bdf7d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdf7d-142">Videorendering</span><span class="sxs-lookup"><span data-stu-id="bdf7d-142">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



