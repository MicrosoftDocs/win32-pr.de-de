---
title: Verwenden visueller Stile mit benutzerdefinierten Steuerelementen und Owner-Drawn Steuerelementen
description: In diesem Thema wird beschrieben, wie die API für visuelle Stile verwendet wird, um visuelle Stile auf benutzerdefinierte Steuerelemente oder vom Besitzer gezeichnete Steuerelemente anzuwenden.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102435"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a><span data-ttu-id="64dd3-103">Verwenden visueller Stile mit benutzerdefinierten Steuerelementen und Owner-Drawn Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="64dd3-103">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>

<span data-ttu-id="64dd3-104">In diesem Thema wird beschrieben, wie die API für visuelle Stile verwendet wird, um visuelle Stile auf benutzerdefinierte Steuerelemente oder vom Besitzer gezeichnete Steuerelemente anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="64dd3-104">This topic describes how to use the visual styles API to apply visual styles to custom controls or owner-drawn controls.</span></span>

-   [<span data-ttu-id="64dd3-105">Zeichnen von Steuerelementen mit visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="64dd3-105">Drawing Controls with Visual Styles</span></span>](#drawing-controls-with-visual-styles)
-   [<span data-ttu-id="64dd3-106">Reagieren auf Designänderungen</span><span class="sxs-lookup"><span data-stu-id="64dd3-106">Responding to Theme Changes</span></span>](#responding-to-theme-changes)
-   [<span data-ttu-id="64dd3-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64dd3-107">Related topics</span></span>](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a><span data-ttu-id="64dd3-108">Zeichnen von Steuerelementen mit visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="64dd3-108">Drawing Controls with Visual Styles</span></span>

<span data-ttu-id="64dd3-109">Visuelle Stile werden von ComCtrl32.dll Version 6 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64dd3-109">Visual styles are supported by ComCtrl32.dll version 6 and later.</span></span> <span data-ttu-id="64dd3-110">Wenn Ihre Anwendung für die Verwendung von ComCtrl32.dll Version 6 und höher konfiguriert ist und diese Version auf dem System verfügbar ist, werden die aktuellen visuellen Stile automatisch auf alle allgemeinen Steuerelemente in Ihrer Anwendung angewendet.</span><span class="sxs-lookup"><span data-stu-id="64dd3-110">If your application is configured to use ComCtrl32.dll version 6 and later, and if that version is available on the system, the current visual styles are automatically applied to all common controls in your application.</span></span> <span data-ttu-id="64dd3-111">Die aktuellen visuellen Stile werden jedoch nicht automatisch auf benutzerdefinierte Steuerelemente oder Steuerelemente angewendet, die vom Besitzer gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="64dd3-111">However, the current visual styles are not automatically applied to custom controls or owner-drawn controls.</span></span> <span data-ttu-id="64dd3-112">Die Anwendung muss Code einschließen, mit dem überprüft wird, ob visuelle Stile verfügbar sind. wenn dies der Fall ist, wird die API für visuelle Stile verwendet, um die aktuell ausgewählten visuellen Stile auf die benutzerdefinierten und vom Besitzer gezeichneten Steuerelemente anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="64dd3-112">Your application must include code that checks whether visual styles are available and, if so, uses the visual styles API to apply the currently selected visual styles to your custom and owner-drawn controls.</span></span>

<span data-ttu-id="64dd3-113">Um zu überprüfen, ob visuelle Stile verfügbar sind, rufen Sie die [**isapptheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="64dd3-113">To check whether visual styles are available, call the [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) function.</span></span> <span data-ttu-id="64dd3-114">Wenn visuelle Stile nicht verfügbar sind, verwenden Sie den Fall Back Code, um das Steuerelement zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-114">If visual styles are not available, use fallback code to draw the control.</span></span>

<span data-ttu-id="64dd3-115">Wenn visuelle Stile verfügbar sind, können Sie Funktionen mit visuellen Stilen wie [**drawdermetext**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) zum Rendering des Steuer Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="64dd3-115">If visual styles are available, you can use visual-styles functions such as [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) to render your control.</span></span> <span data-ttu-id="64dd3-116">Beachten Sie, dass mit [**drawdermetextex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) die Darstellung von Text angepasst werden kann, wobei einige Eigenschaften der Design Schriftart beibehalten werden, während andere geändert werden.</span><span class="sxs-lookup"><span data-stu-id="64dd3-116">Note that [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) enables you to customize the appearance of text, retaining some properties of the theme font while modifying others.</span></span>

<span data-ttu-id="64dd3-117">**So zeichnen Sie ein Steuerelement im aktuellen visuellen Stil**</span><span class="sxs-lookup"><span data-stu-id="64dd3-117">**To draw a control in the current visual style**</span></span>

1.  <span data-ttu-id="64dd3-118">Nennen Sie [**openfomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), und übergeben Sie das *HWND* des Steuer Elements, auf das Sie visuelle Stile anwenden möchten, und eine Klassenliste, die den Typ des Steuer Elements beschreibt.</span><span class="sxs-lookup"><span data-stu-id="64dd3-118">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passing the *hwnd* of the control you want to apply visual styles to and a class list that describes the control's type.</span></span> <span data-ttu-id="64dd3-119">Die Klassen werden in Vssym32. h definiert.</span><span class="sxs-lookup"><span data-stu-id="64dd3-119">The classes are defined in Vssym32.h.</span></span> <span data-ttu-id="64dd3-120">**Opendermedata** gibt ein HTHEME-Handle zurück, aber wenn der Visual Styles-Manager deaktiviert ist oder der aktuelle visuelle Stil keine spezifischen Informationen für ein bestimmtes Steuerelement bereitstellt, gibt die Funktion **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="64dd3-120">**OpenThemeData** returns an HTHEME handle, but if the visual styles manager is disabled or the current visual style does not supply specific information for a given control, the function returns **NULL**.</span></span> <span data-ttu-id="64dd3-121">Wenn der Rückgabewert **null** ist, verwenden Sie nicht visuelle Stile für Zeichnungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-121">If the return value is **NULL**, use non-visual-styles drawing functions.</span></span>
2.  <span data-ttu-id="64dd3-122">Um den Hintergrund des Steuer Elements zu zeichnen, müssen Sie [**drawtemebackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) oder [**drawtemebackgroundex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-122">To draw the control background, call [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) or [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span></span>
3.  <span data-ttu-id="64dd3-123">Um den Speicherort des Inhalts Rechtecks zu ermitteln, müssen Sie [**gettemebackgroundcontentrect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-123">To determine the location of the content rectangle, call [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span>
4.  <span data-ttu-id="64dd3-124">Verwenden Sie zum Rendering von Text entweder [**drawtemetext**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) oder [**drawtemetextex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), und verwenden Sie dabei die Koordinaten des Rechtecks, das von [**gettemebackgroundcontentrect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="64dd3-124">To render text, use either [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) or [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basing the coordinates on the rectangle returned by [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span> <span data-ttu-id="64dd3-125">Diese Funktionen können den Text entweder in der Schriftart des Designs für einen angegebenen Steuerelement Teil und-Zustand oder in der derzeit im Gerätekontext (DC) ausgewählten Schriftart darstellen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-125">These functions can render text either in the theme's font for a specified control part and state, or in the font currently selected into the device context (DC).</span></span>
5.  <span data-ttu-id="64dd3-126">Wenn das Steuerelement eine [**WM- \_ zerstörungsnachricht**](/windows/desktop/winmsg/wm-destroy) empfängt, können Sie [**closefomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) aufrufen, um das Design Handle freizugeben, das beim Aufrufen von [**openfomedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="64dd3-126">When your control receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to release the theme handle that was returned when you called [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="64dd3-127">Der folgende Beispielcode zeigt eine Möglichkeit, ein Schaltflächen-Steuerelement im aktuellen visuellen Stil zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-127">The following example code demonstrates one way to draw a button control in the current visual style.</span></span>


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





<span data-ttu-id="64dd3-128">Der folgende Beispielcode befindet sich im [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldungs Handler für ein untergeordnetes Schaltflächen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="64dd3-128">The following example code is in the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message handler for a subclassed button control.</span></span> <span data-ttu-id="64dd3-129">Der Text für das Steuerelement wird in der Schriftart der visuellen Stile gezeichnet, aber die Farbe ist abhängig vom Zustand des Steuer Elements Anwendungs definiert.</span><span class="sxs-lookup"><span data-stu-id="64dd3-129">The text for the control is drawn in the visual styles font, but the color is application-defined depending on the state of the control.</span></span>


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



<span data-ttu-id="64dd3-130">Sie können Teile aus anderen Steuerelementen verwenden und die einzelnen Teile separat darstellen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-130">You can use parts from other controls and render each part separately.</span></span> <span data-ttu-id="64dd3-131">Beispielsweise können Sie für ein Kalender Steuerelement, das aus einem Raster besteht, jedes quadratische, das durch das Raster gebildet wird, als Symbolleisten-Schaltfläche behandeln, indem Sie das Design handle wie folgt abrufen:</span><span class="sxs-lookup"><span data-stu-id="64dd3-131">For example, for a calendar control that consists of a grid, you can treat each square formed by the grid as a toolbar button, by obtaining the theme handle as follows:</span></span>


```C++
OpenThemeData(hwnd, L"Toolbar");
```



<span data-ttu-id="64dd3-132">Sie können Steuerelemente mischen und abgleichen, indem Sie [**opentemedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) mehrmals für ein bestimmtes Steuerelement aufrufen und den entsprechenden Design Handle verwenden, um verschiedene Teile zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-132">You can mix and match control parts by calling [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) multiple times for a given control and using the appropriate theme handle to draw different parts.</span></span> <span data-ttu-id="64dd3-133">In einigen visuellen Stilen sind bestimmte Teile jedoch möglicherweise nicht mit anderen Teilen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="64dd3-133">In some visual styles, however, certain parts might not be compatible with other parts.</span></span>

<span data-ttu-id="64dd3-134">Ein weiterer Ansatz zum Rendern von Steuerelementen im aktiven visuellen Stil besteht darin, die Systemfarben zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="64dd3-134">Another approach to rendering controls in the active visual style is to use the system colors.</span></span> <span data-ttu-id="64dd3-135">Sie können z. b. Systemfarben verwenden, um die Textfarbe beim Aufrufen der [**drawtemetextex**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) -Funktion festzulegen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-135">For example, you can use system colors to set the text color when calling the [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="64dd3-136">Die meisten Systemfarben werden festgelegt, wenn eine visuelle Stil Datei angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="64dd3-136">Most system colors are set when a visual style file is applied.</span></span>

## <a name="responding-to-theme-changes"></a><span data-ttu-id="64dd3-137">Reagieren auf Designänderungen</span><span class="sxs-lookup"><span data-stu-id="64dd3-137">Responding to Theme Changes</span></span>

<span data-ttu-id="64dd3-138">Wenn das Steuerelement eine [**WM \_**](/windows/desktop/winmsg/wm-themechanged) -Nachricht empfängt und ein globales Handle für das Design enthält, sollte es wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="64dd3-138">When your control receives a [**WM\_THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) message and is holding a global handle to the theme, it should do the following:</span></span>

-   <span data-ttu-id="64dd3-139">Ruft [**closedermedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) auf, um das vorhandene Design Handle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-139">Call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to close the existing theme handle.</span></span>
-   <span data-ttu-id="64dd3-140">[**Öffnen Sie opentemedata**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) , um das Design Handle für den neu geladenen visuellen Stil abzurufen.</span><span class="sxs-lookup"><span data-stu-id="64dd3-140">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) to get the theme handle to the newly loaded visual style.</span></span>

<span data-ttu-id="64dd3-141">Im folgenden Beispiel werden die beiden-Aufrufe veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="64dd3-141">The following example illustrates the two calls.</span></span>


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a><span data-ttu-id="64dd3-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64dd3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64dd3-143">Aktivieren von visuellen Stilen</span><span class="sxs-lookup"><span data-stu-id="64dd3-143">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="64dd3-144">Visuelle Stile</span><span class="sxs-lookup"><span data-stu-id="64dd3-144">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 