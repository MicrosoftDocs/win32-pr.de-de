---
title: Video Aufzeichnungs Referenz
description: Video Aufzeichnungs Referenz
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Video für Windows (Vfw), Video Aufzeichnungs Referenz
- VFW (Video für Windows), Video Aufzeichnungs Referenz
- Avicap, Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036560"
---
# <a name="video-capture-reference"></a><span data-ttu-id="3e209-106">Video Aufzeichnungs Referenz</span><span class="sxs-lookup"><span data-stu-id="3e209-106">Video Capture Reference</span></span>

<span data-ttu-id="3e209-107">In diesem Abschnitt werden die Funktionen, Strukturen, Meldungen und Makros beschrieben, die der avicap-Fenster Klasse zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3e209-107">This section describes the functions, structures, messages, and macros associated with the AVICap window class.</span></span> <span data-ttu-id="3e209-108">Diese Elemente werden wie folgt gruppiert.</span><span class="sxs-lookup"><span data-stu-id="3e209-108">These elements are grouped as follows.</span></span>

## <a name="basic-capture-operations"></a><span data-ttu-id="3e209-109">Grundlegende Erfassungs Vorgänge</span><span class="sxs-lookup"><span data-stu-id="3e209-109">Basic Capture Operations</span></span>

-   [<span data-ttu-id="3e209-110">**capkreatecapturewindow**</span><span class="sxs-lookup"><span data-stu-id="3e209-110">**capCreateCaptureWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [<span data-ttu-id="3e209-111">**Abbruch der WM- \_ Obergrenze \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-111">**WM\_CAP\_ABORT**</span></span>](wm-cap-abort.md)
-   [<span data-ttu-id="3e209-112">**WM- \_ Cap- \_ Treiber \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="3e209-112">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="3e209-113">**WM- \_ Cap- \_ Sequenz**</span><span class="sxs-lookup"><span data-stu-id="3e209-113">**WM\_CAP\_SEQUENCE**</span></span>](wm-cap-sequence.md)
-   [<span data-ttu-id="3e209-114">**WM- \_ Cap- \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="3e209-114">**WM\_CAP\_STOP**</span></span>](wm-cap-stop.md)

## <a name="capture-windows"></a><span data-ttu-id="3e209-115">Erfassungsfenster</span><span class="sxs-lookup"><span data-stu-id="3e209-115">Capture Windows</span></span>

-   [<span data-ttu-id="3e209-116">**Capstatus**</span><span class="sxs-lookup"><span data-stu-id="3e209-116">**CAPSTATUS**</span></span>](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [<span data-ttu-id="3e209-117">**capgetdriverdescription**</span><span class="sxs-lookup"><span data-stu-id="3e209-117">**capGetDriverDescription**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [<span data-ttu-id="3e209-118">**WM- \_ Cap- \_ Treiber \_ Verbindung**</span><span class="sxs-lookup"><span data-stu-id="3e209-118">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="3e209-119">**WM- \_ Cap- \_ Treiber Verbindung \_ trennen**</span><span class="sxs-lookup"><span data-stu-id="3e209-119">**WM\_CAP\_DRIVER\_DISCONNECT**</span></span>](wm-cap-driver-disconnect.md)
-   [<span data-ttu-id="3e209-120">**WM- \_ Cap- \_ \_ Status Get**</span><span class="sxs-lookup"><span data-stu-id="3e209-120">**WM\_CAP\_GET\_STATUS**</span></span>](wm-cap-get-status.md)

## <a name="capture-drivers"></a><span data-ttu-id="3e209-121">Erfassungs Treiber</span><span class="sxs-lookup"><span data-stu-id="3e209-121">Capture Drivers</span></span>

-   [<span data-ttu-id="3e209-122">**Capdrivercaps**</span><span class="sxs-lookup"><span data-stu-id="3e209-122">**CAPDRIVERCAPS**</span></span>](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [<span data-ttu-id="3e209-123">**WM- \_ Cap- \_ Treiber \_ get \_ Caps**</span><span class="sxs-lookup"><span data-stu-id="3e209-123">**WM\_CAP\_DRIVER\_GET\_CAPS**</span></span>](wm-cap-driver-get-caps.md)
-   [<span data-ttu-id="3e209-124">**WM- \_ Cap- \_ Treiber get- \_ \_ Name**</span><span class="sxs-lookup"><span data-stu-id="3e209-124">**WM\_CAP\_DRIVER\_GET\_NAME**</span></span>](wm-cap-driver-get-name.md)
-   [<span data-ttu-id="3e209-125">**WM- \_ Cap- \_ Treiber get- \_ \_ Version**</span><span class="sxs-lookup"><span data-stu-id="3e209-125">**WM\_CAP\_DRIVER\_GET\_VERSION**</span></span>](wm-cap-driver-get-version.md)
-   [<span data-ttu-id="3e209-126">**WM- \_ Cap \_ get \_ Audioformat**</span><span class="sxs-lookup"><span data-stu-id="3e209-126">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="3e209-127">**WM- \_ Cap \_ get \_ Videoformat**</span><span class="sxs-lookup"><span data-stu-id="3e209-127">**WM\_CAP\_GET\_VIDEOFORMAT**</span></span>](wm-cap-get-videoformat.md)
-   [<span data-ttu-id="3e209-128">**WM- \_ Cap- \_ Set \_ Audioformat**</span><span class="sxs-lookup"><span data-stu-id="3e209-128">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)
-   [<span data-ttu-id="3e209-129">**WM- \_ Cap- \_ Set- \_ Videoformat**</span><span class="sxs-lookup"><span data-stu-id="3e209-129">**WM\_CAP\_SET\_VIDEOFORMAT**</span></span>](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a><span data-ttu-id="3e209-130">Erfassungs Modus für Erfassungs Treiber</span><span class="sxs-lookup"><span data-stu-id="3e209-130">Capture Driver Preview and Overlay Modes</span></span>

-   [<span data-ttu-id="3e209-131">**Überlagerung der WM- \_ Obergrenze \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-131">**WM\_CAP\_SET\_OVERLAY**</span></span>](wm-cap-set-overlay.md)
-   [<span data-ttu-id="3e209-132">**WM- \_ Cap- \_ \_ Vorschau festlegen**</span><span class="sxs-lookup"><span data-stu-id="3e209-132">**WM\_CAP\_SET\_PREVIEW**</span></span>](wm-cap-set-preview.md)
-   [<span data-ttu-id="3e209-133">**\_previewrate der WM-Obergrenze \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-133">**WM\_CAP\_SET\_PREVIEWRATE**</span></span>](wm-cap-set-previewrate.md)
-   [<span data-ttu-id="3e209-134">**WM- \_ Cap- \_ Set- \_ Skala**</span><span class="sxs-lookup"><span data-stu-id="3e209-134">**WM\_CAP\_SET\_SCALE**</span></span>](wm-cap-set-scale.md)
-   [<span data-ttu-id="3e209-135">**Bild Lauf der WM- \_ Obergrenze \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-135">**WM\_CAP\_SET\_SCROLL**</span></span>](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a><span data-ttu-id="3e209-136">Dialog Felder für das Erfassen von Treibern</span><span class="sxs-lookup"><span data-stu-id="3e209-136">Capture Driver Video Dialog Boxes</span></span>

-   [<span data-ttu-id="3e209-137">**WM \_ Cap \_ DLG- \_ Video Komprimierung**</span><span class="sxs-lookup"><span data-stu-id="3e209-137">**WM\_CAP\_DLG\_VIDEOCOMPRESSION**</span></span>](wm-cap-dlg-videocompression.md)
-   [<span data-ttu-id="3e209-138">**WM- \_ Cap- \_ DLG- \_ Videodisplay**</span><span class="sxs-lookup"><span data-stu-id="3e209-138">**WM\_CAP\_DLG\_VIDEODISPLAY**</span></span>](wm-cap-dlg-videodisplay.md)
-   [<span data-ttu-id="3e209-139">**WM \_ Cap \_ DLG- \_ Videoformat**</span><span class="sxs-lookup"><span data-stu-id="3e209-139">**WM\_CAP\_DLG\_VIDEOFORMAT**</span></span>](wm-cap-dlg-videoformat.md)
-   [<span data-ttu-id="3e209-140">**WM \_ Cap \_ DLG- \_ videosource**</span><span class="sxs-lookup"><span data-stu-id="3e209-140">**WM\_CAP\_DLG\_VIDEOSOURCE**</span></span>](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a><span data-ttu-id="3e209-141">Audioformat</span><span class="sxs-lookup"><span data-stu-id="3e209-141">Audio Format</span></span>

-   [<span data-ttu-id="3e209-142">**WM- \_ Cap \_ get \_ Audioformat**</span><span class="sxs-lookup"><span data-stu-id="3e209-142">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="3e209-143">**WM- \_ Cap- \_ Set \_ Audioformat**</span><span class="sxs-lookup"><span data-stu-id="3e209-143">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a><span data-ttu-id="3e209-144">Video Erfassungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="3e209-144">Video Capture Settings</span></span>

-   [<span data-ttu-id="3e209-145">**Captureparms**</span><span class="sxs-lookup"><span data-stu-id="3e209-145">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="3e209-146">**WM- \_ Cap- \_ \_ Setup Get Sequence \_ Setup**</span><span class="sxs-lookup"><span data-stu-id="3e209-146">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="3e209-147">**Setup für die WM- \_ Cap- \_ Einrichtung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-147">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a><span data-ttu-id="3e209-148">Erfassungs Datei und Puffer</span><span class="sxs-lookup"><span data-stu-id="3e209-148">Capture File and Buffers</span></span>

-   [<span data-ttu-id="3e209-149">**Captureparms**</span><span class="sxs-lookup"><span data-stu-id="3e209-149">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="3e209-150">**WM- \_ Cap- \_ Datei \_ zuordnen**</span><span class="sxs-lookup"><span data-stu-id="3e209-150">**WM\_CAP\_FILE\_ALLOCATE**</span></span>](wm-cap-file-allocate.md)
-   [<span data-ttu-id="3e209-151">**WM- \_ Cap- \_ Datei get- \_ \_ Erfassungs \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="3e209-151">**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**</span></span>](wm-cap-file-get-capture-file.md)
-   [<span data-ttu-id="3e209-152">**WM- \_ Cap- \_ Datei ( \_ SaveAs)**</span><span class="sxs-lookup"><span data-stu-id="3e209-152">**WM\_CAP\_FILE\_SAVEAS**</span></span>](wm-cap-file-saveas.md)
-   [<span data-ttu-id="3e209-153">**\_ \_ Datei Satz- \_ \_ Erfassungs \_ Datei für WM-Cap**</span><span class="sxs-lookup"><span data-stu-id="3e209-153">**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**</span></span>](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a><span data-ttu-id="3e209-154">Direkte Verwendung von Erfassungsdaten</span><span class="sxs-lookup"><span data-stu-id="3e209-154">Directly Using Capture Data</span></span>

-   [<span data-ttu-id="3e209-155">**WM- \_ Abdeckungs \_ Sequenz- \_ NoFile**</span><span class="sxs-lookup"><span data-stu-id="3e209-155">**WM\_CAP\_SEQUENCE\_NOFILE**</span></span>](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a><span data-ttu-id="3e209-156">Erfassung vom MCI-Gerät</span><span class="sxs-lookup"><span data-stu-id="3e209-156">Capture from MCI Device</span></span>

-   [<span data-ttu-id="3e209-157">**WM- \_ Cap- \_ festgelegte \_ MCI- \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="3e209-157">**WM\_CAP\_SET\_MCI\_DEVICE**</span></span>](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a><span data-ttu-id="3e209-158">Manuelle Frame Erfassung</span><span class="sxs-lookup"><span data-stu-id="3e209-158">Manual Frame Capture</span></span>

-   [<span data-ttu-id="3e209-159">**WM- \_ Cap- \_ Einzel \_ Rahmen**</span><span class="sxs-lookup"><span data-stu-id="3e209-159">**WM\_CAP\_SINGLE\_FRAME**</span></span>](wm-cap-single-frame.md)
-   [<span data-ttu-id="3e209-160">**WM- \_ Cap- \_ Einzel \_ Rahmen \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="3e209-160">**WM\_CAP\_SINGLE\_FRAME\_CLOSE**</span></span>](wm-cap-single-frame-close.md)
-   [<span data-ttu-id="3e209-161">**WM- \_ Cap- \_ Einzel \_ Rahmen \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="3e209-161">**WM\_CAP\_SINGLE\_FRAME\_OPEN**</span></span>](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a><span data-ttu-id="3e209-162">Still-Image Erfassung</span><span class="sxs-lookup"><span data-stu-id="3e209-162">Still-Image Capture</span></span>

-   [<span data-ttu-id="3e209-163">**\_ \_ Bearbeitungs \_ Kopie der WM-Abdeckung**</span><span class="sxs-lookup"><span data-stu-id="3e209-163">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="3e209-164">**WM- \_ Cap- \_ Datei ( \_ savedib)**</span><span class="sxs-lookup"><span data-stu-id="3e209-164">**WM\_CAP\_FILE\_SAVEDIB**</span></span>](wm-cap-file-savedib.md)
-   [<span data-ttu-id="3e209-165">**WM- \_ Abdeckungs \_ \_ Rahmen**</span><span class="sxs-lookup"><span data-stu-id="3e209-165">**WM\_CAP\_GRAB\_FRAME**</span></span>](wm-cap-grab-frame.md)
-   [<span data-ttu-id="3e209-166">**WM- \_ Obergrenze für Abdeckungs \_ \_ Rahmen \_ nostopps**</span><span class="sxs-lookup"><span data-stu-id="3e209-166">**WM\_CAP\_GRAB\_FRAME\_NOSTOP**</span></span>](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a><span data-ttu-id="3e209-167">Erweiterte Aufzeichnungs Optionen</span><span class="sxs-lookup"><span data-stu-id="3e209-167">Advanced Capture Options</span></span>

-   [<span data-ttu-id="3e209-168">**WM- \_ Cap- \_ Datei \_ Satz \_ Infoblock**</span><span class="sxs-lookup"><span data-stu-id="3e209-168">**WM\_CAP\_FILE\_SET\_INFOCHUNK**</span></span>](wm-cap-file-set-infochunk.md)
-   [<span data-ttu-id="3e209-169">**WM- \_ Cap- \_ \_ Benutzer \_ Daten erhalten**</span><span class="sxs-lookup"><span data-stu-id="3e209-169">**WM\_CAP\_GET\_USER\_DATA**</span></span>](wm-cap-get-user-data.md)
-   [<span data-ttu-id="3e209-170">**WM- \_ Cap- \_ \_ Benutzer \_ Daten festlegen**</span><span class="sxs-lookup"><span data-stu-id="3e209-170">**WM\_CAP\_SET\_USER\_DATA**</span></span>](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a><span data-ttu-id="3e209-171">Arbeiten mit Paletten</span><span class="sxs-lookup"><span data-stu-id="3e209-171">Working with Palettes</span></span>

-   [<span data-ttu-id="3e209-172">**\_ \_ Bearbeitungs \_ Kopie der WM-Abdeckung**</span><span class="sxs-lookup"><span data-stu-id="3e209-172">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="3e209-173">**WM \_ Cap \_ PAL \_ AutoCreate**</span><span class="sxs-lookup"><span data-stu-id="3e209-173">**WM\_CAP\_PAL\_AUTOCREATE**</span></span>](wm-cap-pal-autocreate.md)
-   [<span data-ttu-id="3e209-174">**WM \_ Cap \_ PAL \_ manualcreate**</span><span class="sxs-lookup"><span data-stu-id="3e209-174">**WM\_CAP\_PAL\_MANUALCREATE**</span></span>](wm-cap-pal-manualcreate.md)
-   [<span data-ttu-id="3e209-175">**WM- \_ Cap- \_ PAL \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="3e209-175">**WM\_CAP\_PAL\_OPEN**</span></span>](wm-cap-pal-open.md)
-   [<span data-ttu-id="3e209-176">**WM- \_ Cap- \_ PAL \_ Einfügen**</span><span class="sxs-lookup"><span data-stu-id="3e209-176">**WM\_CAP\_PAL\_PASTE**</span></span>](wm-cap-pal-paste.md)
-   [<span data-ttu-id="3e209-177">**WM- \_ Cap- \_ PAL \_ Speichern**</span><span class="sxs-lookup"><span data-stu-id="3e209-177">**WM\_CAP\_PAL\_SAVE**</span></span>](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a><span data-ttu-id="3e209-178">Bereitzustellen an andere Anwendungen</span><span class="sxs-lookup"><span data-stu-id="3e209-178">Yielding to Other Applications</span></span>

-   [<span data-ttu-id="3e209-179">**WM- \_ Cap- \_ \_ Setup Get Sequence \_ Setup**</span><span class="sxs-lookup"><span data-stu-id="3e209-179">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="3e209-180">**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**</span><span class="sxs-lookup"><span data-stu-id="3e209-180">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="3e209-181">**Setup für die WM- \_ Cap- \_ Einrichtung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-181">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a><span data-ttu-id="3e209-182">Avicap-Rückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="3e209-182">AVICap Callback Functions</span></span>

-   [<span data-ttu-id="3e209-183">**capcontrolcallback**</span><span class="sxs-lookup"><span data-stu-id="3e209-183">**capControlCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [<span data-ttu-id="3e209-184">**caperrorcallback**</span><span class="sxs-lookup"><span data-stu-id="3e209-184">**capErrorCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [<span data-ttu-id="3e209-185">**capstatus-Rückruf**</span><span class="sxs-lookup"><span data-stu-id="3e209-185">**capStatusCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [<span data-ttu-id="3e209-186">**capvideostreamcallback**</span><span class="sxs-lookup"><span data-stu-id="3e209-186">**capVideoStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [<span data-ttu-id="3e209-187">**capwavestreamcallback**</span><span class="sxs-lookup"><span data-stu-id="3e209-187">**capWaveStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [<span data-ttu-id="3e209-188">**capyieldcallback**</span><span class="sxs-lookup"><span data-stu-id="3e209-188">**capYieldCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [<span data-ttu-id="3e209-189">**WM- \_ Cap- \_ Satz Rückruf ( \_ \_ capcontrol)**</span><span class="sxs-lookup"><span data-stu-id="3e209-189">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)
-   [<span data-ttu-id="3e209-190">**Rückruf Fehler bei WM-Abdeckung \_ \_ festgelegt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-190">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="3e209-191">**\_ \_ \_ Rückruf \_ Rahmen für WM-Cap-Satz**</span><span class="sxs-lookup"><span data-stu-id="3e209-191">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)
-   [<span data-ttu-id="3e209-192">**Rückruf Status der WM- \_ Obergrenze \_ festlegen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e209-192">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="3e209-193">**WM- \_ Abdeckungs \_ Satz \_ Rückruf \_ Videostream**</span><span class="sxs-lookup"><span data-stu-id="3e209-193">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="3e209-194">**WM- \_ Cap- \_ Satz \_ Rückruf \_ WaveStream**</span><span class="sxs-lookup"><span data-stu-id="3e209-194">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)
-   [<span data-ttu-id="3e209-195">**\_ \_ \_ Rückruf \_ Rendite für WM-Cap-Satz**</span><span class="sxs-lookup"><span data-stu-id="3e209-195">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a><span data-ttu-id="3e209-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e209-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e209-197">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="3e209-197">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




