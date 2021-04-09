---
title: LVM_SETWORKAREAS Meldung (kommstrg. h)
description: Legt die Arbeitsbereiche in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das ListView \_ setworkareas-Makro verwenden.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- Windows-Steuerelemente für LVM_SETWORKAREAS Meldung
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956979"
---
# <a name="lvm_setworkareas-message"></a><span data-ttu-id="331f4-105">LVM- \_ setworkareas-Meldung</span><span class="sxs-lookup"><span data-stu-id="331f4-105">LVM\_SETWORKAREAS message</span></span>

<span data-ttu-id="331f4-106">Legt die Arbeitsbereiche in einem Listenansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="331f4-106">Sets the working areas within a list-view control.</span></span> <span data-ttu-id="331f4-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ setworkareas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="331f4-107">You can send this message explicitly or use the [**ListView\_SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="331f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="331f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="331f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="331f4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="331f4-110">Die Anzahl der Strukturen im Array bei *LPRC*.</span><span class="sxs-lookup"><span data-stu-id="331f4-110">The number of structures in the array at *lprc*.</span></span> <span data-ttu-id="331f4-111">Die maximal zulässige Anzahl von Arbeitsbereichen wird durch den Wert für die maximale Arbeitsbereiche von LV definiert \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="331f4-111">The maximum number of working areas allowed is defined by the LV\_MAX\_WORKAREAS value.</span></span>

</dd> <dt>

<span data-ttu-id="331f4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="331f4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="331f4-113">Zeiger auf ein Array von [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen, die die neuen Arbeitsbereiche des Listenansicht-Steuer Elements enthalten.</span><span class="sxs-lookup"><span data-stu-id="331f4-113">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that contain the new working areas of the list-view control.</span></span> <span data-ttu-id="331f4-114">Werte in diesen Strukturen befinden sich in Client Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="331f4-114">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="331f4-115">Wenn dieser Parameter **null** ist, wird der Arbeitsbereich auf den Client Bereich des Steuer Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="331f4-115">If this parameter is **NULL**, the working area will be set to the client area of the control.</span></span> <span data-ttu-id="331f4-116">*wParam* gibt die Anzahl der Strukturen in diesem Array an.</span><span class="sxs-lookup"><span data-stu-id="331f4-116">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="331f4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="331f4-117">Return value</span></span>

<span data-ttu-id="331f4-118">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="331f4-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="331f4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="331f4-119">Requirements</span></span>



| <span data-ttu-id="331f4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="331f4-120">Requirement</span></span> | <span data-ttu-id="331f4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="331f4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="331f4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="331f4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="331f4-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="331f4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="331f4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="331f4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="331f4-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="331f4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="331f4-126">Header</span><span class="sxs-lookup"><span data-stu-id="331f4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="331f4-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="331f4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="331f4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="331f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331f4-129">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="331f4-129">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

