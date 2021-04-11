---
title: TVN_ITEMEXPANDED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- Windows-Steuerelemente für TVN_ITEMEXPANDED Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105945"
---
# <a name="tvn_itemexpanded-notification-code"></a><span data-ttu-id="17860-105">TVN \_ itemexpanded-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="17860-105">TVN\_ITEMEXPANDED notification code</span></span>

<span data-ttu-id="17860-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert wurde.</span><span class="sxs-lookup"><span data-stu-id="17860-106">Notifies a tree-view control's parent window that a parent item's list of child items has expanded or collapsed.</span></span> <span data-ttu-id="17860-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="17860-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="17860-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17860-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17860-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17860-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17860-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="17860-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="17860-111">Der **itemnew** -Member ist eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die gültige Informationen über das übergeordnete Element in den Elementen " **Hitem**", " **State**" und " **LPARAM** " enthält.</span><span class="sxs-lookup"><span data-stu-id="17860-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="17860-112">Der **Aktionsmember** gibt an, ob die Liste erweitert oder reduziert wurde.</span><span class="sxs-lookup"><span data-stu-id="17860-112">The **action** member indicates whether the list expanded or collapsed.</span></span> <span data-ttu-id="17860-113">Eine Liste möglicher Werte finden Sie in der Beschreibung der [**TVM \_ Expand**](tvm-expand.md) Message.</span><span class="sxs-lookup"><span data-stu-id="17860-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17860-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17860-114">Return value</span></span>

<span data-ttu-id="17860-115">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="17860-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="17860-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17860-116">Requirements</span></span>



| <span data-ttu-id="17860-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17860-117">Requirement</span></span> | <span data-ttu-id="17860-118">Wert</span><span class="sxs-lookup"><span data-stu-id="17860-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17860-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17860-119">Minimum supported client</span></span><br/> | <span data-ttu-id="17860-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17860-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17860-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17860-121">Minimum supported server</span></span><br/> | <span data-ttu-id="17860-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17860-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17860-123">Header</span><span class="sxs-lookup"><span data-stu-id="17860-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="17860-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="17860-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="17860-125">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="17860-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="17860-126">**TVN \_ Itemexpandedw** (Unicode) und **TVN \_ itemexpandeda** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="17860-126">**TVN\_ITEMEXPANDEDW** (Unicode) and **TVN\_ITEMEXPANDEDA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="17860-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17860-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17860-128">TVN \_ itemexpanding</span><span class="sxs-lookup"><span data-stu-id="17860-128">TVN\_ITEMEXPANDING</span></span>](tvn-itemexpanding.md)
</dt> </dl>

 

 





