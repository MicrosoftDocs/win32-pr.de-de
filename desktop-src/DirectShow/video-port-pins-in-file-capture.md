---
description: Video Port Pins in der Datei Erfassung
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Video Port Pins in der Datei Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347270"
---
# <a name="video-port-pins-in-file-capture"></a><span data-ttu-id="34c67-103">Video Port Pins in der Datei Erfassung</span><span class="sxs-lookup"><span data-stu-id="34c67-103">Video Port Pins in File Capture</span></span>

<span data-ttu-id="34c67-104">Wenn das Erfassungsgerät über einen Videoport verfügt, muss die Videoport-PIN mit einem Videorenderer verbunden werden, auch wenn Sie nur in einer Datei erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="34c67-104">If the capture device has a video port, the video port pin must be connected to a video renderer, even if you only want to capture to a file.</span></span>

<span data-ttu-id="34c67-105">Wenn Sie " [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) " mit dem Wert " **Pin \_ Category \_ Capture** " und dem Gerät eine Videoport-Pin aufzurufen, verbindet der Erfassungs Diagramm-Generator automatisch die Videoport-PIN mit dem [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter und verbindet den Overlay-Mixer mit dem Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="34c67-105">If you call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the value **PIN\_CATEGORY\_CAPTURE** and the device has a video port pin, the Capture Graph Builder automatically connects the video port pin to the [Overlay Mixer](overlay-mixer-filter.md) filter and connects the Overlay Mixer to the Video Renderer.</span></span> <span data-ttu-id="34c67-106">Der Erfassungs Diagramm-Generator verbirgt das Videofenster durch Aufrufen von [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert **oafalse**.</span><span class="sxs-lookup"><span data-stu-id="34c67-106">The Capture Graph Builder hides the video window by calling [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value **OAFALSE**.</span></span> <span data-ttu-id="34c67-107">Wenn die Anwendung später **RenderStream** mit der **Pin- \_ Kategorie \_ Vorschau** aufruft, ruft der Erfassungs Diagramm-Generator " **Put \_ AutoShow** " mit dem Wert " **oatrue**" auf, um das Videofenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="34c67-107">If the application later calls **RenderStream** with **PIN\_CATEGORY\_PREVIEW**, the Capture Graph Builder calls **put\_AutoShow** with the value **OATRUE**, in order to show the video window.</span></span>

<span data-ttu-id="34c67-108">Nachdem Sie **RenderStream** mit **Pin \_ Category \_ Capture** aufgerufen haben, können Sie überprüfen, ob der Videorenderer hinzugefügt wurde, indem Sie den Filter Graph-Manager nach der [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="34c67-108">After you call **RenderStream** with **PIN\_CATEGORY\_CAPTURE**, you can check whether it has added the Video Renderer by querying the Filter Graph Manager for the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34c67-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34c67-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34c67-110">Aufzeichnen von Videos in einer Datei</span><span class="sxs-lookup"><span data-stu-id="34c67-110">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



