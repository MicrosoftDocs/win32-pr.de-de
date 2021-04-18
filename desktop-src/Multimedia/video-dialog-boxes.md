---
title: Video Dialogfelder
description: Video Dialogfelder
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE Meldung
- capdlgvideosource-Makro
- WM_CAP_DLG_VIDEOFORMAT Meldung
- capdlgvideoformat-Makro
- WM_CAP_DLG_VIDEODISPLAY Meldung
- capdlgvideodisplay-Makro
- WM_CAP_DLG_VIDEOCOMPRESSION Meldung
- capdlgvideocompression-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339797"
---
# <a name="video-dialog-boxes"></a><span data-ttu-id="b6cf8-111">Video Dialogfelder</span><span class="sxs-lookup"><span data-stu-id="b6cf8-111">Video Dialog Boxes</span></span>

<span data-ttu-id="b6cf8-112">Jeder Aufzeichnungs Treiber kann bis zu vier Dialogfelder bereitstellen, um Aspekte der Video Digitalisierung und des Aufzeichnungs Vorgangs zu steuern und Komprimierungs Attribute zu definieren, die zum Verringern der Größe der Videodaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-112">Each capture driver can provide up to four dialog boxes to control aspects of the video digitization and capture process, and to define compression attributes used in reducing the size of the video data.</span></span> <span data-ttu-id="b6cf8-113">Der Inhalt dieser Dialogfelder wird vom Video Erfassungs Treiber definiert.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-113">The contents of these dialog boxes are defined by the video capture driver.</span></span>

<span data-ttu-id="b6cf8-114">Im Dialogfeld Videoquelle wird die Auswahl von Videoeingabe Kanälen und-Parametern gesteuert, die sich auf das im Frame Puffer zu Digitalisier Ende Video Bild auswirken.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-114">The Video Source dialog box controls the selection of video input channels and parameters affecting the video image being digitized in the frame buffer.</span></span> <span data-ttu-id="b6cf8-115">In diesem Dialogfeld werden die Signaltypen aufgelistet, die die Videoquelle mit der aufzeichnungskarte verbinden (in der Regel SVHS und zusammengesetzte Eingaben) und Steuerelemente bereitstellen, um Farbton, Kontrast oder Sättigung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-115">This dialog box enumerates the types of signals that connect the video source to the capture card (typically SVHS and composite inputs), and provides controls to change hue, contrast, or saturation.</span></span> <span data-ttu-id="b6cf8-116">Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mithilfe der WM- [**\_ Cap- \_ DLG- \_ videosource**](wm-cap-dlg-videosource.md) -Nachricht (oder des " [**capdlgvideosource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) "-Makros) anzeigen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-116">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (or the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro).</span></span>

<span data-ttu-id="b6cf8-117">Im Dialogfeld Video Format wird die Auswahl der digitalisierten Video Frame Dimensionen und der Bild-und Komprimierungs Optionen des aufgezeichneten Videos gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-117">The Video Format dialog box controls selection of the digitized video frame dimensions and image-depth, and compression options of the captured video.</span></span> <span data-ttu-id="b6cf8-118">Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mit der Meldung " [**WM \_ Cap \_ DLG \_ Videoformat**](wm-cap-dlg-videoformat.md) " (oder dem Makro " [**capdlgvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ") anzeigen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-118">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro).</span></span>

<span data-ttu-id="b6cf8-119">Im Dialogfeld Videoanzeige wird die Darstellung des Videos auf dem Monitor während der Erfassung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-119">The Video Display dialog box controls the appearance of the video on the monitor during capture.</span></span> <span data-ttu-id="b6cf8-120">Die Steuerelemente in diesem Dialogfeld wirken sich nicht auf die digitalisierten Videodaten aus, Sie können sich jedoch auf die Darstellung des digitalisierten Signals auswirken.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-120">The controls in this dialog box have no effect on the digitized video data, but they might affect the presentation of the digitized signal.</span></span> <span data-ttu-id="b6cf8-121">Beispielsweise können Erfassungsgeräte, die Overlay unterstützen, das Ändern von Farbton, Sättigung, Schlüsselfarbe oder Ausrichtung der Überlagerung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-121">For example, capture devices that support overlay might allow altering hue and saturation, key color, or alignment of the overlay.</span></span> <span data-ttu-id="b6cf8-122">Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mithilfe der WM- [**\_ Cap- \_ DLG- \_ Videodisplay**](wm-cap-dlg-videodisplay.md) -Nachricht (oder des " [**capdlgvideodisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) "-Makros) anzeigen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-122">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (or the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro).</span></span>

<span data-ttu-id="b6cf8-123">Im Dialogfeld Video Komprimierung werden die Attribute für die Video Komprimierung nach der Erfassung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-123">The Video Compression dialog box controls the post-capture video compression attributes.</span></span> <span data-ttu-id="b6cf8-124">Wenn das Dialogfeld von einem Video Erfassungs Treiber unterstützt wird, können Sie es mithilfe der WM- [**\_ Cap- \_ DLG- \_ Video Komprimierungs**](wm-cap-dlg-videocompression.md) Nachricht (oder mit dem [**capdlgvideocompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) -Makro) anzeigen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b6cf8-124">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (or the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro).</span></span>

 

 




