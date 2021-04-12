---
title: HDM_CLEARFILTER Meldung (kommstrg. h)
description: Löscht den Filter für ein bestimmtes Header-Steuerelement. Sie können diese Nachricht explizit senden oder das Header \_ ClearFilter-Makro verwenden.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Windows-Steuerelemente für HDM_CLEARFILTER Meldung
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104492"
---
# <a name="hdm_clearfilter-message"></a><span data-ttu-id="829e3-105">HDM \_ ClearFilter-Meldung</span><span class="sxs-lookup"><span data-stu-id="829e3-105">HDM\_CLEARFILTER message</span></span>

<span data-ttu-id="829e3-106">Löscht den Filter für ein bestimmtes Header-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="829e3-106">Clears the filter for a given header control.</span></span> <span data-ttu-id="829e3-107">Sie können diese Nachricht explizit senden oder das [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="829e3-107">You can send this message explicitly or use the [**Header\_ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="829e3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="829e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="829e3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="829e3-110">Ein Spaltenwert, der angibt, welcher Filter gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="829e3-110">A column value indicating which filter to clear.</span></span>

</dd> <dt>

<span data-ttu-id="829e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="829e3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="829e3-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="829e3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829e3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="829e3-113">Return value</span></span>

<span data-ttu-id="829e3-114">Gibt eine ganze Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="829e3-114">Returns an integer.</span></span> <span data-ttu-id="829e3-115">Das **LRESULT** wird in eine ganze Zahl umgewandelt, die **true**(1) oder **false**(0) angibt.</span><span class="sxs-lookup"><span data-stu-id="829e3-115">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="remarks"></a><span data-ttu-id="829e3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="829e3-116">Remarks</span></span>

<span data-ttu-id="829e3-117">Wenn der Spaltenwert als-1 angegeben wird, werden alle Filter gelöscht, und die [Hdn-Filter \_ Änderungs](hdn-filterchange.md) Benachrichtigung wird nur einmal gesendet.</span><span class="sxs-lookup"><span data-stu-id="829e3-117">If the column value is specified as -1, all the filters are cleared, and the [HDN\_FILTERCHANGE](hdn-filterchange.md) notification is sent only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="829e3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="829e3-118">Requirements</span></span>



| <span data-ttu-id="829e3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="829e3-119">Requirement</span></span> | <span data-ttu-id="829e3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="829e3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="829e3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="829e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="829e3-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="829e3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="829e3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="829e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="829e3-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="829e3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="829e3-125">Header</span><span class="sxs-lookup"><span data-stu-id="829e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="829e3-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="829e3-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829e3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="829e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829e3-128">**\_ClearAllFilters-Header**</span><span class="sxs-lookup"><span data-stu-id="829e3-128">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





