---
title: WM_VSCROLLCLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF \_ -Besitzer Anzeige Format enthält und ein Ereignis auf der vertikalen Schiebe Leiste der Zwischenablage Anzeige auftritt.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477175"
---
# <a name="wm_vscrollclipboard-message"></a><span data-ttu-id="c190a-104">WM \_ vscrollclipboard-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c190a-104">WM\_VSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="c190a-105">Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF-Besitzer Anzeige Format enthält und ein Ereignis auf der vertikalen Schiebe Leiste der Zwischenablage [**\_ Anzeige**](standard-clipboard-formats.md) auftritt.</span><span class="sxs-lookup"><span data-stu-id="c190a-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's vertical scroll bar.</span></span> <span data-ttu-id="c190a-106">Der Besitzer sollte das Zwischenablage Bild scrollen und die ScrollBar-Werte aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c190a-106">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a><span data-ttu-id="c190a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c190a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c190a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c190a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c190a-109">Ein Handle für das Fenster der Zwischenablage Anzeige.</span><span class="sxs-lookup"><span data-stu-id="c190a-109">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="c190a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c190a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c190a-111">Das nieder wertige Wort von *LPARAM* gibt ein ScrollBar-Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="c190a-111">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="c190a-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c190a-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c190a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c190a-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="c190a-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c190a-114">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="c190a-115"><dt>**SB \_ Unten**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-115"><dt>**SB\_BOTTOM**</dt> <dt>7</dt></span></span> </dl>                      | <span data-ttu-id="c190a-116">Scrollen Sie nach unten rechts.</span><span class="sxs-lookup"><span data-stu-id="c190a-116">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="c190a-117"><dt>**SB \_ Endscroll**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="c190a-118">Scrollvorgang beenden.</span><span class="sxs-lookup"><span data-stu-id="c190a-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="c190a-119"><dt>**SB \_ LineDown**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-119"><dt>**SB\_LINEDOWN**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="c190a-120">Scrollen Sie in eine Zeile nach unten.</span><span class="sxs-lookup"><span data-stu-id="c190a-120">Scroll one line down.</span></span><br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="c190a-121"><dt>**SB \_ Lineup**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-121"><dt>**SB\_LINEUP**</dt> <dt>0</dt></span></span> </dl>                      | <span data-ttu-id="c190a-122">Scrollen Sie in einer Zeile nach oben.</span><span class="sxs-lookup"><span data-stu-id="c190a-122">Scroll one line up.</span></span><br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="c190a-123"><dt>**SB \_ PageDown**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-123"><dt>**SB\_PAGEDOWN**</dt> <dt>3</dt></span></span> </dl>                | <span data-ttu-id="c190a-124">Scrollen Sie eine Seite nach unten.</span><span class="sxs-lookup"><span data-stu-id="c190a-124">Scroll one page down.</span></span><br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="c190a-125"><dt>**SB \_ PageUp**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-125"><dt>**SB\_PAGEUP**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="c190a-126">Scrollen Sie eine Seite nach oben.</span><span class="sxs-lookup"><span data-stu-id="c190a-126">Scroll one page up.</span></span><br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="c190a-127"><dt>**SB \_ Fingerposition**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-127"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="c190a-128">Scrollen Sie zur absoluten Position.</span><span class="sxs-lookup"><span data-stu-id="c190a-128">Scroll to absolute position.</span></span> <span data-ttu-id="c190a-129">Die aktuelle Position wird durch das höchst wertige Wort angegeben.</span><span class="sxs-lookup"><span data-stu-id="c190a-129">The current position is specified by the high-order word.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="c190a-130"><dt>**SB \_ Top**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-130"><dt>**SB\_TOP**</dt> <dt>6</dt></span></span> </dl>                               | <span data-ttu-id="c190a-131">Scrollen Sie nach oben links.</span><span class="sxs-lookup"><span data-stu-id="c190a-131">Scroll to upper left.</span></span><br/>                                                                  |



 

<span data-ttu-id="c190a-132">Das aktuellste Wort von *LPARAM* gibt die aktuelle Position des Bild Lauf Felds an, wenn es sich bei dem nieder wertigen Wort von *LPARAM* um **SB- \_ Fingerposition** handelt. andernfalls wird das höherwertige Wort von *LPARAM* nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c190a-132">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word of *lParam* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c190a-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c190a-133">Return value</span></span>

<span data-ttu-id="c190a-134">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c190a-134">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c190a-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c190a-135">Remarks</span></span>

<span data-ttu-id="c190a-136">Der Besitzer der Zwischenablage kann mit der [**scrollwindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) -Funktion im Fenster der Zwischenablage Anzeige einen Bildlauf durchführen und den entsprechenden Bereich für ungültig erklären.</span><span class="sxs-lookup"><span data-stu-id="c190a-136">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="c190a-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c190a-137">Requirements</span></span>



| <span data-ttu-id="c190a-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c190a-138">Requirement</span></span> | <span data-ttu-id="c190a-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c190a-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c190a-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c190a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c190a-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c190a-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c190a-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c190a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c190a-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c190a-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c190a-144">Header</span><span class="sxs-lookup"><span data-stu-id="c190a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c190a-145"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c190a-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c190a-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c190a-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="c190a-147">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c190a-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="c190a-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c190a-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c190a-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c190a-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c190a-150">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c190a-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c190a-151">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="c190a-151">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="c190a-152">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c190a-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c190a-153">[**Scrollwindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="c190a-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

