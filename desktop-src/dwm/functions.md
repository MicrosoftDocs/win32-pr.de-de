---
title: DWM-Funktionen
description: Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Funktionen.
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Desktopfenster-Manager (DWM), Referenz
- Dwm (Desktopfenster-Manager), Referenz
- Desktopfenster-Manager (DWM), Funktionen
- Dwm (Desktopfenster-Manager), Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316604"
---
# <a name="dwm-functions"></a><span data-ttu-id="a13cc-107">DWM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a13cc-107">DWM Functions</span></span>

<span data-ttu-id="a13cc-108">Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a13cc-108">This section contains information about the Desktop Window Manager (DWM) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a13cc-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a13cc-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a13cc-110">Thema</span><span class="sxs-lookup"><span data-stu-id="a13cc-110">Topic</span></span></th>
<th><span data-ttu-id="a13cc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a13cc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a13cc-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>Dwmattachmilcontent</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-113">Diese Funktion ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a13cc-113">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-115">Standardfenster Prozedur für den DWM-Treffer Test innerhalb des nicht-Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a13cc-115">Default window procedure for DWM hit testing within the non-client area.</span></span><br/> <span data-ttu-id="a13cc-116">Außerdem müssen Sie sicherstellen, dass <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> für die <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> Nachricht aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a13cc-116">You also need to ensure that <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> message.</span></span> <span data-ttu-id="a13cc-117">Wenn <strong>DwmDefWindowProc</strong> nicht für die <strong>WM_NCMOUSELEAVE</strong> Nachricht aufgerufen wird, entfernt DWM die Hervorhebung nicht aus den Schaltflächen <strong>maximieren</strong>, <strong>minimieren</strong>und <strong>Schließen</strong> , wenn der Cursor das Fenster verlässt.</span><span class="sxs-lookup"><span data-stu-id="a13cc-117">If <strong>DwmDefWindowProc</strong> is not called for the <strong>WM_NCMOUSELEAVE</strong> message, DWM does not remove the highlighting from the <strong>Maximize</strong>, <strong>Minimize</strong>, and <strong>Close</strong> buttons when the cursor leaves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>Dwmdetachmilcontent</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-119">Diese Funktion ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a13cc-119">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>Dwmenableblurabledwindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-121">Aktiviert den Weichzeichnereffekt in einem angegebenen Fenster.</span><span class="sxs-lookup"><span data-stu-id="a13cc-121">Enables the blur effect on a specified window.</span></span><br/></td><span data-ttu-id="a13cc-122">
<b>Hinweis</b> Beginnend mit Windows 8 führt das Aufrufen dieser Funktion nicht zu einem Weichzeichnereffekt aufgrund einer Stiländerung in der Art und Weise, in der Fenster gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="a13cc-122">
<b>Note</b> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-124">Aktiviert oder deaktiviert die DWM-Komposition.</span><span class="sxs-lookup"><span data-stu-id="a13cc-124">Enables or disables DWM composition.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a13cc-125">Diese Funktion ist ab Windows 8 veraltet.</span><span class="sxs-lookup"><span data-stu-id="a13cc-125">This function is deprecated as of Windows 8.</span></span> <span data-ttu-id="a13cc-126">DWM kann nicht mehr Programm gesteuert deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a13cc-126">DWM can no longer be programmatically disabled.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>Dwmenablemmcss</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-128">Benachrichtigt den DWM, dass die MMCSS-Zeitplanung (Multimedia Class Schedule Service) deaktiviert wird, während der Aufrufprozess aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a13cc-128">Notifies the DWM to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-130">Erweitert den Fensterrahmen in den Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="a13cc-130">Extends the window frame into the client area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>Dwmflush</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-132">Gibt einen Flush-Aufruf aus, der den Aufrufer bis zum nächsten vorhanden ist, wenn alle aktuell ausstehenden Microsoft DirectX Surface-Aktualisierungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="a13cc-132">Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made.</span></span> <span data-ttu-id="a13cc-133">Dies kompensiert sehr komplexe Szenen oder Aufruf Prozesse mit sehr niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="a13cc-133">This compensates for very complex scenes or calling processes with very low priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-135">Ruft die für die DWM-Glaskomposition verwendete aktuelle Farbe ab.</span><span class="sxs-lookup"><span data-stu-id="a13cc-135">Retrieves the current color used for DWM glass composition.</span></span> <span data-ttu-id="a13cc-136">Dieser Wert basiert auf dem aktuellen Farbschema und kann vom Benutzer geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a13cc-136">This value is based on the current color scheme and can be modified by the user.</span></span> <span data-ttu-id="a13cc-137">Anwendungen können Farbänderungen überwachen, indem Sie die <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> Benachrichtigung verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a13cc-137">Applications can listen for color changes by handling the <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>Dwmgetcompositiontiminginfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-139">Ruft die aktuellen Informationen zur Kompositions Zeit für ein angegebenes Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="a13cc-139">Retrieves the current composition timing information for a specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>Dwmgetgraphicsstreamclient</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-141">Diese Funktion ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a13cc-141">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>Dwmgetgraphicsstreamtransformhint</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-143">Diese Funktion ist nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a13cc-143">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>Dwmgettransportattributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-145">Ruft Transport Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="a13cc-145">Retrieves transport attributes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>Dwmgetunmettabrequirements</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span></span><br/></td>
<td><blockquote><span data-ttu-id="a13cc-147">
<strong>Hinweis</strong>  Diese Funktion ist öffentlich verfügbar, aber nicht funktionsfähig für Windows 10, Version 1803.</span><span class="sxs-lookup"><span data-stu-id="a13cc-147">
<strong>Note</strong>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</span></span>
</blockquote>
<span data-ttu-id="a13cc-148">Überprüft die erforderlichen Anforderungen zum erhalten von Registerkarten in der Titelleiste der Anwendung für das angegebene Fenster.</span><span class="sxs-lookup"><span data-stu-id="a13cc-148">Checks the requirements needed to get tabs in the application title bar for the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-150">Ruft den aktuellen Wert eines angegebenen Attributs ab, das auf ein Fenster angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a13cc-150">Retrieves the current value of a specified attribute applied to a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>Dwminvalidateiconfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-152">Wird von einer Anwendung aufgerufen, um anzugeben, dass alle zuvor bereitgestellten ikonischen Bitmaps aus einem Fenster, sowohl Miniaturansichten als auch Peek-Darstellungen, aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a13cc-152">Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-154">Ruft einen Wert ab, der angibt, ob die DWM-Komposition aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a13cc-154">Obtains a value that indicates whether DWM composition is enabled.</span></span> <span data-ttu-id="a13cc-155">Anwendungen auf Computern, auf denen Windows 7 oder früher ausgeführt wird, können Änderungen am Kompositions Status überwachen, indem Sie die <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> Benachrichtigung verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a13cc-155">Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>Dwmmodifypreviousdxframeduration</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-157">Ändert die Anzahl von Monitor Aktualisierungen, über die der vorherige Frame angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a13cc-157">Changes the number of monitor refreshes through which the previous frame will be displayed.</span></span> <br/> <span data-ttu-id="a13cc-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>Dwmmodifypreviousdxframeduration</strong></a> wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a13cc-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="a13cc-159">Beginnend mit Windows 8.1 geben Aufrufe von <strong>dwmmodifypreviousdxframeduration</strong> immer E_NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="a13cc-159">Starting with Windows 8.1, calls to <strong>DwmModifyPreviousDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-161">Ruft die Quellgröße der DWM-Miniaturansicht ab.</span><span class="sxs-lookup"><span data-stu-id="a13cc-161">Retrieves the source size of the DWM thumbnail.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>Dwmregisterminiatur</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-163">Erstellt eine DWM-Miniatur Ansichts Beziehung zwischen den Ziel-und Quell Fenstern.</span><span class="sxs-lookup"><span data-stu-id="a13cc-163">Creates a DWM thumbnail relationship between the destination and source windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>Dwmrendergeste</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-165">Benachrichtigt dwm, dass ein touchkontakt als Geste erkannt wurde und dass DWM Feedback für diese Geste zeichnen sollte.</span><span class="sxs-lookup"><span data-stu-id="a13cc-165">Notifies DWM that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>Dwmsetdxframeduration</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-167">Legt die Anzahl von Monitor Aktualisierungen fest, mit denen der dargestellte Frame angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a13cc-167">Sets the number of monitor refreshes through which to display the presented frame.</span></span> <br/> <span data-ttu-id="a13cc-168">" <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>Dwmsetdxframeduration</strong></a> " wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a13cc-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="a13cc-169">Beginnend mit Windows 8.1 geben Aufrufe von <strong>dwmsetdxframeduration</strong> immer E_NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="a13cc-169">Starting with Windows 8.1, calls to <strong>DwmSetDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>Dwmabticoniclivepreviewbitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-171">Legt eine statische, legendäre Bitmap fest, um eine <em>Live Vorschau</em> (auch als <em>Peek Preview</em>bezeichnet) eines Fensters oder einer Registerkarte anzuzeigen. In der Taskleiste kann diese Bitmap verwendet werden, um eine Vorschau eines Fensters oder einer Registerkarte in voller Höhe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a13cc-171">Sets a static, iconic bitmap to display a <em>live preview</em> (also known as a <em>Peek preview</em>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>Dwmcticonfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-173">Legt eine statische, ikonische Bitmap auf einem Fenster oder einer Registerkarte fest, die als Miniaturansicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a13cc-173">Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation.</span></span> <span data-ttu-id="a13cc-174">Die Taskleiste kann diese Bitmap als Miniatur Ansichts Ziel für das Fenster oder die Registerkarte verwenden.</span><span class="sxs-lookup"><span data-stu-id="a13cc-174">The taskbar can use this bitmap as a thumbnail switch target for the window or tab.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>Dwmsetpresentparameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-176">Legt die aktuellen Parameter für die Frame Komposition fest.</span><span class="sxs-lookup"><span data-stu-id="a13cc-176">Sets the present parameters for frame composition.</span></span> <br/> <span data-ttu-id="a13cc-177">" <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>Dwmsetpresentparameters</strong></a> " wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a13cc-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> is no longer supported.</span></span> <span data-ttu-id="a13cc-178">Beginnend mit Windows 8.1 geben Aufrufe von <strong>dwmsetpresentparameters</strong> immer E_NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="a13cc-178">Starting with Windows 8.1, calls to <strong>DwmSetPresentParameters</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-180">Legt den Wert von nicht-Client-renderingattributen für ein Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="a13cc-180">Sets the value of non-client rendering attributes for a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>Dwmshowcontact</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-182">Wird von einer APP oder einem Framework aufgerufen, um den Typ des visuellen Feedbacks anzugeben, der als Reaktion auf einen bestimmten touchabdruck oder Stift Kontakt gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a13cc-182">Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>Dwmtethercontact</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-184">Ermöglicht das grafische Feedback von toucheingaben und Zieh Interaktionen an den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a13cc-184">Enables the graphical feedback of touch and drag interactions to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>Dwmtransitionownedwindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-186">Koordiniert die Animationen von Tool Fenstern mit dem dwm.</span><span class="sxs-lookup"><span data-stu-id="a13cc-186">Coordinates the animations of tool windows with the DWM.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a13cc-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>Dwmunregisterminiatur</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-188">Entfernt eine DWM-Miniaturansicht, die von der <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>dwmregisterminiatur</strong></a> -Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a13cc-188">Removes a DWM thumbnail relationship created by the <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a13cc-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="a13cc-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="a13cc-190">Aktualisiert die Eigenschaften für eine DWM-Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="a13cc-190">Updates the properties for a DWM thumbnail.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

