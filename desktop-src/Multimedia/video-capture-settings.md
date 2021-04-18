---
title: Video Erfassungs Einstellungen
description: Video Erfassungs Einstellungen
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Captuprojektms-Struktur
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341637"
---
# <a name="video-capture-settings"></a><span data-ttu-id="9146f-108">Video Erfassungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9146f-108">Video Capture Settings</span></span>

<span data-ttu-id="9146f-109">Die [**captureparms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur enthält die Steuerelement Parameter für das Streaming von Videoaufnahmen.</span><span class="sxs-lookup"><span data-stu-id="9146f-109">The [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure contains the control parameters for streaming video capture.</span></span> <span data-ttu-id="9146f-110">Diese Struktur steuert verschiedene Aspekte des Aufzeichnungsprozesses und ermöglicht Ihnen die Durchführung der folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="9146f-110">This structure controls several aspects of the capture process, and allows you to perform the following tasks:</span></span>

-   <span data-ttu-id="9146f-111">Geben Sie die Frame Rate an.</span><span class="sxs-lookup"><span data-stu-id="9146f-111">Specify the frame rate.</span></span>
-   <span data-ttu-id="9146f-112">Geben Sie die Anzahl der zugeordneten Video Puffer an.</span><span class="sxs-lookup"><span data-stu-id="9146f-112">Specify the number of allocated video buffers.</span></span>
-   <span data-ttu-id="9146f-113">Deaktivieren und aktivieren Sie die Audioerfassung.</span><span class="sxs-lookup"><span data-stu-id="9146f-113">Disable and enable audio capture.</span></span>
-   <span data-ttu-id="9146f-114">Geben Sie das Zeitintervall für die Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="9146f-114">Specify the time interval for the capture.</span></span>
-   <span data-ttu-id="9146f-115">Geben Sie an, ob während der Erfassung ein MCI-Gerät (VCR oder Videodisk) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9146f-115">Specify whether an MCI device (VCR or videodisc) is used during capture.</span></span>
-   <span data-ttu-id="9146f-116">Tastatur-oder Maussteuerung zum Beenden des Streamings angeben.</span><span class="sxs-lookup"><span data-stu-id="9146f-116">Specify keyboard or mouse control for ending streaming.</span></span>
-   <span data-ttu-id="9146f-117">Geben Sie den Typ des Videos an, das während der Erfassung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9146f-117">Specify the type of video averaging applied during capture.</span></span>

<span data-ttu-id="9146f-118">Sie können die aktuellen Aufzeichnungs Einstellungen innerhalb der [**captuprojektms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur abrufen, indem Sie die [**\_ gatewaycap- \_ Setup Nachricht get \_ Sequence \_**](wm-cap-get-sequence-setup.md) (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) an ein Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="9146f-118">You can retrieve the current capture settings within the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure by sending the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro) to a capture window.</span></span> <span data-ttu-id="9146f-119">Sie können eine oder mehrere aktuelle Aufzeichnungs Einstellungen festlegen, indem Sie die entsprechenden Member der **captuprojektstruktur** -Struktur aktualisieren und dann [**die \_ \_ \_ \_ Setup**](wm-cap-set-sequence-setup.md) Nachricht für die WM-Cap-Einrichtung (oder das " [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) "-Makro) und **captuprojektmappenelemente** an ein Aufzeichnungs Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="9146f-119">You can set one or more current capture settings by updating the appropriate members of the **CAPTUREPARMS** structure and then sending the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro) and **CAPTUREPARMS** to a capture window.</span></span>

 

 




