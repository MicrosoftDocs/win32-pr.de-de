---
title: LVM_GETSELECTIONMARK Meldung (kommstrg. h)
description: Ruft die Auswahl Markierung von einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getselectionmark-Makro verwenden.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- Windows-Steuerelemente für LVM_GETSELECTIONMARK Meldung
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342468"
---
# <a name="lvm_getselectionmark-message"></a><span data-ttu-id="0e6f3-105">LVM \_ getselectionmark-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0e6f3-105">LVM\_GETSELECTIONMARK message</span></span>

<span data-ttu-id="0e6f3-106">Ruft die Auswahl Markierung von einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-106">Retrieves the selection mark from a list-view control.</span></span> <span data-ttu-id="0e6f3-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ getselectionmark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-107">You can send this message explicitly or use the [**ListView\_GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e6f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e6f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e6f3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e6f3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e6f3-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0e6f3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e6f3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0e6f3-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e6f3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e6f3-113">Return value</span></span>

<span data-ttu-id="0e6f3-114">Gibt das null basierte Auswahl Zeichen oder-1 zurück, wenn kein Auswahl Zeichen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-114">Returns the zero-based selection mark, or -1 if there is no selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e6f3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e6f3-115">Remarks</span></span>

<span data-ttu-id="0e6f3-116">Das *Auswahl Zeichen* ist der Element Index, von dem eine Mehrfachauswahl gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-116">The *selection mark* is the item index from which a multiple selection starts.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6f3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e6f3-117">Requirements</span></span>



| <span data-ttu-id="0e6f3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e6f3-118">Requirement</span></span> | <span data-ttu-id="0e6f3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0e6f3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6f3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e6f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e6f3-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e6f3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e6f3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e6f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e6f3-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e6f3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e6f3-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e6f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e6f3-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e6f3-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e6f3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e6f3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6f3-127">**LVM \_ setselectionmark**</span><span class="sxs-lookup"><span data-stu-id="0e6f3-127">**LVM\_SETSELECTIONMARK**</span></span>](lvm-setselectionmark.md)
</dt> </dl>

 

 





