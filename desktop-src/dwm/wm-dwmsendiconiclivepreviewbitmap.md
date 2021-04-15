---
title: WM_DWMSENDICONICLIVEPREVIEWBITMAP Meldung (dwmapi. h)
description: Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als Live Vorschau (auch als Vorschau Vorschau bezeichnet) dieses Fensters verwendet werden soll.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477001"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a><span data-ttu-id="93006-104">WM \_ dwmsendiconiclivepreviewbitmap-Meldung</span><span class="sxs-lookup"><span data-stu-id="93006-104">WM\_DWMSENDICONICLIVEPREVIEWBITMAP message</span></span>

<span data-ttu-id="93006-105">Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als *Live Vorschau* (auch als *Vorschau Vorschau* bezeichnet) dieses Fensters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93006-105">Instructs a window to provide a static bitmap to use as a *live preview* (also known as a *Peek preview*) of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="93006-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93006-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93006-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93006-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="93006-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="93006-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93006-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93006-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="93006-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93006-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93006-111">Return value</span></span>

<span data-ttu-id="93006-112">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="93006-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="93006-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93006-113">Remarks</span></span>

<span data-ttu-id="93006-114">Eine *Live Vorschau* (auch als *Vorschau Vorschau* bezeichnet) eines Fensters wird angezeigt, wenn ein Benutzer den Mauszeiger über die Miniaturansicht des Fensters in der Taskleiste bewegt oder den Miniatur Ansichts Fokus im Alt + Tab-Fenster verschiebt.</span><span class="sxs-lookup"><span data-stu-id="93006-114">A *live preview* (also known as a *Peek preview*) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window.</span></span> <span data-ttu-id="93006-115">Diese Ansicht ist eine Vorschau des Fensters in voller Größen und kann eine Live Momentaufnahme oder eine Darstellung darstellen.</span><span class="sxs-lookup"><span data-stu-id="93006-115">This view is a full-sized preview of the window and can be a live snapshot or an iconic representation.</span></span>

<span data-ttu-id="93006-116">Desktopfenster-Manager (DWM) sendet diese Nachricht an ein Fenster, wenn alle der folgenden Situationen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="93006-116">Desktop Window Manager (DWM) sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="93006-117">Die Live Vorschau wurde im Fenster aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="93006-117">Live preview has been invoked on the window.</span></span>
-   <span data-ttu-id="93006-118">Das [**dwmwa-Attribut \_ enthält ein \_ berühmtes \_ Bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) -Attribut, das im Fenster festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93006-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="93006-119">Eine legendäre Darstellung ist die einzige, die für dieses Fenster vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="93006-119">An iconic representation is the only one that exists for this window.</span></span>

<span data-ttu-id="93006-120">Das Fenster, in dem diese Meldung empfangen wird, sollte durch das Erstellen einer Bitmap mit vollständigem skalieren Antworten.</span><span class="sxs-lookup"><span data-stu-id="93006-120">The window that receives this message should respond by generating a full-scale bitmap.</span></span> <span data-ttu-id="93006-121">Das Fenster ruft dann die [**dwmseticoniclivepreviewbitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) -Funktion auf, um die Live Vorschau festzulegen.</span><span class="sxs-lookup"><span data-stu-id="93006-121">The window then calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function to set the live preview.</span></span> <span data-ttu-id="93006-122">Wenn im Fenster keine Bitmap in einem bestimmten Zeitraum festgelegt wird, verwendet DWM eine eigene Standarddarstellung für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="93006-122">If the window does not set a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

## <a name="examples"></a><span data-ttu-id="93006-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93006-123">Examples</span></span>

<span data-ttu-id="93006-124">Das folgende Beispiel zeigt eine Antwort auf die **WM- \_ dwmsendiconiclivepreviewbitmap** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="93006-124">The following example demonstrates a response to the **WM\_DWMSENDICONICLIVEPREVIEWBITMAP** message.</span></span> <span data-ttu-id="93006-125">Im Beispiel wird die [**dwmtarticoniclivepreviewbitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) -Funktion mit einem Handle für eine angepasste, geräteunabhängige Bitmap aufgerufen, die als Darstellung des Fensters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93006-125">The example calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function with a handle to a customized, device-independent bitmap to use as the window's representation.</span></span>


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="93006-126">Den gesamten Code finden Sie im Beispiel [Anpassen einer Miniaturansicht und Live Vorschau Bitmap](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="93006-126">For the complete code, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="93006-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93006-127">Requirements</span></span>



| <span data-ttu-id="93006-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93006-128">Requirement</span></span> | <span data-ttu-id="93006-129">Wert</span><span class="sxs-lookup"><span data-stu-id="93006-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="93006-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93006-130">Minimum supported client</span></span><br/> | <span data-ttu-id="93006-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93006-131">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="93006-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93006-132">Minimum supported server</span></span><br/> | <span data-ttu-id="93006-133">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93006-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="93006-134">Header</span><span class="sxs-lookup"><span data-stu-id="93006-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="93006-135"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="93006-135"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93006-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93006-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93006-137">**WM \_ dwmsendianicminiatur**</span><span class="sxs-lookup"><span data-stu-id="93006-137">**WM\_DWMSENDICONICTHUMBNAIL**</span></span>](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[<span data-ttu-id="93006-138">**Dwminvalidateiconfiguration**</span><span class="sxs-lookup"><span data-stu-id="93006-138">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





