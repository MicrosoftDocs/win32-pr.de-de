---
title: Flache Bildlaufleisten
description: Microsoft Internet Explorer 4.0 hat eine neue visuelle Technologie eingeführt, die als flache Scrollleisten bezeichnet wird.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423890"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="8475d-103">Flache Bildlaufleisten</span><span class="sxs-lookup"><span data-stu-id="8475d-103">Flat Scroll Bars</span></span>

<span data-ttu-id="8475d-104">Microsoft Internet Explorer 4.0 hat eine neue visuelle Technologie eingeführt, die als flache Scrollleisten bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="8475d-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="8475d-105">Funktionell verhalten sich flache Bildlaufleisten genauso wie Standard-Scrollleisten.</span><span class="sxs-lookup"><span data-stu-id="8475d-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="8475d-106">Der Unterschied besteht darin, dass Sie deren Darstellung in größerem Umfang als standard-Scrollleisten anpassen können.</span><span class="sxs-lookup"><span data-stu-id="8475d-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="8475d-107">Die folgende Abbildung zeigt ein Fenster, das eine flache Scrollleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="8475d-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![Screenshot eines Fensters, das eine flache Scrollleiste enthält](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="8475d-109">Flache Scrollleisten werden von Comctl32.dll Versionen 4.71 bis 5.82 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8475d-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="8475d-110">Comctl32.dll Versionen 6.00 und höher unterstützen keine flachen Bildlaufleisten.</span><span class="sxs-lookup"><span data-stu-id="8475d-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="8475d-111">Verwenden von flachen Bildlaufleisten</span><span class="sxs-lookup"><span data-stu-id="8475d-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="8475d-112">In diesem Abschnitt wird beschrieben, wie Sie flache Scrollleisten in Ihrer Anwendung implementieren.</span><span class="sxs-lookup"><span data-stu-id="8475d-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="8475d-113">Vorbereitungen</span><span class="sxs-lookup"><span data-stu-id="8475d-113">Before You Begin</span></span>

<span data-ttu-id="8475d-114">Um die flachen Scrollleistenfunktionen zu verwenden, müssen Sie Commctrl.h in Ihre Quelldateien einschließen und eine Verknüpfung mit Comctl32.lib erstellen.</span><span class="sxs-lookup"><span data-stu-id="8475d-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="8475d-115">Hinzufügen von flachen Bildlaufleisten zu einem Fenster</span><span class="sxs-lookup"><span data-stu-id="8475d-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="8475d-116">Um einem Fenster flache Scrollleisten hinzuzufügen, rufen [**Sie InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)auf und übergeben das Handle an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="8475d-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="8475d-117">Anstatt die standardmäßigen Scrollleistenfunktionen zum Bearbeiten ihrer Scrollleisten zu verwenden, müssen Sie die entsprechende FlatSB \_ XXX-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="8475d-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="8475d-118">Es gibt flache Scrollleistenfunktionen zum Festlegen und Abrufen der Scrollinformationen, des Bereichs und der Position.</span><span class="sxs-lookup"><span data-stu-id="8475d-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="8475d-119">Wenn für Ihr Fenster keine flachen Bildlaufleisten initialisiert wurden, wird die API für flache Scrollleisten ggf. auf die entsprechenden Standardfunktionen zurückgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8475d-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="8475d-120">Dadurch können Sie flache Bildlaufleisten aktivieren und deaktivieren, ohne bedingten Code schreiben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="8475d-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="8475d-121">Da eine Anwendung möglicherweise benutzerdefinierte Metriken für ihre flachen Scrollleisten festgelegt hat, werden sie nicht automatisch aktualisiert, wenn sich die Systemmetriken ändern.</span><span class="sxs-lookup"><span data-stu-id="8475d-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="8475d-122">Wenn sich die Metriken der Scrollleiste des Systems ändern, wird eine [**WM \_ SETTINGCHANGE-Nachricht**](/windows/desktop/winmsg/wm-settingchange) übertragen, deren *wParam* auf [**SPI \_ SETNONCLIENTMETRICS festgelegt ist.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)</span><span class="sxs-lookup"><span data-stu-id="8475d-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="8475d-123">Um flache Bildlaufleisten auf die neuen Systemmetriken zu aktualisieren, müssen Anwendungen diese Meldung verarbeiten und die metrikabhängigen Eigenschaften der flachen Scrollleiste explizit ändern.</span><span class="sxs-lookup"><span data-stu-id="8475d-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="8475d-124">Verwenden Sie [**FlatSB \_ SetScrollProp,**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop)um die Eigenschaften der Scrollleiste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8475d-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="8475d-125">Das folgende Codefragment ändert die metrikabhängigen Eigenschaften einer flachen Scrollleiste in die aktuellen Systemwerte.</span><span class="sxs-lookup"><span data-stu-id="8475d-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="8475d-126">Verbessern von flachen Bildlaufleisten</span><span class="sxs-lookup"><span data-stu-id="8475d-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="8475d-127">[**FlatSB \_ Mit SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) können Sie die flachen Scrollleisten ändern, um das Aussehen Ihres Fensters anzupassen.</span><span class="sxs-lookup"><span data-stu-id="8475d-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="8475d-128">Bei vertikalen Bildlaufleisten können Sie die Breite des Balkens und die Höhe der Richtungspfeile ändern.</span><span class="sxs-lookup"><span data-stu-id="8475d-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="8475d-129">Bei horizontalen Scrollleisten können Sie die Höhe des Balkens und die Breite der Richtungspfeile ändern.</span><span class="sxs-lookup"><span data-stu-id="8475d-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="8475d-130">Sie können auch die Hintergrundfarbe der horizontalen und vertikalen Scrollleisten ändern.</span><span class="sxs-lookup"><span data-stu-id="8475d-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="8475d-131">[**FlatSB \_ Mit SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) können Sie auch anpassen, wie die flachen Scrollleisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8475d-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="8475d-132">Durch Ändern der Eigenschaften WSB PROP VSTYLE und WSB PROP HSTYLE können Sie den Typ der Bildlaufleiste \_ \_ \_ \_ festlegen, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8475d-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="8475d-133">Es sind drei Stile verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8475d-133">Three styles are available.</span></span>



|   <span data-ttu-id="8475d-134">Style</span><span class="sxs-lookup"><span data-stu-id="8475d-134">Style</span></span>                 |   <span data-ttu-id="8475d-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8475d-135">Description</span></span>                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8475d-136">\_FSB-ENCARTA-MODUS \_</span><span class="sxs-lookup"><span data-stu-id="8475d-136">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="8475d-137">Eine standardmäßige flache Bildlaufleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8475d-137">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="8475d-138">Wenn der Mauszeiger über eine Richtungsschaltfläche oder den Strich bewegt wird, wird dieser Teil der Scrollleiste in 3D angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8475d-138">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="8475d-139">FSB \_ FLAT \_ MODE</span><span class="sxs-lookup"><span data-stu-id="8475d-139">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="8475d-140">Eine standardmäßige flache Bildlaufleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8475d-140">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="8475d-141">Wenn der Mauszeiger über eine Richtungsschaltfläche oder den Strich bewegt wird, wird dieser Teil der Scrollleiste in invertierten Farben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8475d-141">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="8475d-142">REGULÄRER \_ \_ FSB-MODUS</span><span class="sxs-lookup"><span data-stu-id="8475d-142">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="8475d-143">Eine normale, nichtflat-Scrollleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8475d-143">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="8475d-144">Es werden keine speziellen visuellen Effekte angewendet.</span><span class="sxs-lookup"><span data-stu-id="8475d-144">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="8475d-145">Entfernen von flachen Bildlaufleisten</span><span class="sxs-lookup"><span data-stu-id="8475d-145">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="8475d-146">Wenn Sie flache Bildlaufleisten aus Ihrem Fenster entfernen möchten, rufen Sie die [**UninitializeFlatSB-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) auf, und übergeben Sie das Handle an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="8475d-146">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="8475d-147">Diese Funktion entfernt nur zur Laufzeit flache Bildlaufleisten aus Ihrem Fenster.</span><span class="sxs-lookup"><span data-stu-id="8475d-147">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="8475d-148">Sie müssen diese Funktion nicht aufrufen, wenn Ihr Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="8475d-148">You do not need to call this function when your window is destroyed.</span></span>

 

 