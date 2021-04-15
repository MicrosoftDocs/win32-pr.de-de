---
title: LVM_SETTOOLTIPS Meldung (kommstrg. h)
description: Legt das QuickInfo-Steuerelement fest, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird. Sie können diese Nachricht explizit senden oder das ListView \_ SetToolTips-Makro verwenden.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- Windows-Steuerelemente für LVM_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476074"
---
# <a name="lvm_settooltips-message"></a><span data-ttu-id="031d1-105">LVM- \_ SetToolTips-Meldung</span><span class="sxs-lookup"><span data-stu-id="031d1-105">LVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="031d1-106">Legt das QuickInfo-Steuerelement fest, das vom Listenansicht-Steuerelement zum Anzeigen von Quick Infos verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="031d1-106">Sets the tooltip control that the list-view control will use to display tooltips.</span></span> <span data-ttu-id="031d1-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="031d1-107">You can send this message explicitly or use the [**ListView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="031d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="031d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="031d1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="031d1-110">Handle für das festzulegende QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="031d1-110">Handle to the tooltip control to be set.</span></span></dd> <dt>

<span data-ttu-id="031d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="031d1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="031d1-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="031d1-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031d1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="031d1-113">Return value</span></span>

<span data-ttu-id="031d1-114">Gibt das Handle für das vorherige QuickInfo-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="031d1-114">Returns the handle to the previous tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="031d1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="031d1-115">Requirements</span></span>



| <span data-ttu-id="031d1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="031d1-116">Requirement</span></span> | <span data-ttu-id="031d1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="031d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="031d1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="031d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="031d1-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="031d1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="031d1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="031d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="031d1-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="031d1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="031d1-122">Header</span><span class="sxs-lookup"><span data-stu-id="031d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="031d1-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="031d1-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="031d1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="031d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031d1-125">**LVM \_ gettooltips**</span><span class="sxs-lookup"><span data-stu-id="031d1-125">**LVM\_GETTOOLTIPS**</span></span>](lvm-gettooltips.md)
</dt> </dl>

 

 





