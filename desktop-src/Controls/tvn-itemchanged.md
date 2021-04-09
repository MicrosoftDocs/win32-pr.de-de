---
title: TVN_ITEMCHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Element Attribute geändert wurden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- Windows-Steuerelemente für TVN_ITEMCHANGED Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858934"
---
# <a name="tvn_itemchanged-notification-code"></a><span data-ttu-id="d9baf-105">TVN \_ ItemChanged-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="d9baf-105">TVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="d9baf-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass die Element Attribute geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="d9baf-106">Notifies a tree-view control's parent window that item attributes have changed.</span></span> <span data-ttu-id="d9baf-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="d9baf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d9baf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9baf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9baf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9baf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9baf-110">Zeiger auf eine [**nmtvitemchange**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) -Struktur, die das geänderte Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d9baf-110">Pointer to a [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that changed.</span></span> <span data-ttu-id="d9baf-111">Der **uchanged** -Member ist auf den tvif-Status festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="d9baf-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9baf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9baf-112">Return value</span></span>

<span data-ttu-id="d9baf-113">Gibt **false** zurück, um die Änderung zu akzeptieren, oder **true** , um die Änderung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d9baf-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9baf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9baf-114">Requirements</span></span>



| <span data-ttu-id="d9baf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9baf-115">Requirement</span></span> | <span data-ttu-id="d9baf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d9baf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9baf-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9baf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d9baf-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9baf-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9baf-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9baf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d9baf-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9baf-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9baf-121">Header</span><span class="sxs-lookup"><span data-stu-id="d9baf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9baf-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9baf-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d9baf-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="d9baf-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d9baf-124">**TVN \_ Itemchangedw** (Unicode) und **TVN \_ itemchangeda** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d9baf-124">**TVN\_ITEMCHANGEDW** (Unicode) and **TVN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d9baf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9baf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9baf-126">TVN \_ ItemChanging</span><span class="sxs-lookup"><span data-stu-id="d9baf-126">TVN\_ITEMCHANGING</span></span>](tvn-itemchanging.md)
</dt> </dl>

 

 





