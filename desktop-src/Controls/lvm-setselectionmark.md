---
title: LVM_SETSELECTIONMARK Meldung (kommstrg. h)
description: Legt die Auswahl Markierung in einem Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das ListView \_ setselectionmark-Makro verwenden.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Windows-Steuerelemente für LVM_SETSELECTIONMARK Meldung
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739936"
---
# <a name="lvm_setselectionmark-message"></a><span data-ttu-id="d6e1f-105">LVM- \_ setselectionmark-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d6e1f-105">LVM\_SETSELECTIONMARK message</span></span>

<span data-ttu-id="d6e1f-106">Legt die Auswahl Markierung in einem Listenansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-106">Sets the selection mark in a list-view control.</span></span> <span data-ttu-id="d6e1f-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ setselectionmark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-107">You can send this message explicitly or use the [**ListView\_SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6e1f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6e1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6e1f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d6e1f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d6e1f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6e1f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6e1f-112">NULL basierter Index der neuen Auswahl Markierung.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-112">Zero-based index of the new selection mark.</span></span> <span data-ttu-id="d6e1f-113">Wenn der Wert auf-1 festgelegt ist, wird das Auswahl Zeichen entfernt.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-113">If set to -1, the selection mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e1f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6e1f-114">Return value</span></span>

<span data-ttu-id="d6e1f-115">Gibt die vorherige Auswahl Markierung oder-1 zurück, wenn keine vorherige Auswahl Markierung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-115">Returns the previous selection mark, or -1 if there is no previous selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6e1f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6e1f-116">Remarks</span></span>

<span data-ttu-id="d6e1f-117">Das *Auswahl Zeichen* ist der Element Index, von dem eine Mehrfachauswahl gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-117">The *selection mark* is the item index from which a multiple selection starts.</span></span> <span data-ttu-id="d6e1f-118">Diese Meldung wirkt sich nicht auf den Auswahl Zustand des Elements aus.</span><span class="sxs-lookup"><span data-stu-id="d6e1f-118">This message does not affect the selection state of the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e1f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6e1f-119">Requirements</span></span>



| <span data-ttu-id="d6e1f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6e1f-120">Requirement</span></span> | <span data-ttu-id="d6e1f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d6e1f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e1f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6e1f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e1f-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6e1f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6e1f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6e1f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e1f-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6e1f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6e1f-126">Header</span><span class="sxs-lookup"><span data-stu-id="d6e1f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e1f-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e1f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6e1f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6e1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e1f-129">**LVM \_ getselectionmark**</span><span class="sxs-lookup"><span data-stu-id="d6e1f-129">**LVM\_GETSELECTIONMARK**</span></span>](lvm-getselectionmark.md)
</dt> </dl>

 

 





