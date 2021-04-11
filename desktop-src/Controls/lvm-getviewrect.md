---
title: LVM_GETVIEWRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck aller Elemente im Listenansicht-Steuerelement ab. Die Listenansicht muss in der Symbol Ansicht oder in der kleinen Symbol Ansicht angezeigt werden. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetViewRect-Makros senden.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- Windows-Steuerelemente für LVM_GETVIEWRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040886"
---
# <a name="lvm_getviewrect-message"></a><span data-ttu-id="8b277-106">LVM \_ GetViewRect-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8b277-106">LVM\_GETVIEWRECT message</span></span>

<span data-ttu-id="8b277-107">Ruft das umgebende Rechteck aller Elemente im Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="8b277-107">Retrieves the bounding rectangle of all items in the list-view control.</span></span> <span data-ttu-id="8b277-108">Die Listenansicht muss in der Symbol Ansicht oder in der kleinen Symbol Ansicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8b277-108">The list view must be in icon or small icon view.</span></span> <span data-ttu-id="8b277-109">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="8b277-109">You can send this message explicitly or by using the [**ListView\_GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b277-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b277-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b277-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b277-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8b277-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8b277-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8b277-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b277-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b277-114">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="8b277-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="8b277-115">Alle Koordinaten sind relativ zum sichtbaren Bereich des Listenansicht-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="8b277-115">All coordinates are relative to the visible area of the list-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b277-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b277-116">Return value</span></span>

<span data-ttu-id="8b277-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8b277-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b277-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b277-118">Requirements</span></span>



| <span data-ttu-id="8b277-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b277-119">Requirement</span></span> | <span data-ttu-id="8b277-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8b277-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b277-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b277-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b277-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b277-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b277-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b277-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b277-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b277-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b277-125">Header</span><span class="sxs-lookup"><span data-stu-id="8b277-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b277-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b277-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

