---
title: Still-Image Erfassung
description: Still-Image Erfassung
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP Meldung
- WM_CAP_GRAB_FRAME Meldung
- capgrabframenostop-Makro
- capgrabframe-Makro
- WM_CAP_EDIT_COPY Meldung
- capeditcopy-Makro
- WM_CAP_FILE_SAVEDIB Meldung
- capfilesavedib-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100670"
---
# <a name="still-image-capture"></a><span data-ttu-id="e7223-111">Still-Image Erfassung</span><span class="sxs-lookup"><span data-stu-id="e7223-111">Still-Image Capture</span></span>

<span data-ttu-id="e7223-112">Wenn Sie einen einzelnen Frame als noch Bild erfassen möchten, können Sie die Sende [**\_ \_ \_ Rahmen**](wm-cap-grab-frame.md) Nachricht "WM-Abdeckung zum Abrufen von [**\_ \_ \_ Rahmen \_**](wm-cap-grab-frame-nostop.md) " oder "WM-Abdeckung" (oder das Makro " [**capgrabframenostop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) " oder " [**capgrabframe**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) ") verwenden, um das digitalisierte Bild in einem internen Frame Puffer zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="e7223-112">If you want to capture a single frame as a still image, you can use the [**WM\_CAP\_GRAB\_FRAME\_NOSTOP**](wm-cap-grab-frame-nostop.md) or [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message (or the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) or [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro) to capture the digitized image in an internal frame buffer.</span></span> <span data-ttu-id="e7223-113">Sie können die Anzeige für das erfasste Abbild mithilfe des WM- \_ Abdeckungs \_ \_ Rahmens fixieren.</span><span class="sxs-lookup"><span data-stu-id="e7223-113">You can freeze the display on the captured image by using WM\_CAP\_GRAB\_FRAME.</span></span> <span data-ttu-id="e7223-114">Verwenden Sie andernfalls den WM- \_ Abdeckungs \_ \_ Rahmen \_ nostoppt.</span><span class="sxs-lookup"><span data-stu-id="e7223-114">Otherwise, use WM\_CAP\_GRAB\_FRAME\_NOSTOP.</span></span>

<span data-ttu-id="e7223-115">Nach der Erfassung können Sie das Abbild für die Verwendung durch andere Anwendungen kopieren.</span><span class="sxs-lookup"><span data-stu-id="e7223-115">Once captured, you can copy the image for use by other applications.</span></span> <span data-ttu-id="e7223-116">Sie können ein Bild aus dem Frame Puffer in die Zwischenablage kopieren, indem Sie die Meldung zum [**\_ \_ Bearbeiten \_ der WM**](wm-cap-edit-copy.md) -Abdeckung (oder das [**capeditcopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) -Makro) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7223-116">You can copy an image from the frame buffer to the clipboard by using the [**WM\_CAP\_EDIT\_COPY**](wm-cap-edit-copy.md) message (or the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro).</span></span> <span data-ttu-id="e7223-117">Sie können das Bild auch aus dem Frame Puffer in eine geräteunabhängige Bitmap (DIB) kopieren, indem Sie die [**\_ Datei " \_ \_ savedib**](wm-cap-file-savedib.md) " der WM-Cap-Datei (oder das Makro [**capfilesavedib**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7223-117">You can also copy the image from the frame buffer to a device-independent bitmap (DIB) by using the [**WM\_CAP\_FILE\_SAVEDIB**](wm-cap-file-savedib.md) message (or the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro).</span></span>

<span data-ttu-id="e7223-118">Die Anwendung kann auch die zwei einzelnen Frame Erfassungs Nachrichten verwenden, um einen Sequenz Rahmen nach Frame zu bearbeiten oder um eine Zeitverlaufs-Fotosequenz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e7223-118">Your application can also use the two single-frame capture messages to edit a sequence frame by frame, or to create a time-lapse photography sequence.</span></span>

 

 




