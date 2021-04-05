---
title: Vorschau-und Überlagerungs Modi
description: Vorschau-und Überlagerungs Modi
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW Meldung
- cappreview-Makro
- WM_CAP_SET_PREVIEWRATE Meldung
- cappreviewrate-Makro
- WM_CAP_SET_SCALE Meldung
- cappreviewscale-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947603"
---
# <a name="preview-and-overlay-modes"></a><span data-ttu-id="4af16-109">Vorschau-und Überlagerungs Modi</span><span class="sxs-lookup"><span data-stu-id="4af16-109">Preview and Overlay Modes</span></span>

<span data-ttu-id="4af16-110">Ein Erfassungs Treiber kann zwei Methoden zum Anzeigen eines eingehenden Videodaten Stroms implementieren: Vorschaumodus und Überlagerungs Modus.</span><span class="sxs-lookup"><span data-stu-id="4af16-110">A capture driver can implement two methods for viewing an incoming video stream: preview mode and overlay mode.</span></span> <span data-ttu-id="4af16-111">Wenn ein Aufzeichnungs Treiber beide Methoden implementiert, kann der Benutzer auswählen, welche Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4af16-111">If a capture driver implements both methods, the user can choose which method to use.</span></span>

<span data-ttu-id="4af16-112">Der Vorschaumodus überträgt digitalisierte Frames von der Aufzeichnungs Hardware in den Systemspeicher und zeigt dann die digitalisierten Frames im Erfassungsfenster mithilfe von Funktionen der Graphics Device Interface (GDI) an.</span><span class="sxs-lookup"><span data-stu-id="4af16-112">Preview mode transfers digitized frames from the capture hardware to system memory and then displays the digitized frames in the capture window by using graphics device interface (GDI) functions.</span></span> <span data-ttu-id="4af16-113">Anwendungen können die Vorschau Rate verringern, wenn das übergeordnete Fenster den Fokus verliert, und die Vorschau Rate erhöhen, wenn das übergeordnete Fenster den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="4af16-113">Applications might decrease the preview rate when the parent window loses focus, and increase the preview rate when the parent window gains focus.</span></span> <span data-ttu-id="4af16-114">Durch diese Aktion wird die allgemeine Reaktionsfähigkeit des Systems verbessert, da der Vorschau Vorgang Prozessor intensiv ist.</span><span class="sxs-lookup"><span data-stu-id="4af16-114">This action improves general system responsiveness because the preview operation is processor intensive.</span></span>

<span data-ttu-id="4af16-115">Es gibt drei Nachrichten, um den Vorschauvorgang zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4af16-115">There are three messages to control the preview operation.</span></span>

-   <span data-ttu-id="4af16-116">Verwenden Sie die Vorschau Nachricht der [**WM- \_ Ober \_ \_ Grenze**](wm-cap-set-preview.md) , um den Vorschaumodus zu aktivieren oder zu deaktivieren, indem Sie das-(oder das [**cappreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) -Makro) an ein Aufzeichnungs Fenster senden</span><span class="sxs-lookup"><span data-stu-id="4af16-116">Use the [**WM\_CAP\_SET\_PREVIEW**](wm-cap-set-preview.md) message to enable or disable preview mode by sending the (or the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro) to a capture window.</span></span>
-   <span data-ttu-id="4af16-117">Verwenden Sie die " [**WM \_ Cap \_ Set \_ previewrate**](wm-cap-set-previewrate.md) "-Meldung (oder das " [**cappreviewrate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) "-Makro), um die Rate festzulegen, mit der Frames im Vorschaumodus angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="4af16-117">Use the [**WM\_CAP\_SET\_PREVIEWRATE**](wm-cap-set-previewrate.md) message (or the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro) to set the rate at which frames are displayed in preview mode</span></span>
-   <span data-ttu-id="4af16-118">Verwenden Sie die " [**WM \_ Cap \_ Set \_ Scale**](wm-cap-set-scale.md) "-Nachricht (oder das [**cappreviewscale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) -Makro), um die Skalierung des Vorschau Videos zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4af16-118">Use the [**WM\_CAP\_SET\_SCALE**](wm-cap-set-scale.md) message (or the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro) to enable or disable scaling of the preview video.</span></span>

<span data-ttu-id="4af16-119">Wenn Vorschau und Skalierung aktiviert sind, wird der erfasste Videoframe auf die Abmessungen des Aufzeichnungs Fensters gestreckt.</span><span class="sxs-lookup"><span data-stu-id="4af16-119">When preview and scaling are both enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="4af16-120">Durch Aktivieren des Vorschaumodus wird der Überlagerungs Modus automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4af16-120">Enabling preview mode automatically disables overlay mode.</span></span>

<span data-ttu-id="4af16-121">Der Überlagerungs Modus ist eine Hardware Funktion, die den Inhalt des Aufzeichnungs Puffers auf dem Monitor anzeigt, ohne CPU-Ressourcen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4af16-121">Overlay mode is a hardware function that displays the contents of the capture buffer on the monitor without using CPU resources.</span></span> <span data-ttu-id="4af16-122">Sie können den Überlagerungs Modus aktivieren und deaktivieren, indem Sie die WM-Cap-über [**\_ \_ \_ Lagerungs**](wm-cap-set-overlay.md) Nachricht (oder das [**capoverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) -Makro) an ein Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="4af16-122">You can enable and disable overlay mode by sending the [**WM\_CAP\_SET\_OVERLAY**](wm-cap-set-overlay.md) message (or the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro) to a capture window.</span></span> <span data-ttu-id="4af16-123">Durch Aktivieren des Überlagerungs Modus wird der Vorschaumodus automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4af16-123">Enabling overlay mode automatically disables preview mode.</span></span>

<span data-ttu-id="4af16-124">Sie können auch die Bild Lauf Position des Video Rahmens im Client Bereich des Aufzeichnungs Fensters für den Vorschaumodus oder den Überlagerungs Modus festlegen, indem Sie die WM-Cap-Abbild [**\_ \_ \_ scrollnachricht**](wm-cap-set-scroll.md) (oder das [**capsetscrollpos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) -Makro) an ein Erfassungsfenster senden.</span><span class="sxs-lookup"><span data-stu-id="4af16-124">You can also set the scroll position of the video frame within the client area of the capture window for preview mode or overlay mode by sending the [**WM\_CAP\_SET\_SCROLL**](wm-cap-set-scroll.md) message (or the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro) to a capture window.</span></span>

 

 




