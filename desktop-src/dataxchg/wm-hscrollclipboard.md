---
title: WM_HSCROLLCLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- WM_HSCROLLCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478303"
---
# <a name="wm_hscrollclipboard-message"></a><span data-ttu-id="3e9e8-104">WM- \_ hscrollclipboard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3e9e8-104">WM\_HSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="3e9e8-105">Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-105">Sent to the clipboard owner by a clipboard viewer window.</span></span> <span data-ttu-id="3e9e8-106">Dies tritt auf, wenn die Zwischenablage Daten im CF-Besitzer Anzeige Format enthält und ein Ereignis in der horizontalen Schiebe Leiste der Zwischenablage [**\_ Anzeige**](standard-clipboard-formats.md) auftritt.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-106">This occurs when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's horizontal scroll bar.</span></span> <span data-ttu-id="3e9e8-107">Der Besitzer sollte das Zwischenablage Bild scrollen und die ScrollBar-Werte aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-107">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a><span data-ttu-id="3e9e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e9e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e9e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e9e8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e9e8-110">Ein Handle für das Fenster der Zwischenablage Anzeige.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-110">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="3e9e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e9e8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e9e8-112">Das nieder wertige Wort von *LPARAM* gibt ein ScrollBar-Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-112">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="3e9e8-113">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="3e9e8-114">Das aktuellste Wort von *LPARAM* gibt die aktuelle Position des Bild Lauf Felds an, wenn es sich bei dem nieder wertigen Wort von *LPARAM* um SB-Finger **\_ Positionen** handelt. andernfalls wird das höchst wertige Wort nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-114">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word is not used.</span></span>



| <span data-ttu-id="3e9e8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3e9e8-115">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="3e9e8-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3e9e8-116">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="3e9e8-117"><dt>**SB \_ Endscroll**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="3e9e8-118">Scrollvorgang beenden.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="3e9e8-119"><dt>**SB \_ Links**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-119"><dt>**SB\_LEFT**</dt> <dt>6</dt></span></span> </dl>                            | <span data-ttu-id="3e9e8-120">Scrollen Sie nach oben links.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-120">Scroll to upper left.</span></span><br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="3e9e8-121"><dt>**SB \_ Recht**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-121"><dt>**SB\_RIGHT**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="3e9e8-122">Scrollen Sie nach unten rechts.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-122">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="3e9e8-123"><dt>**SB \_ LineLeft**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-123"><dt>**SB\_LINELEFT**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="3e9e8-124">Scrollt nach links um eine Einheit.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-124">Scrolls left by one unit.</span></span><br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="3e9e8-125"><dt>**SB \_ LineRight**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-125"><dt>**SB\_LINERIGHT**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="3e9e8-126">Scrollt nach rechts um eine Einheit.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-126">Scrolls right by one unit.</span></span><br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="3e9e8-127"><dt>**SB \_ PageLeft**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-127"><dt>**SB\_PAGELEFT**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="3e9e8-128">Führt einen Bildlauf nach links um die Breite des Fensters aus.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-128">Scrolls left by the width of the window.</span></span><br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="3e9e8-129"><dt>**SB \_ PageRight**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-129"><dt>**SB\_PAGERIGHT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="3e9e8-130">Führt einen Bildlauf nach rechts um die Breite des Fensters aus.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-130">Scrolls right by the width of the window.</span></span><br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="3e9e8-131"><dt>**SB \_ Fingerposition**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-131"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="3e9e8-132">Scrollen Sie zur absoluten Position.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-132">Scroll to absolute position.</span></span> <span data-ttu-id="3e9e8-133">Die aktuelle Position wird durch das höchst wertige Wort angegeben.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-133">The current position is specified by the high-order word.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e9e8-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e9e8-134">Return value</span></span>

<span data-ttu-id="3e9e8-135">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e9e8-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e9e8-136">Remarks</span></span>

<span data-ttu-id="3e9e8-137">Der Besitzer der Zwischenablage kann mit der [**scrollwindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) -Funktion im Fenster der Zwischenablage Anzeige einen Bildlauf durchführen und den entsprechenden Bereich für ungültig erklären.</span><span class="sxs-lookup"><span data-stu-id="3e9e8-137">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9e8-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e9e8-138">Requirements</span></span>



| <span data-ttu-id="3e9e8-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e9e8-139">Requirement</span></span> | <span data-ttu-id="3e9e8-140">Wert</span><span class="sxs-lookup"><span data-stu-id="3e9e8-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9e8-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e9e8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9e8-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e9e8-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e9e8-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e9e8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9e8-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e9e8-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e9e8-145">Header</span><span class="sxs-lookup"><span data-stu-id="3e9e8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e9e8-146"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3e9e8-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9e8-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e9e8-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e9e8-148">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="3e9e8-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="3e9e8-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e9e8-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3e9e8-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e9e8-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3e9e8-151">**Licher**</span><span class="sxs-lookup"><span data-stu-id="3e9e8-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e9e8-152">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="3e9e8-152">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="3e9e8-153">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="3e9e8-153">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="3e9e8-154">[**Scrollwindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="3e9e8-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

