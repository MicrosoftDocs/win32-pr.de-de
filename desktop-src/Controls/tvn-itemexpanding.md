---
title: TVN_ITEMEXPANDING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements gerade erweitert oder reduziert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- Windows-Steuerelemente für TVN_ITEMEXPANDING Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957091"
---
# <a name="tvn_itemexpanding-notification-code"></a><span data-ttu-id="ed10b-105">TVN \_ itemexpandingbenachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="ed10b-105">TVN\_ITEMEXPANDING notification code</span></span>

<span data-ttu-id="ed10b-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements gerade erweitert oder reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="ed10b-106">Notifies a tree-view control's parent window that a parent item's list of child items is about to expand or collapse.</span></span> <span data-ttu-id="ed10b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ed10b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="ed10b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed10b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed10b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed10b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed10b-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ed10b-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="ed10b-111">Der **itemnew** -Member ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen über das übergeordnete Element in den Elementen " **Hitem**", " **State**" und " **LPARAM** " enthält.</span><span class="sxs-lookup"><span data-stu-id="ed10b-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="ed10b-112">Der **Aktionsmember** gibt an, ob die Liste erweitert oder reduziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed10b-112">The **action** member indicates whether the list is to expand or collapse.</span></span> <span data-ttu-id="ed10b-113">Eine Liste möglicher Werte finden Sie in der Beschreibung der [**TVM \_ Expand**](tvm-expand.md) Message.</span><span class="sxs-lookup"><span data-stu-id="ed10b-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed10b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed10b-114">Return value</span></span>

<span data-ttu-id="ed10b-115">Gibt **true** zurück, um zu verhindern, dass die Liste erweitert oder reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="ed10b-115">Returns **TRUE** to prevent the list from expanding or collapsing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed10b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed10b-116">Requirements</span></span>



| <span data-ttu-id="ed10b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed10b-117">Requirement</span></span> | <span data-ttu-id="ed10b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ed10b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed10b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed10b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ed10b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed10b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed10b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed10b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ed10b-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed10b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed10b-123">Header</span><span class="sxs-lookup"><span data-stu-id="ed10b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed10b-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed10b-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ed10b-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ed10b-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ed10b-126">**TVN \_ Itemexpandingw** (Unicode) und **TVN \_ itemexpandinga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ed10b-126">**TVN\_ITEMEXPANDINGW** (Unicode) and **TVN\_ITEMEXPANDINGA** (ANSI)</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ed10b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed10b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed10b-128">TVN \_ itemexpanded</span><span class="sxs-lookup"><span data-stu-id="ed10b-128">TVN\_ITEMEXPANDED</span></span>](tvn-itemexpanded.md)
</dt> </dl>

 

 





