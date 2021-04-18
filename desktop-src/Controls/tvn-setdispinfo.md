---
title: TVN_SETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- Windows-Steuerelemente für TVN_SETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338125"
---
# <a name="tvn_setdispinfo-notification-code"></a><span data-ttu-id="ce98d-105">TVN \_ setdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ce98d-105">TVN\_SETDISPINFO notification code</span></span>

<span data-ttu-id="ce98d-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ce98d-106">Notifies a tree-view control's parent window that it must update the information it maintains about an item.</span></span> <span data-ttu-id="ce98d-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ce98d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="ce98d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce98d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce98d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce98d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce98d-110">Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur, die das zu Aktualisier Ende Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ce98d-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure that describes the item being updated.</span></span> <span data-ttu-id="ce98d-111">Der **Hitem** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur gibt das Element an, das aktualisiert wird, und der **Mask** -Member gibt an, welche Attribute des Elements aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce98d-111">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure specifies the item being updated, and the **mask** member specifies which attributes of the item are being updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce98d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce98d-112">Return value</span></span>

<span data-ttu-id="ce98d-113">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ce98d-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce98d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce98d-114">Remarks</span></span>

<span data-ttu-id="ce98d-115">Wenn der **pszText** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der LPSTR- \_ textcallback-Wert ist, sendet das Steuerelement diese Benachrichtigung, um den Text des Elements festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce98d-115">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification to set the item's text.</span></span> <span data-ttu-id="ce98d-116">In diesem Fall wird für das **Mask** -Member von *LPARAM* das tvif- \_ textflag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce98d-116">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>

<span data-ttu-id="ce98d-117">Wenn das **iImage** -oder **iSelectedImage** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der I \_ imagecallback-Wert ist, sendet das Steuerelement diese Benachrichtigung, um den Index des anzuzeigenden Symbol Bilds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ce98d-117">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification to retrieve the index of the icon image to display.</span></span> <span data-ttu-id="ce98d-118">In diesem Fall wird für das **Masken** Element von *LPARAM* das tvif- \_ Image oder das tvif \_ SelectedImage-Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce98d-118">In this case, the **mask** member of *lParam* will have the TVIF\_IMAGE or TVIF\_SELECTEDIMAGE flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce98d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce98d-119">Requirements</span></span>



| <span data-ttu-id="ce98d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce98d-120">Requirement</span></span> | <span data-ttu-id="ce98d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ce98d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce98d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce98d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce98d-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce98d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce98d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce98d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce98d-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce98d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce98d-126">Header</span><span class="sxs-lookup"><span data-stu-id="ce98d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce98d-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce98d-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ce98d-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ce98d-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce98d-129">**TVN \_ Setdispinfow** (Unicode) und **TVN \_ setdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ce98d-129">**TVN\_SETDISPINFOW** (Unicode) and **TVN\_SETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ce98d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce98d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce98d-131">**Tvitem**</span><span class="sxs-lookup"><span data-stu-id="ce98d-131">**TVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[<span data-ttu-id="ce98d-132">**Tvitemex**</span><span class="sxs-lookup"><span data-stu-id="ce98d-132">**TVITEMEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[<span data-ttu-id="ce98d-133">TVN \_ getdispinfo</span><span class="sxs-lookup"><span data-stu-id="ce98d-133">TVN\_GETDISPINFO</span></span>](tvn-getdispinfo.md)
</dt> </dl>

 

 





