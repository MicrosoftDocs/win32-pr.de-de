---
Description: Wird als Signal gesendet, dass ein Fenster oder eine Anwendung beendet werden soll.
ms.assetid: 19500baf-e0ad-4dfa-804f-6a6e0652cffb
title: WM_CLOSE Meldung (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2f1403050cfd3c98ddf90df4399547158a583c50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357713"
---
# <a name="wm_close-message"></a><span data-ttu-id="60c66-103">Meldung zum Schließen der WM \_</span><span class="sxs-lookup"><span data-stu-id="60c66-103">WM\_CLOSE message</span></span>

<span data-ttu-id="60c66-104">Wird als Signal gesendet, dass ein Fenster oder eine Anwendung beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60c66-104">Sent as a signal that a window or an application should terminate.</span></span>

<span data-ttu-id="60c66-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="60c66-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CLOSE                        0x0010
```



## <a name="parameters"></a><span data-ttu-id="60c66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60c66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60c66-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60c66-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60c66-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60c66-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="60c66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60c66-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60c66-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="60c66-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60c66-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60c66-111">Return value</span></span>

<span data-ttu-id="60c66-112">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="60c66-112">Type: **LRESULT**</span></span>

<span data-ttu-id="60c66-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="60c66-113">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="60c66-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60c66-114">Example</span></span>

```cpp
LRESULT CALLBACK WindowProc(
    __in HWND hWindow,
    __in UINT uMsg,
    __in WPARAM wParam,
    __in LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CLOSE:
        DestroyWindow(hWindow);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWindow, uMsg, wParam, lParam);
    }

    return 0;
}
```
<span data-ttu-id="60c66-115">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="60c66-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="60c66-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60c66-116">Remarks</span></span>

<span data-ttu-id="60c66-117">Eine Anwendung kann den Benutzer vor dem Zerstören eines Fensters zur Bestätigung auffordern, indem er die Meldung **zum \_ Schließen der WM** verarbeitet und die Funktion " [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) " nur dann aufruft, wenn der Benutzer die Auswahl bestätigt.</span><span class="sxs-lookup"><span data-stu-id="60c66-117">An application can prompt the user for confirmation, prior to destroying a window, by processing the **WM\_CLOSE** message and calling the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function only if the user confirms the choice.</span></span>

<span data-ttu-id="60c66-118">Standardmäßig ruft die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion auf, um das Fenster zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="60c66-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function calls the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="60c66-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60c66-119">Requirements</span></span>



| <span data-ttu-id="60c66-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60c66-120">Requirement</span></span> | <span data-ttu-id="60c66-121">Wert</span><span class="sxs-lookup"><span data-stu-id="60c66-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c66-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60c66-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60c66-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60c66-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="60c66-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60c66-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60c66-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60c66-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="60c66-126">Header</span><span class="sxs-lookup"><span data-stu-id="60c66-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="60c66-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="60c66-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c66-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60c66-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="60c66-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="60c66-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="60c66-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="60c66-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="60c66-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="60c66-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

<span data-ttu-id="60c66-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="60c66-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="60c66-133">Windows</span><span class="sxs-lookup"><span data-stu-id="60c66-133">Windows</span></span>](windows.md)
</dt> </dl>

 

 
