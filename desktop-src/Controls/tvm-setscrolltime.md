---
title: TVM_SETSCROLLTIME Meldung (kommstrg. h)
description: Legt die maximale Scrollzeit für das Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ setscrolltime-Makros senden.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- Windows-Steuerelemente für TVM_SETSCROLLTIME Meldung
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338765"
---
# <a name="tvm_setscrolltime-message"></a><span data-ttu-id="951f4-105">TVM- \_ setscrolltime-Meldung</span><span class="sxs-lookup"><span data-stu-id="951f4-105">TVM\_SETSCROLLTIME message</span></span>

<span data-ttu-id="951f4-106">Legt die maximale Scrollzeit für das Strukturansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="951f4-106">Sets the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="951f4-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ setscrolltime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="951f4-107">You can send this message explicitly or by using the [**TreeView\_SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="951f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="951f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="951f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="951f4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="951f4-110">Neue maximale Scrollzeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="951f4-110">New maximum scroll time, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="951f4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="951f4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="951f4-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="951f4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="951f4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="951f4-113">Return value</span></span>

<span data-ttu-id="951f4-114">Gibt die vorherige maximale Scrollzeit in Millisekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="951f4-114">Returns the previous maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="951f4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="951f4-115">Remarks</span></span>

<span data-ttu-id="951f4-116">Die maximale Scrollzeit ist die längste Zeitspanne, die ein scrollvorgang ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="951f4-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="951f4-117">Der Bildlauf wird so angepasst, dass der Bildlauf innerhalb der maximalen Scrollzeit stattfindet.</span><span class="sxs-lookup"><span data-stu-id="951f4-117">Scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="951f4-118">Ein scrollvorgang kann weniger Zeit in Anspruch nehmen als das Maximum.</span><span class="sxs-lookup"><span data-stu-id="951f4-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="951f4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="951f4-119">Requirements</span></span>



| <span data-ttu-id="951f4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="951f4-120">Requirement</span></span> | <span data-ttu-id="951f4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="951f4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="951f4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="951f4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="951f4-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="951f4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="951f4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="951f4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="951f4-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="951f4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="951f4-126">Header</span><span class="sxs-lookup"><span data-stu-id="951f4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="951f4-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="951f4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="951f4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="951f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951f4-129">**TVM \_ getscrolltime**</span><span class="sxs-lookup"><span data-stu-id="951f4-129">**TVM\_GETSCROLLTIME**</span></span>](tvm-getscrolltime.md)
</dt> </dl>

 

 





