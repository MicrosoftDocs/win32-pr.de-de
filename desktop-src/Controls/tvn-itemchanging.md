---
title: TVN_ITEMCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich Element Attribute ändern. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- Windows-Steuerelemente für TVN_ITEMCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517825"
---
# <a name="tvn_itemchanging-notification-code"></a><span data-ttu-id="37f7b-105">TVN \_ ItemChanging-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="37f7b-105">TVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="37f7b-106">Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass sich Element Attribute ändern.</span><span class="sxs-lookup"><span data-stu-id="37f7b-106">Notifies a tree-view control's parent window that item attributes are about to change.</span></span> <span data-ttu-id="37f7b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="37f7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="37f7b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37f7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37f7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37f7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37f7b-110">Ein Zeiger auf eine [**nmtvitemchange**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) -Struktur, die das geänderte Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="37f7b-110">Pointer to an [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that is changing.</span></span> <span data-ttu-id="37f7b-111">Der **uchanged** -Member ist auf den tvif-Status festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="37f7b-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37f7b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37f7b-112">Return value</span></span>

<span data-ttu-id="37f7b-113">Gibt **false** zurück, um die Änderung zu akzeptieren, oder **true** , um die Änderung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="37f7b-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="37f7b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37f7b-114">Requirements</span></span>



| <span data-ttu-id="37f7b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37f7b-115">Requirement</span></span> | <span data-ttu-id="37f7b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="37f7b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37f7b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37f7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="37f7b-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37f7b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37f7b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37f7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="37f7b-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37f7b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37f7b-121">Header</span><span class="sxs-lookup"><span data-stu-id="37f7b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f7b-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="37f7b-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="37f7b-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="37f7b-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="37f7b-124">**TVN \_ Itemchangingw** (Unicode) und **TVN \_ itemchanginga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="37f7b-124">**TVN\_ITEMCHANGINGW** (Unicode) and **TVN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="37f7b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37f7b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f7b-126">TVN \_ ItemChanged</span><span class="sxs-lookup"><span data-stu-id="37f7b-126">TVN\_ITEMCHANGED</span></span>](tvn-itemchanged.md)
</dt> </dl>

 

 





