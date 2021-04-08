---
title: TBM_SETLINESIZE Meldung (kommstrg. h)
description: Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- Windows-Steuerelemente für TBM_SETLINESIZE Meldung
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949545"
---
# <a name="tbm_setlinesize-message"></a><span data-ttu-id="c97a6-105">TBM- \_ Nachricht "setlinesize"</span><span class="sxs-lookup"><span data-stu-id="c97a6-105">TBM\_SETLINESIZE message</span></span>

<span data-ttu-id="c97a6-106">Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt.</span><span class="sxs-lookup"><span data-stu-id="c97a6-106">Sets the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="c97a6-107">Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="c97a6-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="c97a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c97a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c97a6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c97a6-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c97a6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c97a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c97a6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c97a6-112">Neue Zeilengröße.</span><span class="sxs-lookup"><span data-stu-id="c97a6-112">New line size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97a6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c97a6-113">Return value</span></span>

<span data-ttu-id="c97a6-114">Gibt einen 32-Bit-Wert zurück, der die vorherige Zeilengröße angibt.</span><span class="sxs-lookup"><span data-stu-id="c97a6-114">Returns a 32-bit value that specifies the previous line size.</span></span>

## <a name="remarks"></a><span data-ttu-id="c97a6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c97a6-115">Remarks</span></span>

<span data-ttu-id="c97a6-116">Die Standardeinstellung für die Zeilengröße ist 1.</span><span class="sxs-lookup"><span data-stu-id="c97a6-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="c97a6-117">Die TrackBar sendet außerdem eine [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht mit den e/a \_ -und TB- \_ LineDown-Benachrichtigungs Codes an das übergeordnete Fenster, wenn der Benutzer die Pfeiltasten drückt.</span><span class="sxs-lookup"><span data-stu-id="c97a6-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97a6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c97a6-118">Requirements</span></span>



| <span data-ttu-id="c97a6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c97a6-119">Requirement</span></span> | <span data-ttu-id="c97a6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c97a6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c97a6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c97a6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c97a6-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c97a6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c97a6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c97a6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c97a6-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c97a6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c97a6-125">Header</span><span class="sxs-lookup"><span data-stu-id="c97a6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97a6-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c97a6-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97a6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c97a6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97a6-128">**TBM \_ getlinesize**</span><span class="sxs-lookup"><span data-stu-id="c97a6-128">**TBM\_GETLINESIZE**</span></span>](tbm-getlinesize.md)
</dt> </dl>

 

 





