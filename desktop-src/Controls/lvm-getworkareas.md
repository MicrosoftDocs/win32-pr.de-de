---
title: LVM_GETWORKAREAS Meldung (kommstrg. h)
description: Ruft die Arbeitsbereiche aus einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getworkareas-Makro verwenden.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Windows-Steuerelemente für LVM_GETWORKAREAS Meldung
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478504"
---
# <a name="lvm_getworkareas-message"></a><span data-ttu-id="fe0d1-105">LVM \_ getworkareas-Meldung</span><span class="sxs-lookup"><span data-stu-id="fe0d1-105">LVM\_GETWORKAREAS message</span></span>

<span data-ttu-id="fe0d1-106">Ruft die Arbeitsbereiche aus einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="fe0d1-106">Retrieves the working areas from a list-view control.</span></span> <span data-ttu-id="fe0d1-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ getworkareas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe0d1-107">You can send this message explicitly or use the [**ListView\_GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe0d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe0d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe0d1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0d1-110">Die Anzahl der [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen im Array bei *LPARAM*.</span><span class="sxs-lookup"><span data-stu-id="fe0d1-110">The number of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures in the array at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="fe0d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe0d1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0d1-112">Ein Zeiger auf ein Array von [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen, die die aktuellen Arbeitsbereiche des Listenansicht-Steuer Elements empfangen.</span><span class="sxs-lookup"><span data-stu-id="fe0d1-112">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that receive the current working areas of the list-view control.</span></span> <span data-ttu-id="fe0d1-113">Werte in diesen Strukturen befinden sich in Client Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="fe0d1-113">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="fe0d1-114">*wParam* gibt die Anzahl der Strukturen in diesem Array an.</span><span class="sxs-lookup"><span data-stu-id="fe0d1-114">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0d1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe0d1-115">Return value</span></span>

<span data-ttu-id="fe0d1-116">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe0d1-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0d1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe0d1-117">Requirements</span></span>



| <span data-ttu-id="fe0d1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe0d1-118">Requirement</span></span> | <span data-ttu-id="fe0d1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fe0d1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0d1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe0d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0d1-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe0d1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe0d1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe0d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0d1-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe0d1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe0d1-124">Header</span><span class="sxs-lookup"><span data-stu-id="fe0d1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0d1-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0d1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0d1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe0d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0d1-127">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="fe0d1-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

