---
title: WM_DWMSENDICONICTHUMBNAIL Meldung (dwmapi. h)
description: Weist ein Fenster an, ein statisches Bitmap bereitzustellen, das als Miniaturansicht dieses Fensters verwendet werden soll.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478765"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a><span data-ttu-id="39360-104">WM \_ dwmsendiimimanthumbnail-Meldung</span><span class="sxs-lookup"><span data-stu-id="39360-104">WM\_DWMSENDICONICTHUMBNAIL message</span></span>

<span data-ttu-id="39360-105">Weist ein Fenster an, ein statisches Bitmap bereitzustellen, das als Miniaturansicht dieses Fensters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39360-105">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="39360-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39360-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39360-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39360-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39360-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="39360-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="39360-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39360-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39360-110">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) dieses Werts ist die maximale x-Koordinate der Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="39360-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this value is the maximum x-coordinate of the thumbnail.</span></span> <span data-ttu-id="39360-111">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die maximale y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="39360-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum y-coordinate.</span></span> <span data-ttu-id="39360-112">Wenn eine Miniaturansicht eine Dimension aufweist, die einen oder beide dieser Werte überschreitet, akzeptiert die DWM die Miniaturansicht nicht.</span><span class="sxs-lookup"><span data-stu-id="39360-112">If a thumbnail has a dimension that exceeds one or both of these values, the DWM does not accept the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39360-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39360-113">Return value</span></span>

<span data-ttu-id="39360-114">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="39360-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="39360-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39360-115">Remarks</span></span>

<span data-ttu-id="39360-116">DWM sendet diese Nachricht an ein Fenster, wenn alle der folgenden Situationen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="39360-116">DWM sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="39360-117">DWM zeigt eine Darstellung des Fensters an.</span><span class="sxs-lookup"><span data-stu-id="39360-117">DWM is displaying an iconic representation of the window.</span></span>
-   <span data-ttu-id="39360-118">Das [**dwmwa-Attribut \_ enthält ein \_ berühmtes \_ Bitmap**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) -Attribut, das im Fenster festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39360-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="39360-119">Das Fenster hat keine zwischengespeicherte Bitmap festgelegt.</span><span class="sxs-lookup"><span data-stu-id="39360-119">The window did not set a cached bitmap.</span></span>
-   <span data-ttu-id="39360-120">Es ist Platz im Cache für eine andere Bitmap vorhanden.</span><span class="sxs-lookup"><span data-stu-id="39360-120">There is room in the cache for another bitmap.</span></span>

<span data-ttu-id="39360-121">Das Fenster, das diese Nachricht empfängt, sollte Antworten, indem Sie eine Bitmap erzeugen, die nicht größer als die in den Nachrichten Parametern angeforderte Größe ist.</span><span class="sxs-lookup"><span data-stu-id="39360-121">The window that receives this message should respond by generating a bitmap that is not larger than the size that is requested in the message parameters.</span></span> <span data-ttu-id="39360-122">Das Fenster ruft dann die Funktion " [**dwmsetticonfiguration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) " auf, um die Standard Miniaturansicht zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="39360-122">The window then calls the [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function to override the default thumbnail.</span></span> <span data-ttu-id="39360-123">Wenn das Fenster keine Bitmap in einem bestimmten Zeitraum bereitstellt, verwendet DWM eine eigene Standarddarstellung für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="39360-123">If the window does not supply a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

<span data-ttu-id="39360-124">Das Fenster muss dem aufrufenden Prozess angehören.</span><span class="sxs-lookup"><span data-stu-id="39360-124">The window must belong to the calling process.</span></span>

## <a name="examples"></a><span data-ttu-id="39360-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39360-125">Examples</span></span>

<span data-ttu-id="39360-126">Im folgenden Codebeispiel wird gezeigt, wie auf die **WM- \_ dwmsendiimc-Meldung** reagiert wird.</span><span class="sxs-lookup"><span data-stu-id="39360-126">The following code example shows how to respond to the **WM\_DWMSENDICONICTHUMBNAIL** message.</span></span> <span data-ttu-id="39360-127">Im Beispiel wird [**dwmtarticonfiguration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)mit einem Handle für eine angepasste, geräteunabhängige Bitmap aufgerufen, die als Windows-Darstellung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39360-127">The example calls [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), with a handle to a customized, device-indepedent bitmap to use as the windows' representation.</span></span>


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="39360-128">Das komplette Beispiel finden Sie im Beispiel [Anpassen einer Miniaturansicht und Live Vorschau Bitmap](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="39360-128">For the complete example, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="39360-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39360-129">Requirements</span></span>



| <span data-ttu-id="39360-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39360-130">Requirement</span></span> | <span data-ttu-id="39360-131">Wert</span><span class="sxs-lookup"><span data-stu-id="39360-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39360-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39360-132">Minimum supported client</span></span><br/> | <span data-ttu-id="39360-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39360-133">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="39360-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39360-134">Minimum supported server</span></span><br/> | <span data-ttu-id="39360-135">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39360-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39360-136">Header</span><span class="sxs-lookup"><span data-stu-id="39360-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="39360-137"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39360-137"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39360-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39360-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39360-139">**Dwminvalidateiconfiguration**</span><span class="sxs-lookup"><span data-stu-id="39360-139">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[<span data-ttu-id="39360-140">**WM \_ dwmsendiconiclivepreviewbitmap**</span><span class="sxs-lookup"><span data-stu-id="39360-140">**WM\_DWMSENDICONICLIVEPREVIEWBITMAP**</span></span>](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

