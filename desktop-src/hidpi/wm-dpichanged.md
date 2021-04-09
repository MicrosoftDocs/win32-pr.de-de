---
title: WM_DPICHANGED Meldung (Winuser. h)
description: Wird gesendet, wenn sich der dpi-Code (Effective dots per inch) für ein Fenster geändert hat.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED Message High dpi
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741833"
---
# <a name="wm_dpichanged-message"></a><span data-ttu-id="aecaf-104">\_Dpichanged-Meldung für WM</span><span class="sxs-lookup"><span data-stu-id="aecaf-104">WM\_DPICHANGED message</span></span>

<span data-ttu-id="aecaf-105">Wird gesendet, wenn sich der dpi-Code (Effective dots per inch) für ein Fenster geändert hat.</span><span class="sxs-lookup"><span data-stu-id="aecaf-105">Sent when the effective dots per inch (dpi) for a window has changed.</span></span> <span data-ttu-id="aecaf-106">Der dpi-Wert ist der Skalierungsfaktor für ein Fenster.</span><span class="sxs-lookup"><span data-stu-id="aecaf-106">The DPI is the scale factor for a window.</span></span> <span data-ttu-id="aecaf-107">Es gibt mehrere Ereignisse, die bewirken können, dass sich der dpi-Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="aecaf-107">There are multiple events that can cause the DPI to change.</span></span> <span data-ttu-id="aecaf-108">In der folgenden Liste sind die möglichen Ursachen für die Änderung in dpi angegeben.</span><span class="sxs-lookup"><span data-stu-id="aecaf-108">The following list indicates the possible causes for the change in DPI.</span></span>

-   <span data-ttu-id="aecaf-109">Das Fenster wird in einen neuen Monitor mit einem anderen dpi-Wert verschoben.</span><span class="sxs-lookup"><span data-stu-id="aecaf-109">The window is moved to a new monitor that has a different DPI.</span></span>
-   <span data-ttu-id="aecaf-110">Der dpi-Code des Monitors, der das Fenster gehostet, ändert sich.</span><span class="sxs-lookup"><span data-stu-id="aecaf-110">The DPI of the monitor hosting the window changes.</span></span>

<span data-ttu-id="aecaf-111">Der aktuelle dpi-Code für ein Fenster gleicht immer dem letzten von **WM \_ dpichanged** gesendeten dpi.</span><span class="sxs-lookup"><span data-stu-id="aecaf-111">The current DPI for a window always equals the last DPI sent by **WM\_DPICHANGED**.</span></span> <span data-ttu-id="aecaf-112">Dies ist der Skalierungsfaktor, auf den das Fenster für Threads skaliert werden soll, die von dpi-Änderungen abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="aecaf-112">This is the scale factor that the window should be scaling to for threads that are aware of DPI changes.</span></span>


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a><span data-ttu-id="aecaf-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="aecaf-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aecaf-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aecaf-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aecaf-115">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) des *wParam* enthält den Y-Achsen-Wert des neuen dpi-Werts des Fensters.</span><span class="sxs-lookup"><span data-stu-id="aecaf-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the *wParam* contains the Y-axis value of the new dpi of the window.</span></span> <span data-ttu-id="aecaf-116">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des *wParam* enthält den Wert der X-Achse des neuen dpi-Werts des Fensters.</span><span class="sxs-lookup"><span data-stu-id="aecaf-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the *wParam* contains the X-axis value of the new DPI of the window.</span></span> <span data-ttu-id="aecaf-117">Beispiel: 96, 120, 144 oder 192.</span><span class="sxs-lookup"><span data-stu-id="aecaf-117">For example, 96, 120, 144, or 192.</span></span> <span data-ttu-id="aecaf-118">Die Werte der X-Achse und der Y-Achse sind bei Windows-apps identisch.</span><span class="sxs-lookup"><span data-stu-id="aecaf-118">The values of the X-axis and the Y-axis are identical for Windows apps.</span></span>

</dd> <dt>

<span data-ttu-id="aecaf-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aecaf-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aecaf-120">Ein Zeiger auf eine [**Rect**](/windows/desktop/api/windef/ns-windef-rect) -Struktur, die eine vorgeschlagene Größe und Position des aktuellen Fensters bereitstellt, das für den neuen dpi-Wert skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="aecaf-120">A pointer to a [**RECT**](/windows/desktop/api/windef/ns-windef-rect) structure that provides a suggested size and position of the current window scaled for the new DPI.</span></span> <span data-ttu-id="aecaf-121">Es wird erwartet, dass sich die apps auf der Grundlage der von *LPARAM* bereitgestellten Vorschläge bei der Verarbeitung dieser Nachricht neu positionieren und die Größe der Fenstergröße ändern.</span><span class="sxs-lookup"><span data-stu-id="aecaf-121">The expectation is that apps will reposition and resize windows based on the suggestions provided by *lParam* when handling this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aecaf-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aecaf-122">Return value</span></span>

<span data-ttu-id="aecaf-123">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aecaf-123">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aecaf-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aecaf-124">Remarks</span></span>

<span data-ttu-id="aecaf-125">Diese Meldung ist nur für Prozesse relevant, die **\_ \_ \_ dpi \_** -abhängige Anwendungen oder dpi-Informationen **\_ \_ pro \_ Monitor \_ erkennen** .</span><span class="sxs-lookup"><span data-stu-id="aecaf-125">This message is only relevant for **PROCESS\_PER\_MONITOR\_DPI\_AWARE** applications or **DPI\_AWARENESS\_PER\_MONITOR\_AWARE** threads.</span></span> <span data-ttu-id="aecaf-126">Sie kann auf bestimmten dpi-Änderungen empfangen werden, wenn das Fenster oder der Prozess der obersten Ebene als **dpi** -Wert oder **System-dpi**-fähig ausgeführt wird. in diesen Fällen kann es jedoch problemlos ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="aecaf-126">It may be received on certain DPI changes if your top-level window or process is running as **DPI unaware** or **system DPI aware**, but in those situations it can be safely ignored.</span></span> <span data-ttu-id="aecaf-127">Weitere Informationen zu den unterschiedlichen Arten von Informationen finden Sie unter [**Process \_ dpi \_ Awareness**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**dpi \_ Awareness**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span><span class="sxs-lookup"><span data-stu-id="aecaf-127">For more information about the different types of awareness, see [**PROCESS\_DPI\_AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**DPI\_AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span></span> <span data-ttu-id="aecaf-128">Ältere Versionen von Windows erforderten die dpi-Informationen, die auf der Ebene einer Anwendung gebunden werden mussten.</span><span class="sxs-lookup"><span data-stu-id="aecaf-128">Older versions of Windows required DPI awareness to be tied at the level of an application.</span></span> <span data-ttu-id="aecaf-129">Diese Apps verwenden **Prozess \_ - \_ dpi**-Informationen.</span><span class="sxs-lookup"><span data-stu-id="aecaf-129">Those apps use **PROCESS\_DPI\_AWARENESS**.</span></span> <span data-ttu-id="aecaf-130">Derzeit ist das dpi-Bewusstsein an Threads und einzelne Fenster gebunden, nicht an die gesamte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="aecaf-130">Currently, DPI awareness is tied to threads and individual windows rather than the entire application.</span></span> <span data-ttu-id="aecaf-131">Diese Apps verwenden **dpi \_**-Informationen.</span><span class="sxs-lookup"><span data-stu-id="aecaf-131">These apps use **DPI\_AWARENESS**.</span></span>

<span data-ttu-id="aecaf-132">Beim Skalieren der Anwendung müssen Sie nur den Wert der X-Achse oder der Y-Achse verwenden, da diese identisch sind.</span><span class="sxs-lookup"><span data-stu-id="aecaf-132">You only need to use either the X-axis or the Y-axis value when scaling your application since they are the same.</span></span>

<span data-ttu-id="aecaf-133">Damit diese Nachricht ordnungsgemäß verarbeitet wird, müssen Sie die Größe des Fensters auf der Grundlage der von *LPARAM* bereitgestellten Vorschläge und der Verwendung von [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)ändern.</span><span class="sxs-lookup"><span data-stu-id="aecaf-133">In order to handle this message correctly, you will need to resize and reposition your window based on the suggestions provided by *lParam* and using [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="aecaf-134">Wenn Sie dies nicht tun, vergrößert oder verkleinert sich das Fenster in Bezug auf alles andere auf dem neuen Monitor.</span><span class="sxs-lookup"><span data-stu-id="aecaf-134">If you do not do this, your window will grow or shrink with respect to everything else on the new monitor.</span></span> <span data-ttu-id="aecaf-135">Wenn ein Benutzer z. b. mehrere Monitore verwendet und das Fenster von einem 96-dpi-Monitor auf einen 192 dpi-Monitor zieht, wird das Fenster in Bezug auf andere Elemente im 192-dpi-Monitor in der Hälfte der Größe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aecaf-135">For example, if a user is using multiple monitors and drags your window from a 96 DPI monitor to a 192 DPI monitor, your window will appear to be half as large with respect to other items on the 192 DPI monitor.</span></span>

<span data-ttu-id="aecaf-136">Der Basiswert von dpi ist als **Benutzer \_ \_ Standardbildschirm \_ dpi** definiert, der auf 96 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aecaf-136">The base value of DPI is defined as **USER\_DEFAULT\_SCREEN\_DPI** which is set to 96.</span></span> <span data-ttu-id="aecaf-137">Um den Skalierungsfaktor für einen Monitor zu ermitteln, nehmen Sie den dpi-Wert an, und teilen Sie die **\_ Standard \_ Bildschirm \_ dpi des Benutzers**.</span><span class="sxs-lookup"><span data-stu-id="aecaf-137">To determine the scaling factor for a monitor, take the DPI value and divide by **USER\_DEFAULT\_SCREEN\_DPI**.</span></span> <span data-ttu-id="aecaf-138">In der folgenden Tabelle finden Sie einige Beispiel-dpi-Werte und zugeordnete Skalierungsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="aecaf-138">The following table provides some sample DPI values and associated scaling factors.</span></span>



| <span data-ttu-id="aecaf-139">DPI-Wert</span><span class="sxs-lookup"><span data-stu-id="aecaf-139">DPI value</span></span> | <span data-ttu-id="aecaf-140">Skalierung in Prozent</span><span class="sxs-lookup"><span data-stu-id="aecaf-140">Scaling percentage</span></span> |
|-----------|--------------------|
| <span data-ttu-id="aecaf-141">96</span><span class="sxs-lookup"><span data-stu-id="aecaf-141">96</span></span>        | <span data-ttu-id="aecaf-142">100 %</span><span class="sxs-lookup"><span data-stu-id="aecaf-142">100%</span></span>               |
| <span data-ttu-id="aecaf-143">120</span><span class="sxs-lookup"><span data-stu-id="aecaf-143">120</span></span>       | <span data-ttu-id="aecaf-144">125%</span><span class="sxs-lookup"><span data-stu-id="aecaf-144">125%</span></span>               |
| <span data-ttu-id="aecaf-145">144</span><span class="sxs-lookup"><span data-stu-id="aecaf-145">144</span></span>       | <span data-ttu-id="aecaf-146">150%</span><span class="sxs-lookup"><span data-stu-id="aecaf-146">150%</span></span>               |
| <span data-ttu-id="aecaf-147">192</span><span class="sxs-lookup"><span data-stu-id="aecaf-147">192</span></span>       | <span data-ttu-id="aecaf-148">200 %</span><span class="sxs-lookup"><span data-stu-id="aecaf-148">200%</span></span>               |



 

<span data-ttu-id="aecaf-149">Im folgenden Beispiel wird ein Beispiel für einen dpi-Änderungs Handler bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="aecaf-149">The following example provides a sample DPI change handler.</span></span>


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



<span data-ttu-id="aecaf-150">Mit dem folgenden Code wird ein Wert von 100% (96 dpi) Linear auf einen beliebigen dpi-Wert skaliert, der durch *g \_ dpi* definiert ist.</span><span class="sxs-lookup"><span data-stu-id="aecaf-150">The following code linearly scales a value from 100% (96 DPI) to an arbitrary DPI defined by *g\_dpi*.</span></span>


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



<span data-ttu-id="aecaf-151">Eine alternative Möglichkeit zum Skalieren eines Werts besteht darin, den dpi-Wert in einen Skalierungsfaktor zu konvertieren und diesen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aecaf-151">An alternative way to scale a value is to convert the DPI value into a scale factor and use that.</span></span>


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a><span data-ttu-id="aecaf-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aecaf-152">Requirements</span></span>



| <span data-ttu-id="aecaf-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aecaf-153">Requirement</span></span> | <span data-ttu-id="aecaf-154">Wert</span><span class="sxs-lookup"><span data-stu-id="aecaf-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aecaf-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aecaf-155">Minimum supported client</span></span><br/> | <span data-ttu-id="aecaf-156">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="aecaf-156">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aecaf-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aecaf-157">Minimum supported server</span></span><br/> | <span data-ttu-id="aecaf-158">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aecaf-158">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aecaf-159">Header</span><span class="sxs-lookup"><span data-stu-id="aecaf-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="aecaf-160"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="aecaf-160"><dt>WinUser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aecaf-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aecaf-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecaf-162">**DPI \_ -Informationen**</span><span class="sxs-lookup"><span data-stu-id="aecaf-162">**DPI\_AWARENESS**</span></span>](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[<span data-ttu-id="aecaf-163">**Prozess- \_ dpi- \_ Bewusstsein**</span><span class="sxs-lookup"><span data-stu-id="aecaf-163">**PROCESS\_DPI\_AWARENESS**</span></span>](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

