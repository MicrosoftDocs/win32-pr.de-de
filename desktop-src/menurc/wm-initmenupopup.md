---
title: WM_INITMENUPOPUP-Nachricht (Winuser.h)
description: 'WM_INITMENUPOPUP Meldung: Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.'
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP Meldung Menüs und andere Ressourcen
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
ms.openlocfilehash: 6d850547d57596dd36b36b941d1782c2aee1f5b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092518"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="18073-105">WM \_ INITMENUPOPUP-Nachricht</span><span class="sxs-lookup"><span data-stu-id="18073-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="18073-106">Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="18073-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="18073-107">Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern.</span><span class="sxs-lookup"><span data-stu-id="18073-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="18073-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="18073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18073-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18073-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18073-110">Ein Handle für das Dropdownmenü oder untermenü.</span><span class="sxs-lookup"><span data-stu-id="18073-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="18073-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18073-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18073-112">Das Wort mit niedriger Reihenfolge gibt die nullbasierte relative Position des Menüelements an, das das Dropdownmenü oder Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="18073-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="18073-113">Das Wort in hoher Reihenfolge gibt an, ob das Dropdownmenü das Fenstermenü ist.</span><span class="sxs-lookup"><span data-stu-id="18073-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="18073-114">Wenn das Menü das Fenstermenü ist, ist dieser Parameter **TRUE.** Andernfalls ist es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="18073-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18073-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18073-115">Return value</span></span>

<span data-ttu-id="18073-116">Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="18073-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="18073-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18073-117">Requirements</span></span>



| <span data-ttu-id="18073-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18073-118">Requirement</span></span> | <span data-ttu-id="18073-119">Wert</span><span class="sxs-lookup"><span data-stu-id="18073-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18073-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18073-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18073-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18073-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="18073-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18073-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18073-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18073-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18073-124">Header</span><span class="sxs-lookup"><span data-stu-id="18073-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18073-125"><dt>Winuser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="18073-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18073-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="18073-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="18073-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="18073-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="18073-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18073-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="18073-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18073-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="18073-130">**WM \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="18073-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="18073-131">**Konzept**</span><span class="sxs-lookup"><span data-stu-id="18073-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18073-132">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="18073-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

