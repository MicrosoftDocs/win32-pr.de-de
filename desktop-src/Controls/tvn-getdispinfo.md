---
title: TVN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Fordert an, dass das übergeordnete Fenster eines Strukturansicht-Steuer Elements Informationen bereitstellt, die zum Anzeigen oder Sortieren eines Elements erforderlich sind. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- Windows-Steuerelemente für TVN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a09bcc683ba9cf2d89a796e63812381254588a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517828"
---
# <a name="tvn_getdispinfo-notification-code"></a><span data-ttu-id="5a8aa-105">TVN \_ getdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="5a8aa-105">TVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="5a8aa-106">Fordert an, dass das übergeordnete Fenster eines Strukturansicht-Steuer Elements Informationen bereitstellt, die zum Anzeigen oder Sortieren eines Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-106">Requests that a tree-view control's parent window provide information needed to display or sort an item.</span></span> <span data-ttu-id="5a8aa-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="5a8aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a8aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a8aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a8aa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a8aa-110">Zeiger auf eine [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="5a8aa-111">Das **Element Element** ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, deren " **Mask**", " **Hitem**", " **State**" und " **LPARAM** "-Member den Typ der erforderlichen Informationen angeben.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure whose **mask**, **hItem**, **state**, and **lParam** members specify the type of information required.</span></span> <span data-ttu-id="5a8aa-112">Sie müssen die Elemente der Struktur mit den entsprechenden Informationen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-112">You must fill the members of the structure with the appropriate information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a8aa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a8aa-113">Return value</span></span>

<span data-ttu-id="5a8aa-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a8aa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a8aa-115">Remarks</span></span>

<span data-ttu-id="5a8aa-116">Dieser Benachrichtigungs Code wird in den folgenden Situationen gesendet:</span><span class="sxs-lookup"><span data-stu-id="5a8aa-116">This notification code is sent under the following circumstances:</span></span>

-   <span data-ttu-id="5a8aa-117">Wenn der **pszText** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der LPSTR- \_ textcallback-Wert ist, sendet das Steuerelement diesen Benachrichtigungs Code, um den Text des Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-117">If the **pszText** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the LPSTR\_TEXTCALLBACK value, the control sends this notification code to retrieve the item's text.</span></span> <span data-ttu-id="5a8aa-118">In diesem Fall wird für das **Mask** -Member von *LPARAM* das tvif- \_ textflag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-118">In this case, the **mask** member of *lParam* will have the TVIF\_TEXT flag set.</span></span>
-   <span data-ttu-id="5a8aa-119">Wenn das **iImage** -oder **iSelectedImage** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der I \_ imagecallback-Wert ist, sendet das Steuerelement diesen Benachrichtigungs Code, um den Index der Symbole eines Elements in der Bildliste des Steuer Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-119">If the **iImage** or **iSelectedImage** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_IMAGECALLBACK value, the control sends this notification code to retrieve the index of an item's icons in the control's image list.</span></span> <span data-ttu-id="5a8aa-120">In diesem Fall wird das tvif SelectedImage-Flag für das **Masken** Element von *LPARAM* festgelegt, wenn das Element ausgewählt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="5a8aa-120">In this case, if the item is selected, the **mask** member of *lParam* will have the TVIF\_SELECTEDIMAGE flag set.</span></span> <span data-ttu-id="5a8aa-121">Wenn das Element nicht ausgewählt ist, wird für das **Mask** -Member von *LPARAM* das tvif- \_ bildflag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-121">If the item is not selected, the **mask** member of *lParam* will have the TVIF\_IMAGE flag set.</span></span>
-   <span data-ttu-id="5a8aa-122">Wenn das **cChildren** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur des Elements der I \_ Children encallback-Wert ist, sendet das Steuerelement diesen Benachrichtigungs Code, um einen Wert abzurufen, der angibt, ob das Element über untergeordnete Elemente verfügt.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-122">If the **cChildren** member of the item's [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure is the I\_CHILDRENCALLBACK value, the control sends this notification code to retrieve a value that indicates whether the item has child items.</span></span> <span data-ttu-id="5a8aa-123">In diesem Fall wird für das **Mask** -Member von *LPARAM* das Flag "tvif \_ Children" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a8aa-123">In this case, the **mask** member of *lParam* will have the TVIF\_CHILDREN flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a8aa-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a8aa-124">Requirements</span></span>



| <span data-ttu-id="5a8aa-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a8aa-125">Requirement</span></span> | <span data-ttu-id="5a8aa-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5a8aa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8aa-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a8aa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5a8aa-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a8aa-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a8aa-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a8aa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5a8aa-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a8aa-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a8aa-131">Header</span><span class="sxs-lookup"><span data-stu-id="5a8aa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a8aa-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a8aa-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5a8aa-133">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5a8aa-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5a8aa-134">**TVN \_ Getdispinfow** (Unicode) und **TVN \_ getdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5a8aa-134">**TVN\_GETDISPINFOW** (Unicode) and **TVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5a8aa-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a8aa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8aa-136">TVN \_ setdispinfo</span><span class="sxs-lookup"><span data-stu-id="5a8aa-136">TVN\_SETDISPINFO</span></span>](tvn-setdispinfo.md)
</dt> </dl>

 

 





