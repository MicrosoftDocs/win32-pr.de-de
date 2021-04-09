---
title: WM_GESTURENOTIFY Meldung (Winuser. h)
description: Gibt Ihnen die Möglichkeit, die Gesten Konfiguration festzulegen.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- Windows-Fingereingabe für WM_GESTURENOTIFY Meldung
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104529"
---
# <a name="wm_gesturenotify-message"></a><span data-ttu-id="0d513-104">WM \_ gesturenotify-Meldung</span><span class="sxs-lookup"><span data-stu-id="0d513-104">WM\_GESTURENOTIFY message</span></span>

<span data-ttu-id="0d513-105">Gibt Ihnen die Möglichkeit, die Gesten Konfiguration festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0d513-105">Gives you a chance to set the gesture configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d513-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d513-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d513-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d513-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d513-108">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d513-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="0d513-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d513-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d513-110">Ein Zeiger auf eine [**gesturenotifystruct**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span><span class="sxs-lookup"><span data-stu-id="0d513-110">A pointer to a [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d513-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d513-111">Return value</span></span>

<span data-ttu-id="0d513-112">Von [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)sollte ein Wert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d513-112">A value should be returned from [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d513-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d513-113">Remarks</span></span>

<span data-ttu-id="0d513-114">Wenn die **WM- \_ gesturenotify** -Nachricht empfangen wird, kann die Anwendung [**setgestureconfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) verwenden, um die zu empfangenden Gesten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0d513-114">When the **WM\_GESTURENOTIFY** message is received, the application can use [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) to specify the gestures to receive.</span></span> <span data-ttu-id="0d513-115">Diese Nachricht sollte immer mit der [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion zusammengefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0d513-115">This message should always be bubbled up using the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="0d513-116">Durch die Verarbeitung der " **\_ gesturenotify** "-Meldung wird die Gesten Konfiguration für die Lebensdauer des Fensters und nicht nur für die nächste Geste geändert.</span><span class="sxs-lookup"><span data-stu-id="0d513-116">Handling the **WM\_GESTURENOTIFY** message will change the gesture configuration for the lifetime of the Window, not just for the next gesture.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0d513-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d513-117">Examples</span></span>

<span data-ttu-id="0d513-118">Im folgenden Beispiel wird gezeigt, wie alle Gesten aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0d513-118">The following example shows how to enable all gestures.</span></span> <span data-ttu-id="0d513-119">Weitere Beispiele finden Sie unter [**setgestureconfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span><span class="sxs-lookup"><span data-stu-id="0d513-119">For more examples, see [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span></span>


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a><span data-ttu-id="0d513-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d513-120">Requirements</span></span>



| <span data-ttu-id="0d513-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d513-121">Requirement</span></span> | <span data-ttu-id="0d513-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0d513-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d513-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d513-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d513-124">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d513-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="0d513-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d513-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d513-126">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d513-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="0d513-127">Header</span><span class="sxs-lookup"><span data-stu-id="0d513-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d513-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0d513-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d513-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d513-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d513-130">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="0d513-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0d513-131">Programmier Handbuch für Windows-Touchgesten</span><span class="sxs-lookup"><span data-stu-id="0d513-131">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="0d513-132">**Gesturenotifystruct**</span><span class="sxs-lookup"><span data-stu-id="0d513-132">**GESTURENOTIFYSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[<span data-ttu-id="0d513-133">**Setgestureconfig**</span><span class="sxs-lookup"><span data-stu-id="0d513-133">**SetGestureConfig**</span></span>](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

