---
title: TBM_SETPOSNOTIFY Meldung (kommstrg. h)
description: Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Windows-Steuerelemente für TBM_SETPOSNOTIFY Meldung
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475912"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="71fdb-104">TBM- \_ setposnotify-Nachricht</span><span class="sxs-lookup"><span data-stu-id="71fdb-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="71fdb-105">Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="71fdb-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="71fdb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71fdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71fdb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71fdb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71fdb-108">wParam wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="71fdb-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="71fdb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71fdb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71fdb-110">Neue logische Position des Schiebereglers.</span><span class="sxs-lookup"><span data-stu-id="71fdb-110">New logical position of the slider.</span></span> <span data-ttu-id="71fdb-111">Gültige logische Positionen sind die ganzzahligen Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen.</span><span class="sxs-lookup"><span data-stu-id="71fdb-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="71fdb-112">Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuer Elements liegt, wird die Position auf den maximalen oder minimalen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="71fdb-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71fdb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71fdb-113">Return value</span></span>

<span data-ttu-id="71fdb-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="71fdb-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71fdb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71fdb-115">Remarks</span></span>

<span data-ttu-id="71fdb-116">Durch den Aufruf von **TBM \_ setposnotify** wird der Schieberegler für den Schieberegler festgelegt, [**z. b. TBM- \_ SetPos**](tbm-setpos.md) . Dies bewirkt jedoch auch, dass die TrackBar das übergeordnete Element über eine " [**WM \_ HScroll**](wm-hscroll.md) "-oder " [**WM \_ VScroll**](wm-vscroll.md) "-Meldung</span><span class="sxs-lookup"><span data-stu-id="71fdb-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="71fdb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71fdb-117">Requirements</span></span>



| <span data-ttu-id="71fdb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71fdb-118">Requirement</span></span> | <span data-ttu-id="71fdb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="71fdb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71fdb-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71fdb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71fdb-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71fdb-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="71fdb-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71fdb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71fdb-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71fdb-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71fdb-124">Header</span><span class="sxs-lookup"><span data-stu-id="71fdb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="71fdb-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="71fdb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





