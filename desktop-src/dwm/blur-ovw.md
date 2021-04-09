---
title: DWM-weich hinter Übersicht
description: Eine der DWM-Effekte (Signature Desktopfenster-Manager) ist ein durchlässiges und verschwommene nicht-Client-Bereich. Mithilfe der DWM-APIs können Anwendungen diese Effekte auf den Client Bereich ihrer Fenster der obersten Ebene anwenden.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Desktopfenster-Manager (DWM), weich/Behind-Effekt
- Dwm (Desktopfenster-Manager), weich-Behind-Effekt
- weich-Behind-Effekt
- durchlässiges wirken
- transparenter Glas Effekt
- Desktopfenster-Manager (DWM), durchlässigem Effekt
- Dwm (Desktopfenster-Manager), durchscheinend
- Desktopfenster-Manager (DWM), transparenter Glas Effekt
- Dwm (Desktopfenster-Manager), transparenter Glas Effekt
- Desktopfenster-Manager (DWM), Erweitern des Fensterrahmens in den Client Bereich
- Dwm (Desktopfenster-Manager), Erweitern des Fensterrahmens in den Client Bereich
- Erweitern des Fensterrahmens in den Client Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039505"
---
# <a name="dwm-blur-behind-overview"></a><span data-ttu-id="948f6-116">DWM-weich hinter Übersicht</span><span class="sxs-lookup"><span data-stu-id="948f6-116">DWM Blur Behind Overview</span></span>

<span data-ttu-id="948f6-117">Eine der DWM-Effekte (Signature Desktopfenster-Manager) ist ein durchlässiges und verschwommene nicht-Client-Bereich.</span><span class="sxs-lookup"><span data-stu-id="948f6-117">One of the signature Desktop Window Manager (DWM) effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="948f6-118">Mithilfe der DWM-APIs können Anwendungen diese Effekte auf den Client Bereich ihrer Fenster der obersten Ebene anwenden.</span><span class="sxs-lookup"><span data-stu-id="948f6-118">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span>

> [!Note]  
> <span data-ttu-id="948f6-119">Windows Vista Home Basic Edition unterstützt den transparenten Glas Effekt nicht.</span><span class="sxs-lookup"><span data-stu-id="948f6-119">Windows Vista Home Basic edition does not support the transparent glass effect.</span></span> <span data-ttu-id="948f6-120">Bereiche, die in der Regel mit dem transparenten Glas Effekt in anderen Windows-Editionen gerendert werden, werden als nicht transparent dargestellt.</span><span class="sxs-lookup"><span data-stu-id="948f6-120">Areas that would typically render with the transparent glass effect on other Windows editions are rendered as opaque.</span></span>
> <span data-ttu-id="948f6-121">Beginnend mit Windows 8 führt das Aufrufen dieser Funktion nicht zu einem Weichzeichnereffekt aufgrund einer Stiländerung in der Art und Weise, in der Fenster gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="948f6-121">Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>


 

<span data-ttu-id="948f6-122">In diesem Thema werden die folgenden Client-Behind-Behind-Szenarien erläutert, die die DWM ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="948f6-122">This topic discusses the following client blur-behind scenarios that the DWM enables.</span></span>

-   [<span data-ttu-id="948f6-123">Hinzufügen von Unschärfe zu einem bestimmten Bereich des Client Bereichs</span><span class="sxs-lookup"><span data-stu-id="948f6-123">Adding Blur to a Specific Region of the Client Area</span></span>](#adding-blur-to-a-specific-region-of-the-client-area)
-   [<span data-ttu-id="948f6-124">Erweitern des Fensterrahmens in den Client Bereich</span><span class="sxs-lookup"><span data-stu-id="948f6-124">Extending the Window Frame into the Client Area</span></span>](#extending-the-window-frame-into-the-client-area)
-   [<span data-ttu-id="948f6-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="948f6-125">Related topics</span></span>](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a><span data-ttu-id="948f6-126">Hinzufügen von Unschärfe zu einem bestimmten Bereich des Client Bereichs</span><span class="sxs-lookup"><span data-stu-id="948f6-126">Adding Blur to a Specific Region of the Client Area</span></span>

<span data-ttu-id="948f6-127">Eine Anwendung kann den Weichzeichnereffekt hinter dem gesamten Client Bereich des Fensters oder auf eine bestimmte Unterregion anwenden.</span><span class="sxs-lookup"><span data-stu-id="948f6-127">An application can apply the blur effect behind the whole client region of the window or to a specific subregion.</span></span> <span data-ttu-id="948f6-128">Dadurch können Anwendungen formatierte Pfade und Suchleisten hinzufügen, die visuell vom Rest der Anwendung getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="948f6-128">This enables applications to add styled path and search bars that are visually separate from the rest of the application.</span></span>

<span data-ttu-id="948f6-129">Bei der in diesem Szenario verwendeten API handelt es sich um die [**dwmenableblurabledwindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) -Funktion, die die DWM-weich- [**hinter Konstanten**](dwm-bb-constants.md) und die [**DWM- \_ blurbehind**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) -Struktur nutzt.</span><span class="sxs-lookup"><span data-stu-id="948f6-129">The API used in this scenario is the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function, which makes use of the [**DWM Blur Behind Constants**](dwm-bb-constants.md) and the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure.</span></span>

<span data-ttu-id="948f6-130">Die folgende Beispiel Funktion, `EnableBlurBehind` , veranschaulicht, wie der weich-Behind-Effekt auf das gesamte Fenster angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="948f6-130">The following example function, `EnableBlurBehind`, illustrates how to apply the blur-behind effect to the whole window.</span></span>


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="948f6-131">Beachten Sie, dass **null** im *hRgnBlur* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="948f6-131">Note that **NULL** is specified in the *hRgnBlur* parameter.</span></span> <span data-ttu-id="948f6-132">Dadurch wird der DWM mitgeteilt, dass der Weichzeichner hinter dem gesamten Fenster angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="948f6-132">This tells the DWM to apply the blur behind the whole window.</span></span>

<span data-ttu-id="948f6-133">In der folgenden Abbildung wird der auf das gesamte Fenster angewendete weich-Behind-Effekt veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="948f6-133">The following image illustrates the blur-behind effect applied to the whole window.</span></span>

![der auf ein Fenster angewendete weich-Behind-Effekt](images/dwm-blurbehindwindow.png)

<span data-ttu-id="948f6-135">Wenn Sie den weich Zeichen hinter einer Unterregion anwenden möchten, wenden Sie ein gültiges Regions handle (hrgn) auf den **hRgnBlur** -Member der [**DWM- \_ blurbehind**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) -Struktur an, und fügen Sie dem **dwFlags** -Member das Flag **DWM \_ BB \_ blurregion** hinzu.</span><span class="sxs-lookup"><span data-stu-id="948f6-135">To apply the blur behind a subregion, apply a valid region handle (HRGN) to the **hRgnBlur** member of the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure and add the **DWM\_BB\_BLURREGION** flag to the **dwFlags** member.</span></span>

<span data-ttu-id="948f6-136">Wenn Sie den weich-Behind-Effekt auf einen Teilbereich des Fensters anwenden, wird der Alphakanal des Fensters für den nicht unscharfen Bereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="948f6-136">When you apply the blur-behind effect to a subregion of the window, the alpha channel of the window is used for the nonblurred area.</span></span> <span data-ttu-id="948f6-137">Dies kann zu einer unerwarteten Transparenz im nicht unscharfen Bereich eines Fensters führen.</span><span class="sxs-lookup"><span data-stu-id="948f6-137">This can cause an unexpected transparency in the nonblurred region of a window.</span></span> <span data-ttu-id="948f6-138">Gehen Sie daher vorsichtig vor, wenn Sie einen Weichzeichnereffekt auf eine Unterregion anwenden.</span><span class="sxs-lookup"><span data-stu-id="948f6-138">Therefore, be careful when you apply a blur effect to a subregion.</span></span>

## <a name="extending-the-window-frame-into-the-client-area"></a><span data-ttu-id="948f6-139">Erweitern des Fensterrahmens in den Client Bereich</span><span class="sxs-lookup"><span data-stu-id="948f6-139">Extending the Window Frame into the Client Area</span></span>

<span data-ttu-id="948f6-140">Eine Anwendung kann die weich Zeichnung des Fensterrahmens auf den Client Bereich ausdehnen.</span><span class="sxs-lookup"><span data-stu-id="948f6-140">An application can extend the blur of the window frame into the client area.</span></span> <span data-ttu-id="948f6-141">Dies ist hilfreich, wenn Sie den Weichzeichnereffekt hinter einem Fenster mit einer angedockten Symbolleiste oder visuell getrennte Steuerelemente vom Rest einer Anwendung anwenden.</span><span class="sxs-lookup"><span data-stu-id="948f6-141">This is useful when you apply the blur effect behind a window with a docked toolbar or visually separate controls from the rest of an application.</span></span> <span data-ttu-id="948f6-142">Diese Funktionalität wird von der Funktion " [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) " verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="948f6-142">This functionality is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span>

<span data-ttu-id="948f6-143">Verwenden Sie zum Aktivieren von weich Zeichen mithilfe von [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)die [**Ränder**](/windows/win32/api/uxtheme/ns-uxtheme-margins) -Struktur, um anzugeben, wie viel in den Client Bereich erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="948f6-143">To enable blur by using [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use the [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) structure to indicate how much to extend into the client area.</span></span> <span data-ttu-id="948f6-144">Die folgende Beispiel Funktion, `ExtendIntoClientBottom` , schaltet die weichzeichnerweiterung unten im nicht-Client-Frame in den Client Bereich um.</span><span class="sxs-lookup"><span data-stu-id="948f6-144">The following example function, `ExtendIntoClientBottom`, toggles the blur extension on the bottom of the non-client frame into the client area.</span></span>


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="948f6-145">In der folgenden Abbildung ist der weich-Behind-Effekt dargestellt, der auf den unteren Rand des Client Bereichs erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="948f6-145">The following image illustrates the blur-behind effect extended into the bottom of the client area.</span></span>

![Bild, das den weich Zeichen-Behind-Effekt anzeigt, der zum unteren Rand eines Client Bereichs erweitert wurde](images/dwm-extendedbottom.png)

<span data-ttu-id="948f6-147">Auch über die [**dwmextendframeinesclientarea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) -Methode verfügbar, ist das "Sheet of Glass"-Effekt, bei dem der Weichzeichnereffekt auf die gesamte Oberfläche des Fensters ohne einen sichtbaren Fensterrahmen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="948f6-147">Also available through the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) method is the "sheet of glass" effect, where the blur effect is applied to the whole surface of the window without a visible window border.</span></span> <span data-ttu-id="948f6-148">Im folgenden Beispiel wird dieser Effekt veranschaulicht, bei dem der Client Bereich ohne Fensterrahmen gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="948f6-148">The following example demonstrates this effect where the client area is rendered without a window border.</span></span>


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="948f6-149">In der folgenden Abbildung ist der weich-Behind im Fenster Stil "Sheet of Glass" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="948f6-149">The following image illustrates the blur-behind in the "sheet of glass" window style.</span></span>

![Bild, das den weich Zeichnungs Effekt im Fenster Stil "Glas Blatt" veranschaulicht](images/dwm-sheetofglass.png)

## <a name="related-topics"></a><span data-ttu-id="948f6-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="948f6-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="948f6-152">Übersicht über Desktop Window Manager</span><span class="sxs-lookup"><span data-stu-id="948f6-152">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="948f6-153">Enable and Control DWM Composition (Aktivieren und Steuern der DWM-Komposition)</span><span class="sxs-lookup"><span data-stu-id="948f6-153">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="948f6-154">Überlegungen zur Leistung und bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="948f6-154">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 