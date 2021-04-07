---
title: Flache Scrollleisten
description: Microsoft Internet Explorer 4,0 führte eine neue visuelle Technologie mit dem Namen "flatscrollleisten" ein.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730457"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="31b6f-103">Flache Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="31b6f-103">Flat Scroll Bars</span></span>

<span data-ttu-id="31b6f-104">Microsoft Internet Explorer 4,0 führte eine neue visuelle Technologie mit dem Namen "flatscrollleisten" ein.</span><span class="sxs-lookup"><span data-stu-id="31b6f-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="31b6f-105">Funktionale, flache Schiebe leisten Verhalten sich genau wie Standard Scrollleisten.</span><span class="sxs-lookup"><span data-stu-id="31b6f-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="31b6f-106">Der Unterschied besteht darin, dass Sie Ihre Darstellung in größerem Umfang als Standard Scrollleisten anpassen können.</span><span class="sxs-lookup"><span data-stu-id="31b6f-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="31b6f-107">Die folgende Abbildung zeigt ein Fenster, das eine flache Bild Lauf Leiste enthält.</span><span class="sxs-lookup"><span data-stu-id="31b6f-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![Screenshot eines Fensters, das eine flatscrollleiste enthält](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="31b6f-109">Flache Schiebe leisten werden von Comctl32.dll Versionen 4,71 bis 5,82 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31b6f-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="31b6f-110">In Comctl32.dll, Version 6,00 und höher, werden keine flachen Schiebe leisten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="31b6f-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="31b6f-111">Verwenden von flachen Schiebe leisten</span><span class="sxs-lookup"><span data-stu-id="31b6f-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="31b6f-112">In diesem Abschnitt wird beschrieben, wie Sie flache Schiebe leisten in der Anwendung implementieren.</span><span class="sxs-lookup"><span data-stu-id="31b6f-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="31b6f-113">Vorbereitungen</span><span class="sxs-lookup"><span data-stu-id="31b6f-113">Before You Begin</span></span>

<span data-ttu-id="31b6f-114">Wenn Sie die Funktionen der flatscrollleiste verwenden möchten, müssen Sie in den Quelldateien kommctrl. h einschließen und mit Comctl32. lib verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="31b6f-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="31b6f-115">Hinzufügen von flatscrollleisten zu einem Fenster</span><span class="sxs-lookup"><span data-stu-id="31b6f-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="31b6f-116">Wenn Sie einem Fenster flatscrollleisten hinzufügen möchten, führen Sie [**initializeflatsb**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)aus, und übergeben Sie das Handle an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="31b6f-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="31b6f-117">Anstatt die Scrollleisten-Standardfunktionen zum Bearbeiten der Schiebe leisten zu verwenden, müssen Sie die entsprechende flatsb \_ xxx-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="31b6f-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="31b6f-118">Es gibt flache Scrollleisten-Funktionen zum Festlegen und Abrufen der scrollinformationen, des Bereichs und der Position.</span><span class="sxs-lookup"><span data-stu-id="31b6f-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="31b6f-119">Wenn für das Fenster keine flatscrollleisten initialisiert wurden, wird die API für die flatscrollleiste auf die entsprechenden Standardfunktionen zurückgestellt, sofern diese verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31b6f-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="31b6f-120">Auf diese Weise können Sie flache Schiebe leisten ein-und ausschalten, ohne bedingten Code schreiben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="31b6f-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="31b6f-121">Da eine Anwendung möglicherweise benutzerdefinierte Metriken für Ihre flachen Schiebe leisten festgelegt hat, werden Sie nicht automatisch aktualisiert, wenn sich Systemmetriken ändern.</span><span class="sxs-lookup"><span data-stu-id="31b6f-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="31b6f-122">Wenn sich die Metriken der systemscrollleiste ändern, wird eine [**WM- \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) -Nachricht gesendet, wobei *wParam* auf [**SPI \_ setnonclientmetrics**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="31b6f-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="31b6f-123">Zum Aktualisieren von flatscrollleisten auf die neuen Systemmetriken müssen Anwendungen diese Nachricht verarbeiten und die metrikabhängigen Eigenschaften der flatscrollleiste explizit ändern.</span><span class="sxs-lookup"><span data-stu-id="31b6f-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="31b6f-124">Verwenden Sie [**flatsb \_ setscrollprop**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop), um die ScrollBar-Eigenschaften zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="31b6f-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="31b6f-125">Mit dem folgenden Code Fragment werden die metrikabhängigen Eigenschaften einer flatscrollleiste auf die aktuellen System Werte geändert.</span><span class="sxs-lookup"><span data-stu-id="31b6f-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


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



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="31b6f-126">Verbessern von flachen Schiebe leisten</span><span class="sxs-lookup"><span data-stu-id="31b6f-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="31b6f-127">[**Flatsb \_ Setscrollprop**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) ermöglicht es Ihnen, die flachen Schiebe leisten zu ändern, um das Aussehen des Fensters anzupassen.</span><span class="sxs-lookup"><span data-stu-id="31b6f-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="31b6f-128">Bei vertikalen Schiebe leisten können Sie die Breite des Balkens und die Höhe der Pfeilrichtung ändern.</span><span class="sxs-lookup"><span data-stu-id="31b6f-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="31b6f-129">Bei horizontalen Schiebe leisten können Sie die Höhe des Balkens und die Breite der Pfeilrichtung ändern.</span><span class="sxs-lookup"><span data-stu-id="31b6f-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="31b6f-130">Sie können auch die Hintergrundfarbe der horizontalen und vertikalen Schiebe leisten ändern.</span><span class="sxs-lookup"><span data-stu-id="31b6f-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="31b6f-131">[**Flatsb \_ Mit setscrollprop**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) können Sie auch anpassen, wie die flachen Schiebe leisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="31b6f-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="31b6f-132">Durch Ändern der Eigenschaften von WSB \_ Prop \_ Vstyle und WSB \_ Prop \_ hstyle können Sie den Typ der Scrollleiste festlegen, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="31b6f-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="31b6f-133">Es sind drei Stile verfügbar.</span><span class="sxs-lookup"><span data-stu-id="31b6f-133">Three styles are available.</span></span>



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b6f-134">FSB- \_ Encarta- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="31b6f-134">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="31b6f-135">Eine standardmäßige flatscrollleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31b6f-135">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="31b6f-136">Wenn die Maus über eine Richtungs Schaltfläche oder den Ziehpunkt bewegt wird, wird dieser Teil der Bild Lauf Leiste in 3D angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31b6f-136">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="31b6f-137">FSB \_ - \_ FlatMode</span><span class="sxs-lookup"><span data-stu-id="31b6f-137">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="31b6f-138">Eine standardmäßige flatscrollleiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31b6f-138">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="31b6f-139">Wenn die Maus über eine Richtungs Schaltfläche oder den Ziehpunkt bewegt wird, wird dieser Teil der Bild Lauf Leiste in umgekehrten Farben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31b6f-139">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="31b6f-140">\_regulärer \_ Modus für FSB</span><span class="sxs-lookup"><span data-stu-id="31b6f-140">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="31b6f-141">Eine normale, nicht flache Bild Lauf Leiste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31b6f-141">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="31b6f-142">Es werden keine besonderen visuellen Effekte angewendet.</span><span class="sxs-lookup"><span data-stu-id="31b6f-142">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="31b6f-143">Entfernen von flachen Schiebe leisten</span><span class="sxs-lookup"><span data-stu-id="31b6f-143">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="31b6f-144">Wenn Sie flache Schiebe leisten aus dem Fenster entfernen möchten, können Sie die Funktion [**uninitializeflatsb**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) aufrufen und das Handle an das Fenster übergeben.</span><span class="sxs-lookup"><span data-stu-id="31b6f-144">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="31b6f-145">Diese Funktion entfernt nur flatscrollleisten aus dem Fenster zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="31b6f-145">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="31b6f-146">Diese Funktion muss nicht aufgerufen werden, wenn das Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="31b6f-146">You do not need to call this function when your window is destroyed.</span></span>

 

 