---
title: EM_SETUNDOLIMIT Meldung (RichEdit. h)
description: Legt die maximale Anzahl von Aktionen fest, die in der Rückgängig-Warteschlange eines Rich-Edit-Steuer Elements gespeichert werden können.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- Windows-Steuerelemente für EM_SETUNDOLIMIT Meldung
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956632"
---
# <a name="em_setundolimit-message"></a><span data-ttu-id="d66eb-104">EM- \_ logdolimit-Meldung</span><span class="sxs-lookup"><span data-stu-id="d66eb-104">EM\_SETUNDOLIMIT message</span></span>

<span data-ttu-id="d66eb-105">Legt die maximale Anzahl von Aktionen fest, die in der Rückgängig-Warteschlange eines Rich-Edit-Steuer Elements gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="d66eb-105">Sets the maximum number of actions that can stored in the undo queue of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d66eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d66eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d66eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d66eb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d66eb-108">Gibt die maximale Anzahl von Aktionen an, die in der Rückgängig-Warteschlange gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="d66eb-108">Specifies the maximum number of actions that can be stored in the undo queue.</span></span>

</dd> <dt>

<span data-ttu-id="d66eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d66eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d66eb-110">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d66eb-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d66eb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d66eb-111">Return value</span></span>

<span data-ttu-id="d66eb-112">Der Rückgabewert ist die neue maximale Anzahl von Rückgängig-Aktionen für das Rich Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d66eb-112">The return value is the new maximum number of undo actions for the rich edit control.</span></span> <span data-ttu-id="d66eb-113">Dieser Wert ist möglicherweise kleiner als *wParam* , wenn der Arbeitsspeicher begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="d66eb-113">This value may be less than *wParam* if memory is limited.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66eb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d66eb-114">Remarks</span></span>

<span data-ttu-id="d66eb-115">Standardmäßig ist die maximale Anzahl von Aktionen in der Rückgängig-Warteschlange 100.</span><span class="sxs-lookup"><span data-stu-id="d66eb-115">By default, the maximum number of actions in the undo queue is 100.</span></span> <span data-ttu-id="d66eb-116">Wenn Sie diese Zahl erhöhen, muss genügend Arbeitsspeicher zur Verfügung stehen, um die neue Zahl aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="d66eb-116">If you increase this number, there must be enough available memory to accommodate the new number.</span></span> <span data-ttu-id="d66eb-117">Um die Leistung zu verbessern, legen Sie den Grenzwert auf den kleinsten möglichen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="d66eb-117">For better performance, set the limit to the smallest possible value.</span></span>

<span data-ttu-id="d66eb-118">Wenn Sie den Grenzwert auf NULL festlegen, wird die Funktion **Rückgängig** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d66eb-118">Setting the limit to zero disables the **Undo** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="d66eb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d66eb-119">Requirements</span></span>



| <span data-ttu-id="d66eb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d66eb-120">Requirement</span></span> | <span data-ttu-id="d66eb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d66eb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d66eb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d66eb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d66eb-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d66eb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d66eb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d66eb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d66eb-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d66eb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d66eb-126">Header</span><span class="sxs-lookup"><span data-stu-id="d66eb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d66eb-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d66eb-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d66eb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d66eb-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d66eb-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d66eb-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d66eb-130">**EM \_ CanRedo**</span><span class="sxs-lookup"><span data-stu-id="d66eb-130">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="d66eb-131">**EM \_ getredoname**</span><span class="sxs-lookup"><span data-stu-id="d66eb-131">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="d66eb-132">**EM \_ getundoname**</span><span class="sxs-lookup"><span data-stu-id="d66eb-132">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="d66eb-133">**EM- \_ Wiederholung**</span><span class="sxs-lookup"><span data-stu-id="d66eb-133">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="d66eb-134">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="d66eb-134">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





