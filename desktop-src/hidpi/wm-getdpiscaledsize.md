---
title: WM_GETDPISCALEDSIZE Meldung (Winuser. h)
description: Diese Meldung weist das Betriebssystem an, dass die Größe des Fensters auf andere Dimensionen als die Standardgröße festgelegt wird.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE Message High dpi
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476857"
---
# <a name="wm_getdpiscaledsize-message"></a><span data-ttu-id="2cbff-104">WM \_ getdpiscaledsize-Meldung</span><span class="sxs-lookup"><span data-stu-id="2cbff-104">WM\_GETDPISCALEDSIZE message</span></span>

<span data-ttu-id="2cbff-105">Diese Meldung weist das Betriebssystem an, dass die Größe des Fensters auf andere Dimensionen als die Standardgröße festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="2cbff-105">This message tells the operating system that the window will be sized to dimensions other than the default.</span></span>

<span data-ttu-id="2cbff-106">Diese Nachricht wird mit einem dpi-kontextkontext von pro Monitor v2 an Fenster der obersten Ebene gesendet, bevor eine [**WM- \_ dpichanged**](wm-dpichanged.md) -Nachricht gesendet wird. Dadurch kann das Fenster die gewünschte Größe für die ausstehende dpi-Änderung berechnen. [ \_ \_](dpi-awareness-context.md)</span><span class="sxs-lookup"><span data-stu-id="2cbff-106">This message is sent to top-level windows with a [DPI\_AWARENESS\_CONTEXT](dpi-awareness-context.md) of Per Monitor v2 before a [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent, and allows the window to compute its desired size for the pending DPI change.</span></span> <span data-ttu-id="2cbff-107">Da die lineare DPI-Skalierung das Standardverhalten ist, ist dies nur in Szenarios nützlich, in denen das Fenster nicht linear skaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cbff-107">As linear DPI scaling is the default behavior, this is only useful in scenarios where the window wants to scale non-linearly.</span></span> <span data-ttu-id="2cbff-108">Wenn die Anwendung auf diese Meldung antwortet, ist die resultierende Größe das Kandidaten Rechteck, das an **WM \_ dpichanged** gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2cbff-108">If the application responds to this message, the resulting size will be the candidate rectangle send to **WM\_DPICHANGED**.</span></span>

<span data-ttu-id="2cbff-109">Verwenden Sie diese Meldung, um die Größe der mit [**WM \_ dpichanged**](wm-dpichanged.md)bereitgestellten Rect zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2cbff-109">Use this message to alter the size of the rect that is provided with [**WM\_DPICHANGED**](wm-dpichanged.md).</span></span>


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a><span data-ttu-id="2cbff-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cbff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbff-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cbff-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbff-112">Der wParam-Wert enthält einen dpi-Wert.</span><span class="sxs-lookup"><span data-stu-id="2cbff-112">The WPARAM contains a DPI value.</span></span> <span data-ttu-id="2cbff-113">Die skalierte Fenstergröße, die von der Anwendung festgelegt wird, muss berechnet werden, als ob das Fenster zu diesem dpi-Wert wechseln soll.</span><span class="sxs-lookup"><span data-stu-id="2cbff-113">The scaled window size that the application would set needs to be computed as if the window were to switch to this DPI.</span></span>

</dd> <dt>

<span data-ttu-id="2cbff-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cbff-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbff-115">Der lParam ist ein in/out-Zeiger auf eine Größen Struktur.</span><span class="sxs-lookup"><span data-stu-id="2cbff-115">The LPARAM is an in/out pointer to a SIZE struct.</span></span> <span data-ttu-id="2cbff-116">Der \_ in- \_ Wert in lParam ist die ausstehende Größe des Fensters nach einem vom Benutzer initiierten Verschiebe Vorgang oder einem Aufrufen von [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="2cbff-116">The \_In\_ value in the LPARAM is the pending size of the window after a user-initiated move or a call to [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="2cbff-117">Wenn die Größe des Fensters geändert wird, ist diese Größe nicht notwendigerweise identisch mit der aktuellen Größe des Fensters, wenn diese Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="2cbff-117">If the window is being resized, this size is not necessarily the same as the window's current size at the time this message is received.</span></span>

<span data-ttu-id="2cbff-118">Der \_ out- \_ Wert in der lParam sollte von der Anwendung geschrieben werden, um die gewünschte skalierte Fenstergröße anzugeben, die dem bereitgestellten dpi-Wert in der wParam entspricht.</span><span class="sxs-lookup"><span data-stu-id="2cbff-118">The \_Out\_ value in the LPARAM should be written to by the application to specify the desired scaled window size corresponding to the provided DPI value in the WPARAM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbff-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cbff-119">Return value</span></span>

<span data-ttu-id="2cbff-120">Die-Funktion gibt einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2cbff-120">The function returns a BOOL.</span></span> <span data-ttu-id="2cbff-121">Die Rückgabe von true gibt an, dass eine neue Größe berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2cbff-121">Returning TRUE indicates that a new size has been computed.</span></span> <span data-ttu-id="2cbff-122">Wenn false zurückgegeben wird, wird die Nachricht nicht behandelt, und die standardmäßige lineare DPI-Skalierung wird auf das Fenster angewendet.</span><span class="sxs-lookup"><span data-stu-id="2cbff-122">Returning FALSE indicates that the message will not be handled, and the default linear DPI scaling will apply to the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbff-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cbff-123">Remarks</span></span>

<span data-ttu-id="2cbff-124">Diese Meldung wird nur an Fenster der obersten Ebene gesendet, die über einen dpi-Kontext von pro Monitor v2 verfügen.</span><span class="sxs-lookup"><span data-stu-id="2cbff-124">This message is only sent to top-level windows which have a DPI awareness context of Per Monitor v2.</span></span>

<span data-ttu-id="2cbff-125">Dieses Ereignis ist erforderlich, um eine ordnungsgemäße nichtlineare Skalierung zu ermöglichen, und stellt sicher, dass die Position des Windows in Beziehung zum Cursor und beim hin-und herwechseln zwischen den Monitoren konstant bleibt.</span><span class="sxs-lookup"><span data-stu-id="2cbff-125">This event is necessary to facilitate graceful non-linear scaling, and ensures that the windows's position remains constant in relationship to the cursor and when moving back and forth across monitors.</span></span>

<span data-ttu-id="2cbff-126">In [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)gibt es keine bestimmte Standardbehandlung für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2cbff-126">There is no specific default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="2cbff-127">Wie bei allen Nachrichten, die nicht explizit behandelt werden, gibt [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) für diese Nachricht 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="2cbff-127">As for all messages it does not explicitly handle, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will return zero for this message.</span></span> <span data-ttu-id="2cbff-128">Wie bereits erwähnt, weist diese Rückgabe das System an, das lineare Standardverhalten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2cbff-128">As noted above, this return tells the system to use the default linear behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbff-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cbff-129">Requirements</span></span>



| <span data-ttu-id="2cbff-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cbff-130">Requirement</span></span> | <span data-ttu-id="2cbff-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2cbff-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbff-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cbff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbff-133">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cbff-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2cbff-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cbff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbff-135">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cbff-135">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2cbff-136">Header</span><span class="sxs-lookup"><span data-stu-id="2cbff-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cbff-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cbff-137"><dt>Winuser.h</dt></span></span> </dl> |



 

