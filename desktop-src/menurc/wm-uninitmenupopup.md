---
title: WM_UNINITMENUPOPUP Meldung (Winuser. h)
description: Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü zerstört wurde.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519191"
---
# <a name="wm_uninitmenupopup-message"></a><span data-ttu-id="48815-104">\_Uninitmenupopup-Meldung der WM</span><span class="sxs-lookup"><span data-stu-id="48815-104">WM\_UNINITMENUPOPUP message</span></span>

<span data-ttu-id="48815-105">Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="48815-105">Sent when a drop-down menu or submenu has been destroyed.</span></span>


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a><span data-ttu-id="48815-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48815-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48815-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48815-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48815-108">Ein Handle für das Menü.</span><span class="sxs-lookup"><span data-stu-id="48815-108">A handle to the menu</span></span>

</dd> <dt>

<span data-ttu-id="48815-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48815-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48815-110">Das hochwertige Wort identifiziert das Menü, das zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="48815-110">The high-order word identifies the menu that was destroyed.</span></span> <span data-ttu-id="48815-111">Dieser Parameter kann derzeit nur als **MF- \_ sysmenu** (Menü Fenster) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="48815-111">Currently, this parameter can only be **MF\_SYSMENU** (the window menu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48815-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48815-112">Remarks</span></span>

<span data-ttu-id="48815-113">Wenn eine Anwendung eine " [**WM \_ initmenupopup**](wm-initmenupopup.md) "-Meldung empfängt, wird eine " **WM \_ uninitmenupopup** "-Meldung empfangen.</span><span class="sxs-lookup"><span data-stu-id="48815-113">If an application receives a [**WM\_INITMENUPOPUP**](wm-initmenupopup.md) message, it will receive a **WM\_UNINITMENUPOPUP** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="48815-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48815-114">Requirements</span></span>



| <span data-ttu-id="48815-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48815-115">Requirement</span></span> | <span data-ttu-id="48815-116">Wert</span><span class="sxs-lookup"><span data-stu-id="48815-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48815-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48815-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48815-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48815-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="48815-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48815-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48815-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48815-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48815-121">Header</span><span class="sxs-lookup"><span data-stu-id="48815-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="48815-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="48815-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48815-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48815-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="48815-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="48815-124">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="48815-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48815-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="48815-126">**Licher**</span><span class="sxs-lookup"><span data-stu-id="48815-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="48815-127">Menüs</span><span class="sxs-lookup"><span data-stu-id="48815-127">Menus</span></span>](menus.md)
</dt> </dl>

 

