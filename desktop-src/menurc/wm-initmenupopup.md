---
title: WM_INITMENUPOPUP Meldung (Winuser. h)
description: Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040324"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="6c32a-105">"WM \_ initmenupopup"-Meldung</span><span class="sxs-lookup"><span data-stu-id="6c32a-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="6c32a-106">Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c32a-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="6c32a-107">Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6c32a-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="6c32a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c32a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c32a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c32a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c32a-110">Ein Handle für das Dropdown Menü oder Untermenü.</span><span class="sxs-lookup"><span data-stu-id="6c32a-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="6c32a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c32a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c32a-112">Das nieder wertige Wort gibt die null basierte relative Position des Menü Elements an, das das Dropdown Menü oder Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="6c32a-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="6c32a-113">Das höchst wertige Wort gibt an, ob das Dropdown Menü das Fenstermenü ist.</span><span class="sxs-lookup"><span data-stu-id="6c32a-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="6c32a-114">Wenn das Menü das Menü "Fenster" ist, ist dieser Parameter " **true**". Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="6c32a-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c32a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c32a-115">Return value</span></span>

<span data-ttu-id="6c32a-116">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6c32a-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c32a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c32a-117">Requirements</span></span>



| <span data-ttu-id="6c32a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c32a-118">Requirement</span></span> | <span data-ttu-id="6c32a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6c32a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c32a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c32a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c32a-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c32a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c32a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c32a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c32a-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c32a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c32a-124">Header</span><span class="sxs-lookup"><span data-stu-id="6c32a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c32a-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6c32a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c32a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c32a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c32a-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6c32a-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="6c32a-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6c32a-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6c32a-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6c32a-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6c32a-130">**WM \_ InitMenu**</span><span class="sxs-lookup"><span data-stu-id="6c32a-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="6c32a-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="6c32a-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c32a-132">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="6c32a-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

