---
title: TBM_GETLINESIZE Meldung (kommstrg. h)
description: Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- Windows-Steuerelemente für TBM_GETLINESIZE Meldung
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957244"
---
# <a name="tbm_getlinesize-message"></a><span data-ttu-id="7626b-105">TBM \_ getlinesize-Meldung</span><span class="sxs-lookup"><span data-stu-id="7626b-105">TBM\_GETLINESIZE message</span></span>

<span data-ttu-id="7626b-106">Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben aus den Pfeiltasten (z. b. die-oder-Taste) verschiebt.</span><span class="sxs-lookup"><span data-stu-id="7626b-106">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="7626b-107">Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="7626b-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="7626b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7626b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7626b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7626b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7626b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7626b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7626b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7626b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7626b-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7626b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7626b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7626b-113">Return value</span></span>

<span data-ttu-id="7626b-114">Gibt einen 32-Bit-Wert zurück, der die Zeilengröße für die TrackBar angibt.</span><span class="sxs-lookup"><span data-stu-id="7626b-114">Returns a 32-bit value that specifies the line size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="7626b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7626b-115">Remarks</span></span>

<span data-ttu-id="7626b-116">Die Standardeinstellung für die Zeilengröße ist 1.</span><span class="sxs-lookup"><span data-stu-id="7626b-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="7626b-117">Die TrackBar sendet außerdem eine [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht mit den e/a \_ -und TB- \_ LineDown-Benachrichtigungs Codes an das übergeordnete Fenster, wenn der Benutzer die Pfeiltasten drückt.</span><span class="sxs-lookup"><span data-stu-id="7626b-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="7626b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7626b-118">Requirements</span></span>



| <span data-ttu-id="7626b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7626b-119">Requirement</span></span> | <span data-ttu-id="7626b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7626b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7626b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7626b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7626b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7626b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7626b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7626b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7626b-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7626b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7626b-125">Header</span><span class="sxs-lookup"><span data-stu-id="7626b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7626b-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7626b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





