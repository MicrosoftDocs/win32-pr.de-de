---
title: Hohe dpi-Entwicklung für Desktop Anwendungen unter Windows
description: Dieser Inhalt richtet sich an Entwickler, die Desktop Anwendungen aktualisieren möchten, um den dynamischen Bildschirm Skalierungsfaktor (auch
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102486"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a><span data-ttu-id="117fc-103">Hohe dpi-Entwicklung für Desktop Anwendungen unter Windows</span><span class="sxs-lookup"><span data-stu-id="117fc-103">High DPI Desktop Application Development on Windows</span></span>

<span data-ttu-id="117fc-104">Dieser Inhalt richtet sich an Entwickler, die Desktop Anwendungen aktualisieren möchten, um die Änderung der Anzeige Skalierungsfaktor (dpi, dpi, dpi, dpi) dynamisch durchzuführen, sodass Ihre Anwendungen auf jeder Anzeige, auf der Sie gerendert werden, auf einen Spitzenwert ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="117fc-104">This content is targeted at developers who are looking to update desktop applications to handle display scale factor (dots per inch, or DPI) changes dynamically, allowing their applications to be crisp on any display they're rendered on.</span></span>

<span data-ttu-id="117fc-105">Wenn Sie eine neue Windows-APP von Grund auf neu erstellen, empfiehlt es sich, eine universelle Windows-Plattform-Anwendung [(UWP)](/windows/uwp/get-started/whats-a-uwp) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="117fc-105">To start, if you're creating a new Windows app from scratch, it is highly recommended that you create a [Universal Windows Platform (UWP)](/windows/uwp/get-started/whats-a-uwp) application.</span></span> <span data-ttu-id="117fc-106">UWP-Anwendungen &mdash; &mdash; werden für jede Anzeige, auf der Sie ausgeführt werden, automatisch und dynamisch skaliert.</span><span class="sxs-lookup"><span data-stu-id="117fc-106">UWP applications automatically&mdash;and dynamically&mdash;scale for each display that they're running on.</span></span>

<span data-ttu-id="117fc-107">Desktop Anwendungen, die ältere Windows-Programmiertechnologien verwenden (unformatierte Win32-Programmierung, Windows Forms, Windows Presentation Framework (WPF) usw.) können die DPI-Skalierung nicht automatisch verarbeiten, ohne dass zusätzliche Entwickler arbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="117fc-107">Desktop applications using older Windows programming technologies (raw Win32 programming, Windows Forms, Windows Presentation Framework (WPF), etc.) are unable to automatically handle DPI scaling without additional developer work.</span></span> <span data-ttu-id="117fc-108">Ohne diese Arbeit werden Anwendungen in vielen gängigen Verwendungs Szenarien verschwommen oder falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="117fc-108">Without such work, applications will appear blurry or incorrectly-sized in many common usage scenarios.</span></span> <span data-ttu-id="117fc-109">Dieses Dokument enthält Kontext und Informationen dazu, was beim Aktualisieren einer Desktop Anwendung zum ordnungsgemäßen Rendering beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="117fc-109">This document provides context and information about what is involved in updating a desktop application to render correctly.</span></span>

## <a name="display-scale-factor--dpi"></a><span data-ttu-id="117fc-110">Skalierungsfaktor & dpi anzeigen</span><span class="sxs-lookup"><span data-stu-id="117fc-110">Display Scale Factor & DPI</span></span>

<span data-ttu-id="117fc-111">Wenn die Anzeige Technologie fortgeschritten ist, haben die Hersteller der Anzeige Bereiche eine wachsende Anzahl von Pixeln in jede Einheit von physischem Raum in ihren Bereichen gepackt.</span><span class="sxs-lookup"><span data-stu-id="117fc-111">As display technology has progressed, display panel manufacturers have packed an increasing number of pixels into each unit of physical space on their panels.</span></span> <span data-ttu-id="117fc-112">Dies hat zur Folge, dass die Punkte pro Zoll (dpi) moderner Anzeige Bereiche viel höher sind als in der Vergangenheit.</span><span class="sxs-lookup"><span data-stu-id="117fc-112">This has resulted in the dots per inch (DPI) of modern display panels being much higher than they have historically been.</span></span> <span data-ttu-id="117fc-113">In der Vergangenheit hatten die meisten Anzeige 96 Pixel pro linearer Zoll von physischem Speicher (96 dpi). in 2017 sind anzeigen mit fast 300 dpi oder höher sofort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="117fc-113">In the past, most displays had 96 pixels per linear inch of physical space (96 DPI); in 2017, displays with nearly 300 DPI or higher are readily available.</span></span>

<span data-ttu-id="117fc-114">Die meisten Legacy-Desktop Benutzeroberflächen-Frameworks verfügen über integrierte Annahmen, dass die Anzeige dpi während der Lebensdauer des Prozesses nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="117fc-114">Most legacy desktop UI frameworks have built-in assumptions that the display DPI will not change during the lifetime of the process.</span></span>  <span data-ttu-id="117fc-115">Diese Annahme ist nicht mehr true, und die Anzeige von DPIs ändert sich häufig mehrmals während der Lebensdauer eines Anwendungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="117fc-115">This assumption no longer holds true, with display DPIs commonly changing several times throughout an application process's lifetime.</span></span> <span data-ttu-id="117fc-116">Einige häufige Szenarien, in denen die Anzeige Skalierungsfaktor/dpi-Änderungen:</span><span class="sxs-lookup"><span data-stu-id="117fc-116">Some common scenarios where the display scale factor/DPI changes are:</span></span>

-   <span data-ttu-id="117fc-117">Konfigurationen mit mehreren Monitoren, bei denen jede Anzeige einen anderen Skalierungsfaktor hat und die Anwendung von einer Anzeige in eine andere verschoben wird (z. b. ein 4K und eine 1080p-Anzeige)</span><span class="sxs-lookup"><span data-stu-id="117fc-117">Multiple-monitor setups where each display has a different scale factor and the application is moved from one display to another (such as a 4K and a 1080p display)</span></span>
-   <span data-ttu-id="117fc-118">Andocken und Andocken eines großen dpi-Laptops mit einer externen Anzeige mit niedriger dpi (oder umgekehrt)</span><span class="sxs-lookup"><span data-stu-id="117fc-118">Docking and undocking a high DPI laptop with a low-DPI external display (or vice versa)</span></span>
-   <span data-ttu-id="117fc-119">Herstellen einer Verbindung über Remotedesktop von einem Laptop/Tablet mit hoher dpi-Verbindung mit einem Gerät mit geringer dpi (oder umgekehrt)</span><span class="sxs-lookup"><span data-stu-id="117fc-119">Connecting via Remote Desktop from a high DPI laptop/tablet to a low-DPI device (or vice versa)</span></span>
-   <span data-ttu-id="117fc-120">Ändern der Einstellungen für die Anzeige des Skalierungsfaktors während der Ausführung von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="117fc-120">Making a display-scale-factor settings change while applications are running</span></span>

<span data-ttu-id="117fc-121">In diesen Szenarien zeichnen sich UWP-Anwendungen automatisch selbst für den neuen dpi-Abschnitt neu auf.</span><span class="sxs-lookup"><span data-stu-id="117fc-121">In these scenarios, UWP applications redraw themselves for the new DPI automatically.</span></span> <span data-ttu-id="117fc-122">Standardmäßig und ohne zusätzliche Entwickler Arbeit ist dies bei Desktop Anwendungen nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="117fc-122">By default, and without additional developer work, desktop applications do not.</span></span> <span data-ttu-id="117fc-123">Desktop Anwendungen, die diese zusätzlichen Aufgaben nicht ausführen, um auf dpi-Änderungen zu reagieren, werden möglicherweise unscharf oder falsch für den Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="117fc-123">Desktop applications that don't do this extra work to respond to DPI changes may appear blurry or incorrectly-sized to the user.</span></span>

## <a name="dpi-awareness-mode"></a><span data-ttu-id="117fc-124">DPI-Awareness-Modus</span><span class="sxs-lookup"><span data-stu-id="117fc-124">DPI Awareness Mode</span></span>

<span data-ttu-id="117fc-125">Desktop Anwendungen müssen Windows informieren, wenn Sie die DPI-Skalierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="117fc-125">Desktop applications must tell Windows if they support DPI scaling.</span></span> <span data-ttu-id="117fc-126">Standardmäßig betrachtet das System Desktop Anwendungen mit dpi-Wert und Bitmap.</span><span class="sxs-lookup"><span data-stu-id="117fc-126">By default, the system considers desktop applications DPI unaware and bitmap-stretches their windows.</span></span> <span data-ttu-id="117fc-127">Wenn Sie einen der folgenden verfügbaren dpi-Awareness-Modi festlegen, können die Anwendungen explizit angeben, wie die DPI-Skalierung verarbeitet werden soll:</span><span class="sxs-lookup"><span data-stu-id="117fc-127">By setting one of the following available DPI awareness modes, applications can explicitly tell Windows how they wish to handle DPI scaling:</span></span>

### <a name="dpi-unaware"></a><span data-ttu-id="117fc-128">DPI nicht bekannt</span><span class="sxs-lookup"><span data-stu-id="117fc-128">DPI Unaware</span></span>

<span data-ttu-id="117fc-129">Dpi-abhängige Anwendungen werden mit einem Fixed-dpi-Wert von 96 (100%).</span><span class="sxs-lookup"><span data-stu-id="117fc-129">DPI unaware applications render at a fixed DPI value of 96 (100%).</span></span> <span data-ttu-id="117fc-130">Wenn diese Anwendungen auf einem Bildschirm mit einer Anzeige Skala größer als 96 dpi ausgeführt werden, wird die Anwendungs Bitmap von Windows auf die erwartete physische Größe gestreckt.</span><span class="sxs-lookup"><span data-stu-id="117fc-130">Whenever these applications are run on a screen with a display scale greater than 96 DPI, Windows will stretch the application bitmap to the expected physical size.</span></span> <span data-ttu-id="117fc-131">Dies führt dazu, dass die Anwendung verschwommen erscheint.</span><span class="sxs-lookup"><span data-stu-id="117fc-131">This results in the application appearing blurry.</span></span>

### <a name="system-dpi-awareness"></a><span data-ttu-id="117fc-132">System-dpi-Informationen</span><span class="sxs-lookup"><span data-stu-id="117fc-132">System DPI Awareness</span></span>

<span data-ttu-id="117fc-133">Desktop Anwendungen, die System-dpi-fähig sind, erhalten in der Regel den dpi-Wert des primären verbundenen Monitors zum Zeitpunkt der Benutzeranmeldung.</span><span class="sxs-lookup"><span data-stu-id="117fc-133">Desktop applications that are system DPI aware typically receive the DPI of the primary connected monitor as of the time of user sign-in.</span></span> <span data-ttu-id="117fc-134">Während der Initialisierung legen Sie die Benutzeroberfläche entsprechend fest (Größenänderung, auswählen von Schriftgrößen, Laden von Assets usw.), indem Sie diesen System-dpi-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="117fc-134">During initialization, they lay out their UI appropriately (sizing controls, choosing font sizes, loading assets, etc.) using that System DPI value.</span></span> <span data-ttu-id="117fc-135">Auf diese Weise werden System-dpi-fähige Anwendungen nicht auf dpi skaliert (Bitmap gestreckt) von Windows on zeigt das Rendering bei diesem einzelnen dpi an.</span><span class="sxs-lookup"><span data-stu-id="117fc-135">As such, System DPI-aware applications are not DPI scaled (bitmap stretched) by Windows on displays rendering at that single DPI.</span></span> <span data-ttu-id="117fc-136">Wenn die Anwendung in eine Anzeige mit einem anderen Skalierungsfaktor verschoben wird, oder wenn sich der Anzeige Skalierungsfaktor auf andere Weise ändert, wird Windows das Fenster der Anwendung skalieren, sodass Sie unscharf angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="117fc-136">When the application is moved to a display with a different scale factor, or if the display scale factor otherwise changes, Windows will bitmap scale the application's windows, making them appear blurry.</span></span> <span data-ttu-id="117fc-137">Effektiv werden System-dpi-fähige Desktop Anwendungen nur mit einem einzigen Display scale-Faktor nur mit einem einzigen Display Skalierungsfaktor versehen, wenn sich der dpi-Faktor ändert.</span><span class="sxs-lookup"><span data-stu-id="117fc-137">Effectively, System DPI-aware desktop applications only render crisply at a single display scale factor, becoming blurry whenever the DPI changes.</span></span>

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a><span data-ttu-id="117fc-138">Per-Monitor und Per-Monitor (v2) dpi-Informationen</span><span class="sxs-lookup"><span data-stu-id="117fc-138">Per-Monitor and Per-Monitor (V2) DPI Awareness</span></span>

<span data-ttu-id="117fc-139">Es wird empfohlen, Desktop Anwendungen so zu aktualisieren, dass Sie den dpi-Modus pro Monitor verwenden, sodass Sie sofort ordnungsgemäß renderfähig werden, wenn sich der dpi-Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="117fc-139">It is recommended that desktop applications be updated to use per-monitor DPI awareness mode, allowing them to immediately render correctly whenever the DPI changes.</span></span> <span data-ttu-id="117fc-140">Wenn in einer Anwendung Windows angezeigt wird, dass Sie in diesem Modus ausgeführt werden soll, wird die Anwendung von Windows nicht mit Bitmap gestreckt, wenn der dpi-Wert geändert wird. stattdessen wird [WM \_ dpichanged](wm-dpichanged.md) an das Anwendungsfenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="117fc-140">When an application reports to Windows that it wants to run in this mode, Windows will not bitmap stretch the application when the DPI changes, instead sending [WM\_DPICHANGED](wm-dpichanged.md) to the application window.</span></span> <span data-ttu-id="117fc-141">Dann ist die gesamte Aufgabe der Anwendung, die Größe der neuen dpi-Größe selbst zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="117fc-141">It is then the complete responsibility of the application to handle resizing itself for the new DPI.</span></span> <span data-ttu-id="117fc-142">Die meisten Benutzeroberflächen-Frameworks, die von Desktop Anwendungen verwendet werden (allgemeine Windows-Steuerelemente (Comctl32), Windows Forms, Windows Presentation Framework usw.) unterstützen keine automatische DPI-Skalierung, sodass Entwickler die Größe der Inhalte ihrer Fenster selbst ändern und neu positionieren müssen.</span><span class="sxs-lookup"><span data-stu-id="117fc-142">Most UI frameworks used by desktop applications (Windows common controls (comctl32), Windows Forms, Windows Presentation Framework, etc.) do not support automatic DPI scaling, requiring developers to resize and reposition the contents of their windows themselves.</span></span>

<span data-ttu-id="117fc-143">Es gibt zwei Versionen von Per-Monitor Awareness, dass sich eine Anwendung selbst registrieren kann: Version 1 und Version 2 (PMv2).</span><span class="sxs-lookup"><span data-stu-id="117fc-143">There are two versions of Per-Monitor awareness that an application can register itself as: version 1 and version 2 (PMv2).</span></span> <span data-ttu-id="117fc-144">Das Registrieren eines Prozesses als Ausführung im PMv2-Awareness-Modus führt zu folgenden Ergebnissen:</span><span class="sxs-lookup"><span data-stu-id="117fc-144">Registering a process as running in PMv2 awareness mode results in:</span></span>

1.  <span data-ttu-id="117fc-145">Die Anwendung, die benachrichtigt wird, wenn sich der dpi-Wert ändert (sowohl die der obersten als auch die untergeordneten HWNDs)</span><span class="sxs-lookup"><span data-stu-id="117fc-145">The application being notified when the DPI changes (both the top-level and child HWNDs)</span></span>
2.  <span data-ttu-id="117fc-146">Die Anwendung, die die unformatierten Pixel der einzelnen anzeigen anzeigen</span><span class="sxs-lookup"><span data-stu-id="117fc-146">The application seeing the raw pixels of each display</span></span>
3.  <span data-ttu-id="117fc-147">Die Anwendung wird von Windows nie als Bitmap skaliert.</span><span class="sxs-lookup"><span data-stu-id="117fc-147">The application never being bitmap scaled by Windows</span></span>
4.  <span data-ttu-id="117fc-148">Automatischer nicht-Client Bereich (Fenster Beschriftung, Scrollleisten usw.) DPI-Skalierung nach Windows</span><span class="sxs-lookup"><span data-stu-id="117fc-148">Automatic non-client area (window caption, scroll bars, etc.) DPI scaling by Windows</span></span>
5.  <span data-ttu-id="117fc-149">Win32-Dialoge (aus " [deatedialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)") werden von Windows automatisch mit dpi skaliert</span><span class="sxs-lookup"><span data-stu-id="117fc-149">Win32 dialogs (from [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatically DPI scaled by Windows</span></span>
6.  <span data-ttu-id="117fc-150">Design-gezeichnete Bitmap-Objekte in allgemeinen Steuerelementen (Kontrollkästchen, Schaltflächen Hintergründe usw.) werden automatisch am richtigen dpi-Skalierungsfaktor gerendert.</span><span class="sxs-lookup"><span data-stu-id="117fc-150">Theme-drawn bitmap assets in common controls (checkboxes, button backgrounds, etc.) being automatically rendered at the appropriate DPI scale factor</span></span>

<span data-ttu-id="117fc-151">Bei der Ausführung im Per-Monitor v2-Awareness-Modus werden Anwendungen benachrichtigt, wenn sich Ihr dpi-Zeitpunkt geändert hat.</span><span class="sxs-lookup"><span data-stu-id="117fc-151">When running in Per-Monitor v2 Awareness mode, applications are notified when their DPI has changed.</span></span> <span data-ttu-id="117fc-152">Wenn die Größe einer Anwendung für den neuen dpi-Wert nicht geändert wird, wird die Benutzeroberfläche der Anwendung zu klein oder zu groß angezeigt (abhängig von der Differenz der vorherigen und neuen dpi-Werte).</span><span class="sxs-lookup"><span data-stu-id="117fc-152">If an application does not resize itself for the new DPI, the application UI will appear too small or too large (depending on the difference in the previous and new DPI values).</span></span>

> [!Note]  
> <span data-ttu-id="117fc-153">Das PMv1-Bewusstsein (Per-Monitor v1) ist sehr begrenzt.</span><span class="sxs-lookup"><span data-stu-id="117fc-153">Per-Monitor V1 (PMv1) awareness is very limited.</span></span> <span data-ttu-id="117fc-154">Es wird empfohlen, dass Anwendungen PMv2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="117fc-154">It is recommended that applications use PMv2.</span></span>

<span data-ttu-id="117fc-155">In der folgenden Tabelle wird gezeigt, wie Anwendungen in verschiedenen Szenarien dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="117fc-155">The following table shows how applications will render under different scenarios:</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="117fc-156">DPI-Awareness-Modus</span><span class="sxs-lookup"><span data-stu-id="117fc-156">DPI Awareness Mode</span></span></th>
<th><span data-ttu-id="117fc-157">Eingeführte Windows-Version</span><span class="sxs-lookup"><span data-stu-id="117fc-157">Windows Version Introduced</span></span></th>
<th><span data-ttu-id="117fc-158">Anwendungs Ansicht von dpi</span><span class="sxs-lookup"><span data-stu-id="117fc-158">Application's view of DPI</span></span></th>
<th><span data-ttu-id="117fc-159">Verhalten bei dpi-Änderungen</span><span class="sxs-lookup"><span data-stu-id="117fc-159">Behavior on DPI change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="117fc-160">Bewusste</span><span class="sxs-lookup"><span data-stu-id="117fc-160">Unaware</span></span></td>
<td><span data-ttu-id="117fc-161">–</span><span class="sxs-lookup"><span data-stu-id="117fc-161">N/A</span></span></td>
<td><span data-ttu-id="117fc-162">Alle anzeigen sind 96 dpi.</span><span class="sxs-lookup"><span data-stu-id="117fc-162">All displays are 96 DPI</span></span></td>
<td><span data-ttu-id="117fc-163">Bitmap-Streckung (Blurry)</span><span class="sxs-lookup"><span data-stu-id="117fc-163">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="117fc-164">System</span><span class="sxs-lookup"><span data-stu-id="117fc-164">System</span></span></td>
<td><span data-ttu-id="117fc-165">Vista</span><span class="sxs-lookup"><span data-stu-id="117fc-165">Vista</span></span></td>
<td><span data-ttu-id="117fc-166">Alle anzeigen weisen denselben dpi-Vorgang auf (der dpi-Zeitpunkt der primären Anzeige zum Zeitpunkt des Starts der aktuellen Benutzersitzung).</span><span class="sxs-lookup"><span data-stu-id="117fc-166">All displays have the same DPI (the DPI of the primary display at the time the current user session was started)</span></span></td>
<td><span data-ttu-id="117fc-167">Bitmap-Streckung (Blurry)</span><span class="sxs-lookup"><span data-stu-id="117fc-167">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="117fc-168">Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="117fc-168">Per-Monitor</span></span></td>
<td><span data-ttu-id="117fc-169">8.1</span><span class="sxs-lookup"><span data-stu-id="117fc-169">8.1</span></span></td>
<td><span data-ttu-id="117fc-170">Der dpi-Wert der Anzeige, in der sich das Anwendungsfenster hauptsächlich befindet</span><span class="sxs-lookup"><span data-stu-id="117fc-170">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="117fc-171">HWND der obersten Ebene wird bei dpi-Änderungen benachrichtigt</span><span class="sxs-lookup"><span data-stu-id="117fc-171">Top-level HWND is notified of DPI change</span></span></li>
<li><span data-ttu-id="117fc-172">Keine DPI-Skalierung von Benutzeroberflächen Elementen.</span><span class="sxs-lookup"><span data-stu-id="117fc-172">No DPI scaling of any UI elements.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="117fc-173">Per-Monitor v2</span><span class="sxs-lookup"><span data-stu-id="117fc-173">Per-Monitor V2</span></span></td>
<td><span data-ttu-id="117fc-174">Windows 10 Creators Update (1703)</span><span class="sxs-lookup"><span data-stu-id="117fc-174">Windows 10 Creators Update (1703)</span></span></td>
<td><span data-ttu-id="117fc-175">Der dpi-Wert der Anzeige, in der sich das Anwendungsfenster hauptsächlich befindet</span><span class="sxs-lookup"><span data-stu-id="117fc-175">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="117fc-176">Auf oberster Ebene <span class="underline">und</span> untergeordnete HWNDs werden bei dpi-Änderungen benachrichtigt</span><span class="sxs-lookup"><span data-stu-id="117fc-176">Top-level <span class="underline">and</span> child HWNDs are notified of DPI change</span></span></li>
</ul>
<br/> <span data-ttu-id="117fc-177"><span class="underline">Automatische DPI-Skalierung von:</span>
</span><span class="sxs-lookup"><span data-stu-id="117fc-177"><span class="underline">Automatic DPI scaling of:</span>
</span></span><ul>
<li><span data-ttu-id="117fc-178">Nicht-Client Bereich</span><span class="sxs-lookup"><span data-stu-id="117fc-178">Non-client area</span></span></li>
<li><span data-ttu-id="117fc-179">Design-gezeichnete Bitmaps in allgemeinen Steuerelementen (Comctl32 V6)</span><span class="sxs-lookup"><span data-stu-id="117fc-179">Theme-drawn bitmaps in common controls (comctl32 V6)</span></span></li>
<li><span data-ttu-id="117fc-180">Dialogfelder ("<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">kreatedialog</a>")</span><span class="sxs-lookup"><span data-stu-id="117fc-180">Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a><span data-ttu-id="117fc-181">DPI-Informationen pro Monitor (v1)</span><span class="sxs-lookup"><span data-stu-id="117fc-181">Per Monitor (V1) DPI Awareness</span></span>

<span data-ttu-id="117fc-182">Per-Monitor v1-dpi-Awareness-Modus (PMv1) wurde mit Windows 8.1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="117fc-182">Per-Monitor V1 DPI awareness mode (PMv1) was introduced with Windows 8.1.</span></span> <span data-ttu-id="117fc-183">Dieser dpi-Awareness-Modus ist sehr begrenzt und bietet nur die unten aufgeführten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="117fc-183">This DPI awareness mode is very limited and only offers the functionality listed below.</span></span> <span data-ttu-id="117fc-184">Es wird empfohlen, dass Desktop Anwendungen den Per-Monitor v2-Sensibilisierungs Modus verwenden, der unter Windows 10 1703 oder höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="117fc-184">It is recommended that desktop applications use Per-Monitor v2 awareness mode, supported on Windows 10 1703 or above.</span></span>

<span data-ttu-id="117fc-185">Die anfängliche Unterstützung für die Überwachung pro Monitor bot nur Anwendungen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="117fc-185">The initial support for per-monitor awareness only offered applications the following:</span></span>

1.  <span data-ttu-id="117fc-186">HWNDs der obersten Ebene werden über eine dpi-Änderung benachrichtigt und eine neue vorgeschlagene Größe bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="117fc-186">Top-level HWNDs are notified of a DPI change and provided a new suggested size</span></span>
2.  <span data-ttu-id="117fc-187">Windows wird keine bitmapstreckung der Anwendungs Benutzeroberfläche durchführt</span><span class="sxs-lookup"><span data-stu-id="117fc-187">Windows will not bitmap stretch the application UI</span></span>
3.  <span data-ttu-id="117fc-188">Die Anwendung sieht alle anzeigen in physischen Pixeln (siehe Virtualisierung).</span><span class="sxs-lookup"><span data-stu-id="117fc-188">The application sees all displays in physical pixels (see virtualization)</span></span>

<span data-ttu-id="117fc-189">Unter Windows 10 1607 oder höher können PMv1-Anwendungen bei WM nccreate auch [enablenonclientdpiscalingaufgerufen](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) werden, \_ um anzufordern, dass Windows den nicht-Client Bereich des Fensters ordnungsgemäß skaliert.</span><span class="sxs-lookup"><span data-stu-id="117fc-189">On Windows 10 1607 or above, PMv1 applications may also call [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) during WM\_NCCREATE to request that Windows correctly scale the window's non-client area.</span></span>

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a><span data-ttu-id="117fc-190">DPI-Skalierungs Unterstützung pro Monitor durch Benutzeroberflächen Framework/-Technologie</span><span class="sxs-lookup"><span data-stu-id="117fc-190">Per Monitor DPI Scaling Support by UI Framework / Technology</span></span>

<span data-ttu-id="117fc-191">Die folgende Tabelle zeigt die Ebene der Unterstützung für dpi-Informationen pro Monitor, die von verschiedenen Windows-Benutzeroberflächen-Frameworks ab Windows 10 1703 angeboten wird:</span><span class="sxs-lookup"><span data-stu-id="117fc-191">The table below shows the level of per-monitor DPI awareness support offered by various Windows UI frameworks as of Windows 10 1703:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="117fc-192">Framework/Technologie</span><span class="sxs-lookup"><span data-stu-id="117fc-192">Framework / Technology</span></span></th>
<th><span data-ttu-id="117fc-193">Support</span><span class="sxs-lookup"><span data-stu-id="117fc-193">Support</span></span></th>
<th><span data-ttu-id="117fc-194">Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="117fc-194">OS Version</span></span></th>
<th><span data-ttu-id="117fc-195">DPI-Skalierung verarbeitet von</span><span class="sxs-lookup"><span data-stu-id="117fc-195">DPI Scaling handled by</span></span></th>
<th><span data-ttu-id="117fc-196">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="117fc-196">Further Reading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="117fc-197">Universelle Windows-Plattform (UWP)</span><span class="sxs-lookup"><span data-stu-id="117fc-197">Universal Windows Platform (UWP)</span></span></td>
<td><span data-ttu-id="117fc-198">Vollständig</span><span class="sxs-lookup"><span data-stu-id="117fc-198">Full</span></span></td>
<td><span data-ttu-id="117fc-199">1607</span><span class="sxs-lookup"><span data-stu-id="117fc-199">1607</span></span></td>
<td><span data-ttu-id="117fc-200">UI-Framework</span><span class="sxs-lookup"><span data-stu-id="117fc-200">UI framework</span></span></td>
<td><span data-ttu-id="117fc-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universelle Windows-Plattform (UWP)</a></span><span class="sxs-lookup"><span data-stu-id="117fc-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universal Windows Platform (UWP)</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="117fc-202">Unformatierte Win32-/Common-Steuerelemente V6 (comctl32.dll)</span><span class="sxs-lookup"><span data-stu-id="117fc-202">Raw Win32/Common Controls V6 (comctl32.dll)</span></span></td>
<td><ul>
<li><span data-ttu-id="117fc-203">An alle HWNDs gesendete dpi-Änderungs Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="117fc-203">DPI change notification messages sent to all HWNDs</span></span></li>
<li><span data-ttu-id="117fc-204">Design-gezeichnete Objekte werden korrekt in allgemeinen Steuerelementen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="117fc-204">Theme-drawn assets render correctly in common controls</span></span></li>
<li><span data-ttu-id="117fc-205">Automatische DPI-Skalierung für Dialoge</span><span class="sxs-lookup"><span data-stu-id="117fc-205">Automatic DPI scaling for dialogs</span></span></li>
</ul></td>
<td><span data-ttu-id="117fc-206">1703</span><span class="sxs-lookup"><span data-stu-id="117fc-206">1703</span></span></td>
<td><span data-ttu-id="117fc-207">Application</span><span class="sxs-lookup"><span data-stu-id="117fc-207">Application</span></span></td>
<td><span data-ttu-id="117fc-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub-Beispiel</a></span><span class="sxs-lookup"><span data-stu-id="117fc-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="117fc-209">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="117fc-209">Windows Forms</span></span></td>
<td><span data-ttu-id="117fc-210">Eingeschränkte automatische pro-Monitor-DPI-Skalierung für einige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="117fc-210">Limited automatic per-monitor DPI scaling for some controls</span></span></td>
<td><span data-ttu-id="117fc-211">1703</span><span class="sxs-lookup"><span data-stu-id="117fc-211">1703</span></span></td>
<td><span data-ttu-id="117fc-212">UI-Framework</span><span class="sxs-lookup"><span data-stu-id="117fc-212">UI framework</span></span></td>
<td><span data-ttu-id="117fc-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Hohe dpi-Unterstützung in Windows Forms</a></span><span class="sxs-lookup"><span data-stu-id="117fc-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">High DPI Support in Windows Forms</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="117fc-214">Windows Presentation Framework (WPF)</span><span class="sxs-lookup"><span data-stu-id="117fc-214">Windows Presentation Framework (WPF)</span></span></td>
<td><span data-ttu-id="117fc-215">Systemeigene WPF-Anwendungen, die in anderen Frameworks gehostete WPF-Anwendungen und andere in WPF gehostete Frameworks nicht automatisch skalieren</span><span class="sxs-lookup"><span data-stu-id="117fc-215">Native WPF applications will DPI scale WPF hosted in other frameworks and other frameworks hosted in WPF do not automatically scale</span></span></td>
<td><span data-ttu-id="117fc-216">1607</span><span class="sxs-lookup"><span data-stu-id="117fc-216">1607</span></span></td>
<td><span data-ttu-id="117fc-217">UI-Framework</span><span class="sxs-lookup"><span data-stu-id="117fc-217">UI framework</span></span></td>
<td><span data-ttu-id="117fc-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub-Beispiel</a></span><span class="sxs-lookup"><span data-stu-id="117fc-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="117fc-219">GDI</span><span class="sxs-lookup"><span data-stu-id="117fc-219">GDI</span></span></td>
<td><span data-ttu-id="117fc-220">Keine</span><span class="sxs-lookup"><span data-stu-id="117fc-220">None</span></span></td>
<td><span data-ttu-id="117fc-221">–</span><span class="sxs-lookup"><span data-stu-id="117fc-221">N/A</span></span></td>
<td><span data-ttu-id="117fc-222">Application</span><span class="sxs-lookup"><span data-stu-id="117fc-222">Application</span></span></td>
<td><span data-ttu-id="117fc-223">Siehe <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI-Skalierung</a></span><span class="sxs-lookup"><span data-stu-id="117fc-223">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="117fc-224">GDI+</span><span class="sxs-lookup"><span data-stu-id="117fc-224">GDI+</span></span></td>
<td><span data-ttu-id="117fc-225">Keine</span><span class="sxs-lookup"><span data-stu-id="117fc-225">None</span></span></td>
<td><span data-ttu-id="117fc-226">–</span><span class="sxs-lookup"><span data-stu-id="117fc-226">N/A</span></span></td>
<td><span data-ttu-id="117fc-227">Application</span><span class="sxs-lookup"><span data-stu-id="117fc-227">Application</span></span></td>
<td><span data-ttu-id="117fc-228">Siehe <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI-Skalierung</a></span><span class="sxs-lookup"><span data-stu-id="117fc-228">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="117fc-229">MFC</span><span class="sxs-lookup"><span data-stu-id="117fc-229">MFC</span></span></td>
<td><span data-ttu-id="117fc-230">Keine</span><span class="sxs-lookup"><span data-stu-id="117fc-230">None</span></span></td>
<td><span data-ttu-id="117fc-231">–</span><span class="sxs-lookup"><span data-stu-id="117fc-231">N/A</span></span></td>
<td><span data-ttu-id="117fc-232">Application</span><span class="sxs-lookup"><span data-stu-id="117fc-232">Application</span></span></td>
<td><span data-ttu-id="117fc-233">–</span><span class="sxs-lookup"><span data-stu-id="117fc-233">N/A</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a><span data-ttu-id="117fc-234">Aktualisieren bestehender Anwendungen</span><span class="sxs-lookup"><span data-stu-id="117fc-234">Updating Existing Applications</span></span>

<span data-ttu-id="117fc-235">Um eine vorhandene Desktop Anwendung zum ordnungsgemäßen verarbeiten der DPI-Skalierung zu aktualisieren, muss Sie so aktualisiert werden, dass zumindest die wichtigen Teile der Benutzeroberfläche aktualisiert werden, um auf dpi-Änderungen zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="117fc-235">In order to update an existing desktop application to handle DPI scaling properly, it needs to be updated such that, at a minimum, the important parts of its UI are updated to respond to DPI changes.</span></span>

<span data-ttu-id="117fc-236">Die meisten Desktop Anwendungen werden im System-dpi-Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="117fc-236">Most desktop applications run under system DPI awareness mode.</span></span> <span data-ttu-id="117fc-237">Anwendungen mit System-dpi-Unterstützung Skalieren in der Regel auf den dpi-Wert der primären Anzeige (die Anzeige, in der sich die Taskleiste zum Zeitpunkt der Windows-Sitzung befand).</span><span class="sxs-lookup"><span data-stu-id="117fc-237">System-DPI-aware applications typically scale to the DPI of the primary display (the display that the system tray was located on at the time the Windows session was started).</span></span> <span data-ttu-id="117fc-238">Wenn sich der dpi-Wert ändert, wird die Benutzeroberfläche dieser Anwendungen von Windows durch Bitmap gestreckt, was häufig zu einer Unschärfe führt.</span><span class="sxs-lookup"><span data-stu-id="117fc-238">When the DPI changes, Windows will bitmap stretch the UI of these applications, which often results in them being blurry.</span></span> <span data-ttu-id="117fc-239">Beim Aktualisieren einer System-DPI-fähigen Anwendung, die pro Monitor-dpi-Wert unterstützt wird, muss der Code, der das Benutzeroberflächen Layout verarbeitet, so aktualisiert werden, dass es nicht nur während der Anwendungs Initialisierung ausgeführt wird, sondern auch, wenn eine dpi-Änderungs Benachrichtigung ([WM \_ dpichanged](wm-dpichanged.md) im Fall von Win32) empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="117fc-239">When updating a System DPI-aware application to become per-monitor-DPI aware, the code which handles UI layout needs to be updated such that it is performed not only during application initialization, but also whenever a DPI change notification ([WM\_DPICHANGED](wm-dpichanged.md) in the case of Win32) is received.</span></span> <span data-ttu-id="117fc-240">Dies umfasst in der Regel das erneute Aufrufen von Annahmen im Code, dass die Benutzeroberfläche nur einmal skaliert werden muss.</span><span class="sxs-lookup"><span data-stu-id="117fc-240">This typically involves revisiting any assumptions in the code that the UI only needs to be scaled once.</span></span>

<span data-ttu-id="117fc-241">Im Fall von Win32-Programmierung haben viele Win32-APIs auch keinen dpi-oder Anzeige Kontext, sodass Sie nur Werte relativ zum System-dpi-Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="117fc-241">Also, in the case of Win32 programming, many Win32 APIs do not have any DPI or display context so they will only return values relative to the System DPI.</span></span> <span data-ttu-id="117fc-242">Es kann nützlich sein, den Code zu durchlaufen, um nach einigen dieser APIs zu suchen und diese durch dpi-abhängige Varianten zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="117fc-242">It can be useful to grep through your code to look for some of these APIs and replace them with DPI-aware variants.</span></span> <span data-ttu-id="117fc-243">Einige der gängigen APIs mit dpi-abhängigen Varianten sind:</span><span class="sxs-lookup"><span data-stu-id="117fc-243">Some of the common APIs that have DPI-aware variants are:</span></span>



| <span data-ttu-id="117fc-244">Single dpi-Version</span><span class="sxs-lookup"><span data-stu-id="117fc-244">Single DPI version</span></span>   | <span data-ttu-id="117fc-245">Per-Monitor Version</span><span class="sxs-lookup"><span data-stu-id="117fc-245">Per-Monitor version</span></span>        |
|----------------------|----------------------------|
| <span data-ttu-id="117fc-246">GetSystemMetrics</span><span class="sxs-lookup"><span data-stu-id="117fc-246">GetSystemMetrics</span></span>     | <span data-ttu-id="117fc-247">Getsystemmetricsfordpi</span><span class="sxs-lookup"><span data-stu-id="117fc-247">GetSystemMetricsForDpi</span></span>     |
| <span data-ttu-id="117fc-248">"Setting windowrectex"</span><span class="sxs-lookup"><span data-stu-id="117fc-248">AdjustWindowRectEx</span></span>   | <span data-ttu-id="117fc-249">"Setting windowrectexfordpi"</span><span class="sxs-lookup"><span data-stu-id="117fc-249">AdjustWindowRectExForDpi</span></span>   |
| <span data-ttu-id="117fc-250">SystemParametersInfo</span><span class="sxs-lookup"><span data-stu-id="117fc-250">SystemParametersInfo</span></span> | <span data-ttu-id="117fc-251">Systemparametersinfofordpi</span><span class="sxs-lookup"><span data-stu-id="117fc-251">SystemParametersInfoForDpi</span></span> |
| <span data-ttu-id="117fc-252">Getdpiformonitor</span><span class="sxs-lookup"><span data-stu-id="117fc-252">GetDpiForMonitor</span></span>     | <span data-ttu-id="117fc-253">Getdpiforwindow</span><span class="sxs-lookup"><span data-stu-id="117fc-253">GetDpiForWindow</span></span>            |



 

<span data-ttu-id="117fc-254">Es ist auch eine gute Idee, in Ihrer Codebasis nach hart codierten Größen zu suchen, die einen konstanten dpi-Wert annehmen. Diese werden durch Code ersetzt, der die DPI-Skalierung ordnungsgemäß berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="117fc-254">It is also a good idea to search for hard-coded sizes in your codebase that assume a constant DPI, replacing them with code that correctly accounts for DPI scaling.</span></span> <span data-ttu-id="117fc-255">Im folgenden finden Sie ein Beispiel, das alle diese Vorschläge umfasst:</span><span class="sxs-lookup"><span data-stu-id="117fc-255">Below is an example that incorporates all of these suggestions:</span></span>

### <a name="example"></a><span data-ttu-id="117fc-256">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="117fc-256">Example:</span></span>

<span data-ttu-id="117fc-257">Das folgende Beispiel zeigt einen vereinfachten Win32-Fall, bei dem ein untergeordnetes HWND erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="117fc-257">The example below shows a simplified Win32 case of creating a child HWND.</span></span> <span data-ttu-id="117fc-258">Beim Aufrufen von "upatewindow" wird davon ausgegangen, dass die Anwendung mit 96 dpi ausgeführt wird und weder die Größe der Schaltfläche noch die Position bei höheren DPIs korrekt ist:</span><span class="sxs-lookup"><span data-stu-id="117fc-258">The call to CreateWindow assumes that the application is running at 96 DPI, and neither the button's size nor position will be correct at higher DPIs:</span></span>


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



<span data-ttu-id="117fc-259">Der aktualisierte Code unten zeigt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="117fc-259">The updated code below shows:</span></span>

1.  <span data-ttu-id="117fc-260">Der Code Erstellungs Code dpi, der die Position und die Größe des untergeordneten HWND für den dpi-Wert des übergeordneten Fensters skaliert.</span><span class="sxs-lookup"><span data-stu-id="117fc-260">The window-creation code DPI scaling the position and size of the child HWND for the DPI of its parent window</span></span>
2.  <span data-ttu-id="117fc-261">Reagieren auf dpi-Änderungen durch Neupositionieren und Ändern der Größe des untergeordneten HWND</span><span class="sxs-lookup"><span data-stu-id="117fc-261">Responding to DPI change by repositioning and resizing the child HWND</span></span>
3.  <span data-ttu-id="117fc-262">Die hart codierten Größen wurden entfernt und durch Code ersetzt, der auf dpi-Änderungen antwortet.</span><span class="sxs-lookup"><span data-stu-id="117fc-262">Hard-coded sizes removed and replaced with code that responds to DPI changes</span></span>


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



<span data-ttu-id="117fc-263">Beim Aktualisieren einer System-DPI-fähigen Anwendung sind einige häufige Schritte zu befolgen:</span><span class="sxs-lookup"><span data-stu-id="117fc-263">When updating a System DPI-aware application, some common steps to follow are:</span></span>

1.  <span data-ttu-id="117fc-264">Markieren Sie den Prozess mit dpi-Werten pro Monitor (v2), indem Sie ein Anwendungs Manifest (oder eine andere Methode, abhängig von den verwendeten Benutzeroberflächen-Frameworks) verwenden.</span><span class="sxs-lookup"><span data-stu-id="117fc-264">Mark the process as per-monitor DPI aware (V2) using an application manifest (or other method, depending on the UI framework(s) used).</span></span>
2.  <span data-ttu-id="117fc-265">Machen Sie die Benutzeroberflächen-Layoutlogik wiederverwendbar, und verschieben Sie Sie aus dem Anwendungs Initialisierungs Code so, dass Sie wieder verwendet werden kann, wenn eine dpi-Änderung auftritt (WM \_ dpichanged im Fall von Windows-Programmierung (Win32)).</span><span class="sxs-lookup"><span data-stu-id="117fc-265">Make UI layout logic reusable and move it out of application-initialization code such that it can be reused when a DPI change occurs (WM\_DPICHANGED in the case of Windows (Win32) programming).</span></span>
3.  <span data-ttu-id="117fc-266">Für ungültig erklärten Code, der annimmt, dass dpi-sensible Daten (dpi/Fonts/sizes usw.) niemals aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="117fc-266">Invalidate any code that assumes that DPI-sensitive data (DPI/fonts/sizes/etc.) never need to be updated.</span></span> <span data-ttu-id="117fc-267">Es ist eine gängige Vorgehensweise, bei der Prozess Initialisierung Schriftgrößen und dpi-Werte zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="117fc-267">It is a very common practice to cache font sizes and DPI values at process initialization.</span></span> <span data-ttu-id="117fc-268">Wenn Sie eine Anwendung so aktualisieren, dass Sie mit dpi-Werten pro Monitor erreicht wird, müssen dpi-sensible Daten neu ausgewertet werden, wenn ein neuer dpi-Wert erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="117fc-268">When updating an application to become per-monitor DPI aware, DPI-sensitive data must be reevaluated whenever a new DPI is encountered.</span></span>
4.  <span data-ttu-id="117fc-269">Wenn eine dpi-Änderung durchgeführt wird, laden Sie alle bitmapassets für den neuen dpi-Vorgang neu bzw. ändern Sie Sie neu, oder verwenden Sie optional Bitmap die aktuell geladenen Assets auf die richtige Größe.</span><span class="sxs-lookup"><span data-stu-id="117fc-269">When a DPI change occurs, reload (or re-rasterize) any bitmap assets for the new DPI or, optionally, bitmap stretch the currently loaded assets to the correct size.</span></span>
5.  <span data-ttu-id="117fc-270">Grep für APIs, die nicht Per-Monitor dpi-fähig sind und Sie durch Per-Monitor dpi-fähigen APIs ersetzen (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="117fc-270">Grep for APIs that are not Per-Monitor DPI aware and replace them with Per-Monitor DPI-aware APIs (where applicable).</span></span> <span data-ttu-id="117fc-271">Beispiel: Ersetzen Sie GetSystemMetrics durch getsystemmetricsfordpi.</span><span class="sxs-lookup"><span data-stu-id="117fc-271">Example: replace GetSystemMetrics with GetSystemMetricsForDpi.</span></span>
6.  <span data-ttu-id="117fc-272">Testen Sie die Anwendung auf einem Multidisplay-/Multi-dpi-System.</span><span class="sxs-lookup"><span data-stu-id="117fc-272">Test your application on a multiple-display/multi-DPI system.</span></span>
7.  <span data-ttu-id="117fc-273">Verwenden Sie für alle Fenster der obersten Ebene in Ihrer Anwendung, die Sie nicht auf die richtige dpi-Skala aktualisieren können, die DPI-Skalierung im gemischten Modus (unten beschrieben), um die Bitmap-Streckung dieser Fenster der obersten Ebene durch das System zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="117fc-273">For any top-level windows in your application that you are unable to update to properly DPI scale, use mixed-mode DPI scaling (described below) to allow bitmap stretching of these top-level windows by the system.</span></span>

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a><span data-ttu-id="117fc-274">Mixed-Mode DPI-Skalierung (DPI-Skalierung unter Prozess)</span><span class="sxs-lookup"><span data-stu-id="117fc-274">Mixed-Mode DPI Scaling (Sub-Process DPI Scaling)</span></span>

<span data-ttu-id="117fc-275">Beim Aktualisieren einer Anwendung zur Unterstützung der dpi-Konformität pro Monitor kann es manchmal unpraktisch sein, jedes Fenster in der Anwendung in einem einzigen Schritt zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="117fc-275">When updating an application to support per-monitor DPI awareness, it can sometimes become impractical or impossible to update every window in the application in one go.</span></span> <span data-ttu-id="117fc-276">Dies kann einfach auf die Zeit und den Aufwand zurückzuführen sein, die zum Aktualisieren und Testen der gesamten Benutzeroberfläche erforderlich sind, oder weil Sie nicht den gesamten UI-Code besitzen, den Sie ausführen müssen (wenn die Anwendung möglicherweise die Benutzeroberfläche von Drittanbietern lädt).</span><span class="sxs-lookup"><span data-stu-id="117fc-276">This can simply be due to the time and effort required to update and test all UI, or because you do not own all of the UI code that you need to run (if your application perhaps loads third-party UI).</span></span> <span data-ttu-id="117fc-277">In diesen Situationen bietet Windows eine Möglichkeit zur Erleichterung der Überwachung pro Monitor, indem es Ihnen ermöglicht, einige ihrer Anwendungsfenster (nur auf oberster Ebene) in Ihrem ursprünglichen dpi-Kompatibilitätsmodus auszuführen, während Sie sich auf Ihre Zeit und ihre Energie konzentrieren, um die wichtigsten Teile Ihrer Benutzeroberfläche zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="117fc-277">In these situations, Windows offers a way to ease into the world of per-monitor awareness by letting you run some of your application windows (top-level only) in their original DPI-awareness mode while you focus your time and energy updating the more important parts of your UI.</span></span>

<span data-ttu-id="117fc-278">Im folgenden wird veranschaulicht, wie das aussehen könnte: Sie aktualisieren die Benutzeroberfläche der Hauptanwendung ("Hauptfenster" in der Abbildung), sodass Sie mit dem dpi-Bewusstsein pro Monitor ausgeführt werden können, während Sie andere Fenster im vorhandenen Modus ausführen ("sekundäres Fenster").</span><span class="sxs-lookup"><span data-stu-id="117fc-278">Below is an illustration of what this could look like: you update your main application UI ("Main Window"  in the illustration) to run with per-monitor DPI awareness while you run other windows in their existing mode ("Secondary Window").</span></span>

![Unterschiede bei der DPI-Skalierung zwischen den Informations Modi](images/hub-page-illustrations.png)

<span data-ttu-id="117fc-280">Vor dem Windows 10 Anniversary Update (1607) war der dpi-Awareness-Modus eines Prozesses eine Prozess weite Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="117fc-280">Prior to the Windows 10 Anniversary Update (1607), the DPI awareness mode of a process was a process-wide property.</span></span> <span data-ttu-id="117fc-281">Ab dem Windows 10 Anniversary Update kann diese Eigenschaft jetzt pro Fenster der **obersten Ebene** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="117fc-281">Beginning in the Windows 10 Anniversary Update, this property can now be set per **top-level** window.</span></span> <span data-ttu-id="117fc-282">(**Unter** geordnete Fenster müssen weiterhin der Skalierungs Größe ihres übergeordneten Elements entsprechen.) Ein Fenster der obersten Ebene ist als Fenster ohne übergeordnetes Element definiert.</span><span class="sxs-lookup"><span data-stu-id="117fc-282">(**Child** windows must continue to match the scaling size of their parent.) A top-level window is defined as a window with no parent.</span></span> <span data-ttu-id="117fc-283">Dies ist in der Regel ein "reguläres" Fenster mit den Schaltflächen Minimieren, maximieren und schließen.</span><span class="sxs-lookup"><span data-stu-id="117fc-283">This is typically a "regular" window with minimize, maximize, and close buttons.</span></span> <span data-ttu-id="117fc-284">Das Szenario, für das das unter Prozess-dpi-Bewusstsein vorgesehen ist, besteht darin, dass die sekundäre Benutzeroberfläche von Windows (Bitmap gestreckt) skaliert wird, während Sie sich auf die Aktualisierung Ihrer primären Benutzeroberfläche konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="117fc-284">The scenario that sub-process DPI awareness is intended for is to have secondary UI scaled by Windows (bitmap stretched) while you focus your time and resources on updating your primary UI.</span></span>

<span data-ttu-id="117fc-285">Um unter Prozess-dpi-Informationen zu aktivieren, rufen Sie [**setthreaddpiawareness Context**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) vor und nach jedem Fenster Erstellungs Aufruf auf.</span><span class="sxs-lookup"><span data-stu-id="117fc-285">To enable sub-process DPI awareness, call [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) before and after any window creation calls.</span></span> <span data-ttu-id="117fc-286">Das Fenster, das erstellt wird, wird mit dem dpi-Bewusstsein verknüpft, das Sie über setthreaddpiawareness Context festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="117fc-286">The window that is created will be associated with the DPI awareness that you set via SetThreadDpiAwarenessContext.</span></span> <span data-ttu-id="117fc-287">Verwenden Sie den zweiten-Befehl, um die dpi-Informationen des aktuellen Threads wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="117fc-287">Use the second call to restore the current thread s DPI awareness.</span></span>

<span data-ttu-id="117fc-288">Wenn Sie die unter Prozess-DPI-Skalierung verwenden, können Sie sich auf Windows verlassen, um einige der DPI-Skalierung für Ihre Anwendung durchzuführen. Dadurch können Sie die Komplexität Ihrer Anwendung erhöhen.</span><span class="sxs-lookup"><span data-stu-id="117fc-288">While using sub-process DPI scaling enables you to rely on Windows to do some of the DPI scaling for your application, it can increase the complexity of your application.</span></span> <span data-ttu-id="117fc-289">Es ist wichtig, dass Sie die Nachteile dieses Ansatzes und die Art der komplexen Komplexität verstehen.</span><span class="sxs-lookup"><span data-stu-id="117fc-289">It is important that you understand the drawbacks of this approach and nature of the complexities that it introduces.</span></span> <span data-ttu-id="117fc-290">Weitere Informationen zu unter Prozess-dpi-Informationen finden Sie unter die [DPI-Skalierung im gemischten Modus und die dpi-fähigen APIs.](high-dpi-improvements-for-desktop-applications.md)</span><span class="sxs-lookup"><span data-stu-id="117fc-290">For more information about sub-process DPI awareness, see [Mixed-Mode DPI Scaling and DPI-aware APIs.](high-dpi-improvements-for-desktop-applications.md)</span></span>

## <a name="testing-your-changes"></a><span data-ttu-id="117fc-291">Testen der Änderungen</span><span class="sxs-lookup"><span data-stu-id="117fc-291">Testing Your Changes</span></span>

<span data-ttu-id="117fc-292">Nachdem Sie die Anwendung so aktualisiert haben, dass Sie pro Monitor-dpi-Wert ist, ist es wichtig sicherzustellen, dass Ihre Anwendung ordnungsgemäß auf dpi-Änderungen in einer gemischten dpi-Umgebung antwortet.</span><span class="sxs-lookup"><span data-stu-id="117fc-292">After you have updated your application to become per-monitor DPI aware, it is important to validate your application properly responds to DPI changes in a mixed-DPI environment.</span></span> <span data-ttu-id="117fc-293">Zu Test enden Besonderheiten zählen:</span><span class="sxs-lookup"><span data-stu-id="117fc-293">Some specifics to test include:</span></span>

1.  <span data-ttu-id="117fc-294">Verschieben von Anwendungs Fenstern zwischen Anzeigen verschiedener dpi-Werte</span><span class="sxs-lookup"><span data-stu-id="117fc-294">Moving application windows back and forth between displays of different DPI values</span></span>
2.  <span data-ttu-id="117fc-295">Starten der Anwendung für die Anzeige verschiedener dpi-Werte</span><span class="sxs-lookup"><span data-stu-id="117fc-295">Starting your application on displays of different DPI values</span></span>
3.  <span data-ttu-id="117fc-296">Ändern des Skalierungsfaktors für den Monitor, während die Anwendung ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="117fc-296">Changing the scale factor for your monitor while the application is running</span></span>
4.  <span data-ttu-id="117fc-297">Ändern Sie die Anzeige, die Sie als primäre Anzeige verwenden, und melden Sie sich _von Windows_ ab, und testen Sie die Anwendung nach dem erneuten Anmelden erneut.</span><span class="sxs-lookup"><span data-stu-id="117fc-297">Changing the display that you use as the primary display, _signing out of Windows_, then re-testing your application after signing back in.</span></span> <span data-ttu-id="117fc-298">Dies ist besonders nützlich für die Suche nach Code, der hart codierte Größen/Dimensionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="117fc-298">This is particularly useful in finding code that uses hard-coded sizes/dimensions.</span></span>

## <a name="common-pitfalls-win32"></a><span data-ttu-id="117fc-299">Häufige Fehler (Win32)</span><span class="sxs-lookup"><span data-stu-id="117fc-299">Common Pitfalls (Win32)</span></span>

<span data-ttu-id="117fc-300">**Das vorgeschlagene Rechteck, das in WM dpichanged bereitgestellt wird, wird nicht verwendet. \_**</span><span class="sxs-lookup"><span data-stu-id="117fc-300">**Not using the suggested rectangle that is provided in WM\_DPICHANGED**</span></span>

<span data-ttu-id="117fc-301">Wenn Windows das Anwendungsfenster an eine [**WM- \_ dpichanged**](wm-dpichanged.md) -Meldung sendet, enthält diese Meldung ein empfohlenes Rechteck, das Sie zum Ändern der Größe des Fensters verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="117fc-301">When Windows sends your application window a [**WM\_DPICHANGED**](wm-dpichanged.md) message, this message includes a suggested rectangle that you should use to resize your window.</span></span> <span data-ttu-id="117fc-302">Es ist wichtig, dass Ihre Anwendung dieses Rechteck verwendet, um die Größe selbst zu ändern. Dies geschieht wie folgt:</span><span class="sxs-lookup"><span data-stu-id="117fc-302">It is critical that your application use this rectangle to resize itself, as this will:</span></span>

1.  <span data-ttu-id="117fc-303">Stellen Sie sicher, dass sich der Mauszeiger beim Ziehen zwischen den Anzeigen an derselben relativen Position im Fenster verbleibt.</span><span class="sxs-lookup"><span data-stu-id="117fc-303">Ensure that the mouse cursor will stay in the same relative position on the Window when dragging between displays</span></span>
2.  <span data-ttu-id="117fc-304">Verhindern, dass das Anwendungsfenster in einen rekursiven dpi-Änderungs-Cycle gelangt, bei dem eine dpi-Änderung eine nachfolgende dpi-Änderung auslöst, die eine andere dpi-Änderung auslöst.</span><span class="sxs-lookup"><span data-stu-id="117fc-304">Prevent the application window from getting into a recursive dpi-change cycle where one DPI change triggers a subsequent DPI change, which triggers yet another DPI change.</span></span>

<span data-ttu-id="117fc-305">Wenn Sie über anwendungsspezifische Anforderungen verfügen, die die Verwendung des vorgeschlagenen Rechtecks verhindern, das Windows in der WM \_ dpichanged-Meldung bereitstellt, finden Sie weitere Informationen unter [**WM \_ getdpiscaledsize**](wm-getdpiscaledsize.md).</span><span class="sxs-lookup"><span data-stu-id="117fc-305">If you have application-specific requirements that prevent you from using the suggested rectangle that Windows provides in the WM\_DPICHANGED message, see [**WM\_GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span></span> <span data-ttu-id="117fc-306">Diese Meldung kann verwendet werden, um Windows eine gewünschte Größe zu geben, die Sie verwenden möchten, sobald die dpi-Änderung aufgetreten ist, während die oben beschriebenen Probleme weiterhin vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="117fc-306">This message can be used to give Windows a desired size you'd like used once the DPI change has occurred, while still avoiding the issues described above.</span></span>

<span data-ttu-id="117fc-307">**Fehlende Dokumentation zur Virtualisierung**</span><span class="sxs-lookup"><span data-stu-id="117fc-307">**Lack of documentation about virtualization**</span></span>

<span data-ttu-id="117fc-308">Wenn ein HWND oder ein Prozess entweder als dpi-oder System-dpi-fähig ausgeführt wird, kann es sich um eine von Fenstern gestreckte Bitmap handeln.</span><span class="sxs-lookup"><span data-stu-id="117fc-308">When an HWND or process is running as either DPI unaware or system DPI aware, it can be bitmap stretched by Windows.</span></span> <span data-ttu-id="117fc-309">In diesem Fall skaliert und konvertiert Windows dpi-sensible Informationen von einigen APIs in den Koordinatenraum des aufrufenden Threads.</span><span class="sxs-lookup"><span data-stu-id="117fc-309">When this happens, Windows scales and converts DPI-sensitive information from some APIs to the coordinate space of the calling thread.</span></span> <span data-ttu-id="117fc-310">Wenn z. b. ein dpi-abhängiger Thread die Bildschirmgröße beim Ausführen auf einer High-dpi-Anzeige abfragt, wird die Antwort der Anwendung von Windows virtualisiert, als ob der Bildschirm in 96 dpi-Einheiten enthalten wäre.</span><span class="sxs-lookup"><span data-stu-id="117fc-310">For example, if a DPI-unaware thread queries the screen size while running on a high-DPI display, Windows will virtualize the answer given to the application as if the screen were in 96 DPI units.</span></span> <span data-ttu-id="117fc-311">Wenn ein System-dpi-fähiger Thread mit einer Anzeige auf einem anderen dpi-Wert interagiert, als beim Starten der Sitzung des aktuellen Benutzers verwendet wurde, werden von Windows möglicherweise einige API-Aufrufe in den Koordinaten Bereich, den das HWND verwenden würde, beim ursprünglichen dpi-Skalierungsfaktor von Windows in dpi skaliert.</span><span class="sxs-lookup"><span data-stu-id="117fc-311">Alternatively, when a System DPI-aware thread is interacting with a display at a different DPI than was in use when the current user's session was started, Windows will DPI-scale some API calls into the coordinate space that the HWND would be using if it were running at its original DPI scale factor.</span></span>

<span data-ttu-id="117fc-312">Wenn Sie Ihre Desktop Anwendung auf die DPI-Skalierung aktualisieren, kann es schwierig zu wissen, welche API-Aufrufe virtualisierte Werte basierend auf dem Thread Kontext zurückgeben können. Diese Informationen sind zurzeit von Microsoft nicht ausreichend dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="117fc-312">When you update your desktop application to DPI scale properly, it can difficult to know which API calls can return virtualized values based on the thread context; this information is not currently sufficiently documented by Microsoft.</span></span> <span data-ttu-id="117fc-313">Beachten Sie, dass der Rückgabewert möglicherweise virtualisiert wird, wenn Sie eine System-API von einem dpi-abhängigen oder System-DPI-fähigen Thread Kontext abrufen.</span><span class="sxs-lookup"><span data-stu-id="117fc-313">Be aware that if you call any system API from a DPI-unaware or system-DPI-aware thread context, the return value might be virtualized.</span></span> <span data-ttu-id="117fc-314">Stellen Sie daher sicher, dass der Thread im dpi-Kontext ausgeführt wird, den Sie bei der Interaktion mit dem Bildschirm oder den einzelnen Fenstern erwarten.</span><span class="sxs-lookup"><span data-stu-id="117fc-314">As such, make sure your thread is running in the DPI context you expect when interacting with the screen or individual windows.</span></span> <span data-ttu-id="117fc-315">Wenn Sie den dpi-Kontext eines Threads mithilfe von [setthreaddpiawarenesscontext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)vorübergehend ändern, stellen Sie sicher, dass Sie den alten Kontext wiederherstellen, wenn Sie fertig sind, um an anderer Stelle in der Anwendung ein falsches Verhalten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="117fc-315">When temporarily changing a thread's DPI context using [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), be sure to restore the old context when you're done to avoid causing incorrect behavior elsewhere in your application.</span></span>

<span data-ttu-id="117fc-316">**Viele Windows-APIs haben keinen dpi-Kontext.**</span><span class="sxs-lookup"><span data-stu-id="117fc-316">**Many Windows APIs do not have an DPI context**</span></span>

<span data-ttu-id="117fc-317">Viele ältere Windows-APIs enthalten keinen dpi-oder HWND-Kontext als Teil ihrer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="117fc-317">Many legacy Windows APIs do not include a DPI or HWND context as part of their interface.</span></span> <span data-ttu-id="117fc-318">Infolgedessen müssen Entwickler häufig zusätzliche Aufgaben ausführen, um die Skalierung von dpi-sensiblen Informationen, wie z. b. Größen, Punkten oder Symbolen, zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="117fc-318">As a result, developers often have to do additional work to handle the scaling of any DPI-sensitive information, such as sizes, points, or icons.</span></span> <span data-ttu-id="117fc-319">Beispielsweise müssen Entwickler, die [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) verwenden, entweder ein Stretch geladenes Symbol oder alternative APIs verwenden, um korrekte Symbole für den entsprechenden dpi-Wert (z. b. [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew)) zu laden.</span><span class="sxs-lookup"><span data-stu-id="117fc-319">As an example, developers using [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) must either bitmap stretch loaded icons or use alternate APIs to load correctly-sized icons for the appropriate DPI, such as [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span></span>

<span data-ttu-id="117fc-320">**Erzwungene zurück setzung der Prozess weiten dpi-Informationen**</span><span class="sxs-lookup"><span data-stu-id="117fc-320">**Forced reset of process-wide DPI awareness**</span></span>

<span data-ttu-id="117fc-321">Im Allgemeinen kann der dpi-Awareness-Modus des Prozesses nach der Prozess Initialisierung nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="117fc-321">In general, the DPI awareness mode of your process cannot be changed after process initialization.</span></span> <span data-ttu-id="117fc-322">Windows kann jedoch zwangsweise den dpi-Informationsmodus Ihres Prozesses ändern, wenn Sie versuchen, die Anforderung zu unterbrechen, dass alle hwnds in einer Fenster Struktur denselben dpi-Awareness-Modus aufweisen.</span><span class="sxs-lookup"><span data-stu-id="117fc-322">Windows can, however, forcibly change the DPI awareness mode of your process if you attempt to break the requirement that all HWNDs in a window tree have the same DPI awareness mode.</span></span> <span data-ttu-id="117fc-323">In allen Versionen von Windows, ab Windows 10 1703, ist es nicht möglich, verschiedene hwnds in einer HWND-Struktur in verschiedenen dpi-Bekanntheits Modi auszuführen.</span><span class="sxs-lookup"><span data-stu-id="117fc-323">On all versions of Windows, as of Windows 10 1703, it is not possible to have different HWNDs in an HWND tree run in different DPI awareness modes.</span></span> <span data-ttu-id="117fc-324">Wenn Sie versuchen, eine Beziehung zwischen untergeordneten und übergeordneten Elementen zu erstellen, die diese Regel unterbricht, kann die dpi-Bekanntheit des gesamten Prozesses zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="117fc-324">If you attempt to create a child-parent relationship that breaks this rule, the DPI awareness of the entire process can be reset.</span></span> <span data-ttu-id="117fc-325">Dies kann durch folgende Aktionen ausgelöst werden:</span><span class="sxs-lookup"><span data-stu-id="117fc-325">This can be triggered by:</span></span>

1.  <span data-ttu-id="117fc-326">Ein CreateWindow-Aufruf, bei dem das übergeordnete Fenster über einen anderen dpi-Awareness-Modus als der aufrufende Thread verfügt.</span><span class="sxs-lookup"><span data-stu-id="117fc-326">A CreateWindow call where the passed in parent window is of a different DPI awareness mode than the calling thread.</span></span>
2.  <span data-ttu-id="117fc-327">Ein SetParent-Befehl, bei dem die beiden Fenster mit unterschiedlichen dpi-Informations Modi verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="117fc-327">A SetParent call where the two windows are associated with different DPI awareness modes.</span></span>

<span data-ttu-id="117fc-328">Die folgende Tabelle zeigt, was geschieht, wenn Sie versuchen, diese Regel zu verletzen:</span><span class="sxs-lookup"><span data-stu-id="117fc-328">The table below shows what happens if you attempt to violate this rule:</span></span>



| <span data-ttu-id="117fc-329">Vorgang</span><span class="sxs-lookup"><span data-stu-id="117fc-329">Operation</span></span>                 | <span data-ttu-id="117fc-330">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="117fc-330">Windows 8.1</span></span>                                  | <span data-ttu-id="117fc-331">Windows 10 (1607 und früher)</span><span class="sxs-lookup"><span data-stu-id="117fc-331">Windows 10 (1607 and earlier)</span></span>                | <span data-ttu-id="117fc-332">Windows 10 (1703 und höher)</span><span class="sxs-lookup"><span data-stu-id="117fc-332">Windows 10 (1703 and later)</span></span>                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| <span data-ttu-id="117fc-333">Up Window (in-proc)</span><span class="sxs-lookup"><span data-stu-id="117fc-333">CreateWindow (In-Proc)</span></span>    | <span data-ttu-id="117fc-334">–</span><span class="sxs-lookup"><span data-stu-id="117fc-334">N/A</span></span>                                          | <span data-ttu-id="117fc-335">**Child erbt** (gemischter Modus)</span><span class="sxs-lookup"><span data-stu-id="117fc-335">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="117fc-336">**Child erbt** (gemischter Modus)</span><span class="sxs-lookup"><span data-stu-id="117fc-336">**Child inherits** (mixed mode)</span></span>              |
| <span data-ttu-id="117fc-337">"Kreatewindow" (Kreuz proc)</span><span class="sxs-lookup"><span data-stu-id="117fc-337">CreateWindow (Cross-Proc)</span></span> | <span data-ttu-id="117fc-338">**Erzwungene zurück** Setzung (der Prozess des Aufrufers)</span><span class="sxs-lookup"><span data-stu-id="117fc-338">**Forced reset** (of caller's process)</span></span>       | <span data-ttu-id="117fc-339">**Child erbt** (gemischter Modus)</span><span class="sxs-lookup"><span data-stu-id="117fc-339">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="117fc-340">**Erzwungene zurück** Setzung (der Prozess des Aufrufers)</span><span class="sxs-lookup"><span data-stu-id="117fc-340">**Forced reset** (of caller's process)</span></span>       |
| <span data-ttu-id="117fc-341">SetParent (in-proc)</span><span class="sxs-lookup"><span data-stu-id="117fc-341">SetParent (In-Proc)</span></span>       | <span data-ttu-id="117fc-342">–</span><span class="sxs-lookup"><span data-stu-id="117fc-342">N/A</span></span>                                          | <span data-ttu-id="117fc-343">**Erzwungene zurück** Setzung (aktueller Prozess)</span><span class="sxs-lookup"><span data-stu-id="117fc-343">**Forced reset** (of current process)</span></span>        | <span data-ttu-id="117fc-344"> Fehler ( \_ ungültiger \_ Zustand)</span><span class="sxs-lookup"><span data-stu-id="117fc-344">**Fail** (ERROR\_INVALID\_STATE)</span></span>             |
| <span data-ttu-id="117fc-345">SetParent (Cross-proc)</span><span class="sxs-lookup"><span data-stu-id="117fc-345">SetParent (Cross-Proc)</span></span>    | <span data-ttu-id="117fc-346">**Erzwungene zurück** Setzung (der Prozess des untergeordneten Fensters)</span><span class="sxs-lookup"><span data-stu-id="117fc-346">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="117fc-347">**Erzwungene zurück** Setzung (der Prozess des untergeordneten Fensters)</span><span class="sxs-lookup"><span data-stu-id="117fc-347">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="117fc-348">**Erzwungene zurück** Setzung (der Prozess des untergeordneten Fensters)</span><span class="sxs-lookup"><span data-stu-id="117fc-348">**Forced reset** (of child window's process)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="117fc-349">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="117fc-349">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="117fc-350">Hohe dpi-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="117fc-350">High DPI API Reference</span></span>](high-dpi-reference.md)
</dt> <dt>

[<span data-ttu-id="117fc-351">Dpi-Skalierungs-und dpi-kompatible APIs im gemischten Modus.</span><span class="sxs-lookup"><span data-stu-id="117fc-351">Mixed-Mode DPI Scaling and DPI-aware APIs.</span></span>](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

