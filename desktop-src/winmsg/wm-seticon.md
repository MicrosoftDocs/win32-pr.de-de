---
description: Ordnet ein neues großes oder kleines Symbol einem Fenster zu. Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: WM_SETICON Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216040"
---
# <a name="wm_seticon-message"></a><span data-ttu-id="da6e4-104">WM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="da6e4-104">WM\_SETICON message</span></span>

<span data-ttu-id="da6e4-105">Ordnet ein neues großes oder kleines Symbol einem Fenster zu.</span><span class="sxs-lookup"><span data-stu-id="da6e4-105">Associates a new large or small icon with a window.</span></span> <span data-ttu-id="da6e4-106">Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.</span><span class="sxs-lookup"><span data-stu-id="da6e4-106">The system displays the large icon in the ALT+TAB dialog box, and the small icon in the window caption.</span></span>


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a><span data-ttu-id="da6e4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="da6e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da6e4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da6e4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da6e4-109">Der Typ des festzulegenden Symbols.</span><span class="sxs-lookup"><span data-stu-id="da6e4-109">The type of icon to be set.</span></span> <span data-ttu-id="da6e4-110">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="da6e4-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="da6e4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="da6e4-111">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="da6e4-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="da6e4-112">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="da6e4-113"><dt>**Symbol \_ Big**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="da6e4-113"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="da6e4-114">Legen Sie das große Symbol für das Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="da6e4-114">Set the large icon for the window.</span></span><br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="da6e4-115"><dt>**Symbol \_ Kleiner**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="da6e4-115"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="da6e4-116">Legen Sie das kleine Symbol für das Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="da6e4-116">Set the small icon for the window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="da6e4-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da6e4-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da6e4-118">Ein Handle für das neue große oder kleine Symbol.</span><span class="sxs-lookup"><span data-stu-id="da6e4-118">A handle to the new large or small icon.</span></span> <span data-ttu-id="da6e4-119">Wenn dieser Parameter **null** ist, wird das Symbol entfernt, das von *wParam* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da6e4-119">If this parameter is **NULL**, the icon indicated by *wParam* is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da6e4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da6e4-120">Return value</span></span>

<span data-ttu-id="da6e4-121">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="da6e4-121">Type: **LRESULT**</span></span>

<span data-ttu-id="da6e4-122">Der Rückgabewert ist ein Handle für das vorherige große oder kleine Symbol, abhängig vom Wert von *wParam*.</span><span class="sxs-lookup"><span data-stu-id="da6e4-122">The return value is a handle to the previous large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="da6e4-123">Der Wert ist **null** , wenn das Fenster zuvor kein Symbol des Typs enthielt, der von *wParam* angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="da6e4-123">It is **NULL** if the window previously had no icon of the type indicated by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="da6e4-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da6e4-124">Remarks</span></span>

<span data-ttu-id="da6e4-125">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt ein Handle für das vorherige große oder kleine Symbol zurück, das dem Fenster zugeordnet ist, je nach Wert von *wParam*.</span><span class="sxs-lookup"><span data-stu-id="da6e4-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns a handle to the previous large or small icon associated with the window, depending on the value of *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="da6e4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da6e4-126">Requirements</span></span>



| <span data-ttu-id="da6e4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da6e4-127">Requirement</span></span> | <span data-ttu-id="da6e4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="da6e4-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da6e4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da6e4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="da6e4-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da6e4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="da6e4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da6e4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="da6e4-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da6e4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da6e4-133">Header</span><span class="sxs-lookup"><span data-stu-id="da6e4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="da6e4-134"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="da6e4-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da6e4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da6e4-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="da6e4-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="da6e4-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da6e4-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="da6e4-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="da6e4-138">**WM- \_ getIcon**</span><span class="sxs-lookup"><span data-stu-id="da6e4-138">**WM\_GETICON**</span></span>](wm-geticon.md)
</dt> <dt>

<span data-ttu-id="da6e4-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="da6e4-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="da6e4-140">Windows</span><span class="sxs-lookup"><span data-stu-id="da6e4-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
