---
Description: Wird an ein Fenster gesendet, nachdem sich die Größe geändert hat.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: WM_SIZE Meldung (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362173"
---
# <a name="wm_size-message"></a><span data-ttu-id="5521c-103">WM- \_ Größen Meldung</span><span class="sxs-lookup"><span data-stu-id="5521c-103">WM\_SIZE message</span></span>

<span data-ttu-id="5521c-104">Wird an ein Fenster gesendet, nachdem sich die Größe geändert hat.</span><span class="sxs-lookup"><span data-stu-id="5521c-104">Sent to a window after its size has changed.</span></span>

<span data-ttu-id="5521c-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5521c-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a><span data-ttu-id="5521c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5521c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5521c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5521c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5521c-108">Der Typ der angeforderten Größe der Größe.</span><span class="sxs-lookup"><span data-stu-id="5521c-108">The type of resizing requested.</span></span> <span data-ttu-id="5521c-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="5521c-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5521c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5521c-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="5521c-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5521c-111">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <span data-ttu-id="5521c-112"><dt>**Größe \_ Maxhide**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5521c-112"><dt>**SIZE\_MAXHIDE**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="5521c-113">Die Nachricht wird an alle Popup Fenster gesendet, wenn ein anderes Fenster maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="5521c-113">Message is sent to all pop-up windows when some other window is maximized.</span></span><br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <span data-ttu-id="5521c-114"><dt>**Größe \_ Maximiert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5521c-114"><dt>**SIZE\_MAXIMIZED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="5521c-115">Das Fenster wurde maximiert.</span><span class="sxs-lookup"><span data-stu-id="5521c-115">The window has been maximized.</span></span><br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <span data-ttu-id="5521c-116"><dt>**Größe \_ Maxshow**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5521c-116"><dt>**SIZE\_MAXSHOW**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="5521c-117">Die Nachricht wird an alle Popup Fenster gesendet, wenn ein anderes Fenster auf die frühere Größe wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5521c-117">Message is sent to all pop-up windows when some other window has been restored to its former size.</span></span><br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <span data-ttu-id="5521c-118"><dt>**Größe \_ Minimiert**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5521c-118"><dt>**SIZE\_MINIMIZED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="5521c-119">Das Fenster wurde minimiert.</span><span class="sxs-lookup"><span data-stu-id="5521c-119">The window has been minimized.</span></span><br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <span data-ttu-id="5521c-120"><dt>**Größe \_ Wieder hergestellt**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5521c-120"><dt>**SIZE\_RESTORED**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="5521c-121">Die Größe des Fensters wurde geändert, aber weder die **\_ minimierte Größe** noch die **Größe des \_ maximierten** Werts.</span><span class="sxs-lookup"><span data-stu-id="5521c-121">The window has been resized, but neither the **SIZE\_MINIMIZED** nor **SIZE\_MAXIMIZED** value applies.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5521c-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5521c-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5521c-123">Das nieder wertige Wort von *LPARAM* gibt die neue Breite des Client Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="5521c-123">The low-order word of *lParam* specifies the new width of the client area.</span></span>

<span data-ttu-id="5521c-124">Das hochwertige Wort von *LPARAM* gibt die neue Höhe des Client Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="5521c-124">The high-order word of *lParam* specifies the new height of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5521c-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5521c-125">Return value</span></span>

<span data-ttu-id="5521c-126">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5521c-126">Type: **LRESULT**</span></span>

<span data-ttu-id="5521c-127">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5521c-127">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="5521c-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5521c-128">Example</span></span>

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

<span data-ttu-id="5521c-129">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="5521c-129">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="5521c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5521c-130">Remarks</span></span>

<span data-ttu-id="5521c-131">Wenn die Funktion " [**setscrollpos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) " oder " [**muvewindow**](/windows/win32/api/winuser/nf-winuser-movewindow) " als Ergebnis der **WM- \_ Größen** Meldung für ein untergeordnetes Fenster aufgerufen wird, sollte der *bredraw* -Parameter oder der *brepaint* -Parameter nicht NULL sein, damit das Fenster neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5521c-131">If the [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) or [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function is called for a child window as a result of the **WM\_SIZE** message, the *bRedraw* or *bRepaint* parameter should be nonzero to cause the window to be repainted.</span></span>

<span data-ttu-id="5521c-132">Obwohl die Breite und Höhe eines Fensters 32-Bit-Werte ist, enthält der *LPARAM* -Parameter nur die nieder wertigen 16 Bits der einzelnen Werte.</span><span class="sxs-lookup"><span data-stu-id="5521c-132">Although the width and height of a window are 32-bit values, the *lParam* parameter contains only the low-order 16 bits of each.</span></span>

<span data-ttu-id="5521c-133">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet die **WM- \_ Größe** und die WM-Verschiebungs Nachricht, wenn Sie die [**WM- \_ windowposchge**](wm-windowposchanged.md) -Nachricht verarbeitet. **\_**</span><span class="sxs-lookup"><span data-stu-id="5521c-133">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="5521c-134">Die **WM- \_ Größe** und die WM-Verschiebungs Nachricht werden nicht gesendet, wenn eine Anwendung die **WM- \_ windowposchangsnachricht** verarbeitet, ohne **defwindowproc** Aufrufs. **\_**</span><span class="sxs-lookup"><span data-stu-id="5521c-134">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5521c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5521c-135">Requirements</span></span>



| <span data-ttu-id="5521c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5521c-136">Requirement</span></span> | <span data-ttu-id="5521c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5521c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5521c-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5521c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5521c-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5521c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5521c-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5521c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5521c-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5521c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5521c-142">Header</span><span class="sxs-lookup"><span data-stu-id="5521c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5521c-143"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5521c-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5521c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5521c-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="5521c-145">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5521c-145">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="5521c-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5521c-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5521c-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5521c-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5521c-148">**Fenster**</span><span class="sxs-lookup"><span data-stu-id="5521c-148">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="5521c-149">**WM-Windows-Server \_**</span><span class="sxs-lookup"><span data-stu-id="5521c-149">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="5521c-150">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5521c-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5521c-151">Windows</span><span class="sxs-lookup"><span data-stu-id="5521c-151">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="5521c-152">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5521c-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="5521c-153">[**Setscrollpos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="5521c-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

 
