---
title: WM_ENTERMENULOOP Meldung (Winuser. h)
description: Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife eingegeben wurde.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337720"
---
# <a name="wm_entermenuloop-message"></a><span data-ttu-id="cf9b4-104">WM- \_ entermenuloop-Meldung</span><span class="sxs-lookup"><span data-stu-id="cf9b4-104">WM\_ENTERMENULOOP message</span></span>

<span data-ttu-id="cf9b4-105">Benachrichtigt die Hauptfenster Prozedur einer Anwendung, dass eine modale Menü Schleife eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-105">Notifies an application's main window procedure that a menu modal loop has been entered.</span></span>


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a><span data-ttu-id="cf9b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf9b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf9b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf9b4-108">Gibt an, ob das Menü Fenster mithilfe der [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-108">Specifies whether the window menu was entered using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function.</span></span> <span data-ttu-id="cf9b4-109">Dieser Parameter hat den Wert true, wenn das Menü Fenster mithilfe von **TrackPopupMenu** eingegeben wurde, und **false** , wenn dies nicht der **Fall** war.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-109">This parameter has a value of **TRUE** if the window menu was entered using **TrackPopupMenu**, and **FALSE** if it was not.</span></span>

</dd> <dt>

<span data-ttu-id="cf9b4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf9b4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf9b4-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9b4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf9b4-112">Return value</span></span>

<span data-ttu-id="cf9b4-113">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf9b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf9b4-114">Remarks</span></span>

<span data-ttu-id="cf9b4-115">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9b4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf9b4-116">Requirements</span></span>



| <span data-ttu-id="cf9b4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf9b4-117">Requirement</span></span> | <span data-ttu-id="cf9b4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cf9b4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9b4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf9b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9b4-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf9b4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cf9b4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf9b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9b4-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf9b4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cf9b4-123">Header</span><span class="sxs-lookup"><span data-stu-id="cf9b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf9b4-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="cf9b4-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf9b4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf9b4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf9b4-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cf9b4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf9b4-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="cf9b4-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="cf9b4-128">**WM- \_ exitmenuloop**</span><span class="sxs-lookup"><span data-stu-id="cf9b4-128">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
</dt> <dt>

<span data-ttu-id="cf9b4-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="cf9b4-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cf9b4-130">Menüs</span><span class="sxs-lookup"><span data-stu-id="cf9b4-130">Menus</span></span>](menus.md)
</dt> </dl>

 

