---
title: Aktivieren und Steuern der DWM-Komposition
description: Die Desktopfenster-Manager (DWM)-Kompositions-APIs bieten verschiedene Funktionen zum Festlegen und Abfragen grundlegender Informationen, die von der DWM verwendet werden.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Desktopfenster-Manager (DWM), Komposition
- Dwm (Desktopfenster-Manager), Komposition
- Komposition
- Desktop Komposition
- farbliche Kennzeichnung
- Rendering außerhalb der Client Region
- Desktopfenster-Manager (DWM), farbige Farbgebung
- Dwm (Desktopfenster-Manager), farbige Farbgebung
- Desktopfenster-Manager (DWM), Rendering außerhalb der Client Region
- Dwm (Desktopfenster-Manager), Rendering außerhalb der Client Region
- Desktopfenster-Manager (DWM), Messaging
- Dwm (Desktopfenster-Manager), Messaging
- messaging
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856760"
---
# <a name="enable-and-control-dwm-composition"></a><span data-ttu-id="ce6da-116">Aktivieren und Steuern der DWM-Komposition</span><span class="sxs-lookup"><span data-stu-id="ce6da-116">Enable and control DWM composition</span></span>

<span data-ttu-id="ce6da-117">Die Desktopfenster-Manager (DWM)-Kompositions-APIs bieten verschiedene Funktionen zum Festlegen und Abfragen grundlegender Informationen, die von der DWM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce6da-117">The Desktop Window Manager (DWM) composition APIs provide several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="ce6da-118">Mit diesen APIs können Sie den Kompositions Statusabfragen und ändern.</span><span class="sxs-lookup"><span data-stu-id="ce6da-118">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="ce6da-119">Außerdem können Sie die renderinganricht Linie für verschiedene DWM-Fenster Attribute festlegen und Abfragen.</span><span class="sxs-lookup"><span data-stu-id="ce6da-119">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span>

## <a name="retrieving-colorization-information"></a><span data-ttu-id="ce6da-120">Informationen zur Farbgebung werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ce6da-120">Retrieving colorization information</span></span>

<span data-ttu-id="ce6da-121">Die Farbe des nicht-Client Bereichs eines Fensters wird durch das aktuelle System Farbschema bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ce6da-121">The color of the non-client region of a window is determined by the current system color theme.</span></span> <span data-ttu-id="ce6da-122">Der Wert für die farbliche Kennzeichnung wird über die DWM-APIs bereitgestellt, damit die Anwendung die Client Benutzeroberfläche mit dem System Farbschema abgleichen kann.</span><span class="sxs-lookup"><span data-stu-id="ce6da-122">The colorization value is provided through the DWM APIs to enable your application to match client UI with the system color theme.</span></span>

<span data-ttu-id="ce6da-123">Um auf diesen Wert für die Farbgebung zuzugreifen und die Farbänderung zu überwachen, verwenden Sie die Funktion [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) und die [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ce6da-123">To access this colorization value, and monitor the color change, use the [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) function and the [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) message.</span></span>

<span data-ttu-id="ce6da-124">In diesem Beispiel wird veranschaulicht, wie Sie die geänderte Farbe der Farbe behandeln und auf die neue Farbe zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ce6da-124">This example demonstrates how to handle the color changed message and access the new color.</span></span>

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a><span data-ttu-id="ce6da-125">Steuern des Renderings außerhalb der Client Region</span><span class="sxs-lookup"><span data-stu-id="ce6da-125">Controlling non-client region rendering</span></span>

<span data-ttu-id="ce6da-126">Zwei der visuellen Effekte, die DWM ermöglicht, sind Transparenz des nicht-Client Bereichs eines Fensters und Übergangseffekte.</span><span class="sxs-lookup"><span data-stu-id="ce6da-126">Two of the visual effects that DWM enables are transparency of the non-client region of a window, and transition effects.</span></span> <span data-ttu-id="ce6da-127">Möglicherweise muss Ihre Anwendung diese Effekte aus Formatierungs-oder Kompatibilitätsgründen deaktivieren oder erneut aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ce6da-127">Your application might have to disable or re-enable these effects for styling or compatibility reasons.</span></span> <span data-ttu-id="ce6da-128">Die folgenden Funktionen werden verwendet, um Transparenz und das Verhalten des Übergangs Effekts zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ce6da-128">The following functions are used to manage transparency and transition effect behavior.</span></span>

- [<span data-ttu-id="ce6da-129">**DwmGetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="ce6da-129">**DwmGetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [<span data-ttu-id="ce6da-130">**DwmSetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="ce6da-130">**DwmSetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

<span data-ttu-id="ce6da-131">Rufen Sie zum Abrufen des aktuellen nicht-Client-Renderingzustands für das Fenster einer Anwendung [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) auf, wobei *dwattribute* auf [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ce6da-131">To retrieve the current non-client rendering state for an application's window, call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with *dwAttribute* set to [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span></span> <span data-ttu-id="ce6da-132">Wie Sie in der Dokumentation für [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)sehen können, ist der abgerufene Attribut Wert, wenn Sie dieses Flag an **DwmGetWindowAttribute** übergeben, vom Typ **bool**.</span><span class="sxs-lookup"><span data-stu-id="ce6da-132">As you can see from the documentation for [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), when you pass that flag to **DwmGetWindowAttribute**, the retrieved attribute value is of type **BOOL**.</span></span> <span data-ttu-id="ce6da-133">Verschiedene Flags bewirken, dass **DwmGetWindowAttribute** Werte unterschiedlicher Typen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ce6da-133">Different flags cause **DwmGetWindowAttribute** to return values of different types.</span></span> <span data-ttu-id="ce6da-134">Hier sehen Sie ein Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="ce6da-134">Here's a code example.</span></span>

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

<span data-ttu-id="ce6da-135">Im nächsten Beispiel wird gezeigt, wie das [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) -Flag mit **DwmGetWindowAttribute** verwendet wird, um das erweiterte Rahmen Rahmen-Rechteck eines Fensters abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ce6da-135">This next example shows how to use the [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag with **DwmGetWindowAttribute** to retrieve the extended frame bounds rectangle of a window.</span></span> <span data-ttu-id="ce6da-136">Die Dokumentation für dieses Flag gibt an, dass der abgerufene Attribut Wert vom Typ " **Rect**" ist.</span><span class="sxs-lookup"><span data-stu-id="ce6da-136">The documentation for that flag tells us that the retrieved attribute value is of type **RECT**.</span></span>

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> <span data-ttu-id="ce6da-137">Befolgen Sie das oben gezeigte Programmier Muster, wenn Sie [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) mit Flags für verschiedene Attribute aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ce6da-137">Follow the same programming pattern shown above when you call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with flags for different attributes.</span></span> <span data-ttu-id="ce6da-138">Das Thema [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) -Enumeration gibt an, welcher Werttyp, auf den Sie einen Zeiger im *pvattribute* -Parameter für **DwmGetWindowAttribute** übergeben sollten, in der Zeile für jedes Flag.</span><span class="sxs-lookup"><span data-stu-id="ce6da-138">The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter for **DwmGetWindowAttribute**.</span></span> <span data-ttu-id="ce6da-139">Der *cbattribute* -Parameter enthält die Größe dieses Objekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ce6da-139">The *cbAttribute* parameter contains the size, in bytes, of that object.</span></span>

<span data-ttu-id="ce6da-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) ermöglicht der Anwendung das Festlegen der nicht-Client Bereichs-renderinganricht Linie.</span><span class="sxs-lookup"><span data-stu-id="ce6da-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) enables your application to set the non-client area rendering policy.</span></span> <span data-ttu-id="ce6da-141">Diese Funktion bestimmt auch, wie die Anwendung DWM-Übergangseffekte behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="ce6da-141">That function also determines how your application should handle DWM transition effects.</span></span>

<span data-ttu-id="ce6da-142">Im nächsten Beispiel wird das Rendering außerhalb des Client Bereichs deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ce6da-142">This next example disables non-client area rendering.</span></span> <span data-ttu-id="ce6da-143">Dies bewirkt, dass alle vorherigen Aufrufe von [dwmenableblurabledwindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) oder [dwmextendframeindeclientarea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ce6da-143">This causes any previous calls to [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) or to [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to be disabled.</span></span>

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

<span data-ttu-id="ce6da-144">Neben der Steuerung des nicht-Client Bereichs Rendering kann [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) auch DWM-Übergangseffekte steuern.</span><span class="sxs-lookup"><span data-stu-id="ce6da-144">In addition to controlling the non-client area rendering, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) can also control DWM transition effects.</span></span> <span data-ttu-id="ce6da-145">Sie können das Übergangs Verhalten mithilfe von **dwmwa-über \_ Gängen \_ forcedeaktiviert** als *dwattribute* -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce6da-145">You can set transition behavior by using **DWMWA\_TRANSITIONS\_FORCEDISABLED** as the *dwAttribute* parameter.</span></span>

## <a name="messages"></a><span data-ttu-id="ce6da-146">Meldungen</span><span class="sxs-lookup"><span data-stu-id="ce6da-146">Messages</span></span>

<span data-ttu-id="ce6da-147">Die folgenden Meldungen enthalten eine Benachrichtigung über DWM-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ce6da-147">The following messages provide notification of DWM events.</span></span> <span data-ttu-id="ce6da-148">Diese Nachrichten können zum Überwachen von Änderungen verwendet werden, z. b. Änderungen des Kompositions Status und Änderungen am System Farbdesign.</span><span class="sxs-lookup"><span data-stu-id="ce6da-148">These messages can be used to monitor changes such as composition state changes and system color theme changes.</span></span>

- [<span data-ttu-id="ce6da-149">**WM \_ dwmcolorizationcolorchanged**</span><span class="sxs-lookup"><span data-stu-id="ce6da-149">**WM\_DWMCOLORIZATIONCOLORCHANGED**</span></span>](wm-dwmcolorizationcolorchanged.md)
- [<span data-ttu-id="ce6da-150">**WM \_ dwmcompositionchanged**</span><span class="sxs-lookup"><span data-stu-id="ce6da-150">**WM\_DWMCOMPOSITIONCHANGED**</span></span>](wm-dwmcompositionchanged.md)
- [<span data-ttu-id="ce6da-151">**WM \_ dwmncrenderingchanged**</span><span class="sxs-lookup"><span data-stu-id="ce6da-151">**WM\_DWMNCRENDERINGCHANGED**</span></span>](wm-dwmncrenderingchanged.md)
- [<span data-ttu-id="ce6da-152">**WM \_ dwmwindowmaximizedchange**</span><span class="sxs-lookup"><span data-stu-id="ce6da-152">**WM\_DWMWINDOWMAXIMIZEDCHANGE**</span></span>](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a><span data-ttu-id="ce6da-153">Deaktivieren der DWM-Komposition (Windows 7 und früher)</span><span class="sxs-lookup"><span data-stu-id="ce6da-153">Disabling DWM composition (Windows 7 and earlier)</span></span>

> [!WARNING]
> <span data-ttu-id="ce6da-154">Die Informationen in diesem Abschnitt gelten nur für Windows 7 und frühere Systeme.</span><span class="sxs-lookup"><span data-stu-id="ce6da-154">The info in this section applies only to Windows 7 and earlier systems.</span></span>

<span data-ttu-id="ce6da-155">Da DWM die GPU (Graphics Processing Unit) für die Desktop Komposition verwendet, muss Ihre Anwendung DWM möglicherweise auf Kompatibilität deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ce6da-155">Because DWM uses the graphics processing unit (GPU) for desktop composition, your application might have to disable DWM for compatibility.</span></span> <span data-ttu-id="ce6da-156">Anwendungen, die die vollständige Kontrolle über den Desktop übernehmen, z. b. Spiele, die im Vollbildmodus ausgeführt werden, müssen bestimmen, ob die DWM aktiviert ist. ist dies der Fall, deaktivieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="ce6da-156">Applications that take full control of the desktop, such as games that run in full-screen mode, must determine whether the DWM is enabled and if it is, disable it.</span></span> <span data-ttu-id="ce6da-157">Zu diesem Zweck werden zwei Funktionen benötigt.</span><span class="sxs-lookup"><span data-stu-id="ce6da-157">To do this, two functions are needed.</span></span>

- [<span data-ttu-id="ce6da-158">**DwmIsCompositionEnabled**</span><span class="sxs-lookup"><span data-stu-id="ce6da-158">**DwmIsCompositionEnabled**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [<span data-ttu-id="ce6da-159">**DwmEnableComposition**</span><span class="sxs-lookup"><span data-stu-id="ce6da-159">**DwmEnableComposition**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

<span data-ttu-id="ce6da-160">Ein Aufruf von [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) , bei dem " *fEnable* " auf **DWM \_ EC " \_ disablecomposition** " festgelegt ist, deaktiviert die DWM-Komposition, bis der aufrufende Prozess beendet wurde oder die Komposition durch Aufrufen von " **DwmEnableComposition** " mit " *fEnable* " auf " **DWM \_ EC \_ enablecomposition**" erneut aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="ce6da-160">A call to [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) with *fEnable* set to **DWM\_EC\_DISABLECOMPOSITION** disables DWM composition until either the calling process has shut down, or composition has been re-enabled by calling **DwmEnableComposition** with *fEnable* set to **DWM\_EC\_ENABLECOMPOSITION**.</span></span> <span data-ttu-id="ce6da-161">Die DWM-Komposition wird automatisch neu gestartet, sobald alle Anwendungen, die die Komposition deaktiviert haben, die Komposition durch Aufrufen von **DwmEnableComposition** entweder heruntergefahren oder manuell erneut aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="ce6da-161">DWM composition restarts automatically as soon as all applications that have disabled composition have either shut down or have manually re-enabled composition by calling **DwmEnableComposition**.</span></span>

> [!NOTE]  
> <span data-ttu-id="ce6da-162">Die DWM deaktiviert die Komposition automatisch, wenn eine Anwendung versucht, direkt zur primären Anzeige Oberfläche zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ce6da-162">The DWM automatically disables composition when an application attempts to draw directly to the primary display surface.</span></span> <span data-ttu-id="ce6da-163">Die Komposition wird deaktiviert, bis die primäre Geräteoberfläche von der Anwendung freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce6da-163">Composition will be disabled until the primary device surface is released by that application.</span></span>
