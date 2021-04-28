---
title: TBM_SETPOSNOTIFY Meldung (Commctrl.h)
description: 'TBM_SETPOSNOTIFY Meldung: Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104078"
---
# <a name="tbm_setposnotify-message"></a><span data-ttu-id="7aa3d-104">TBM \_ SETPOSNOTIFY-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7aa3d-104">TBM\_SETPOSNOTIFY message</span></span>

<span data-ttu-id="7aa3d-105">Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.</span><span class="sxs-lookup"><span data-stu-id="7aa3d-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7aa3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7aa3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aa3d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7aa3d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7aa3d-108">wParam wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7aa3d-108">wParam is unused.</span></span>

</dd> <dt>

<span data-ttu-id="7aa3d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7aa3d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7aa3d-110">Neue logische Position des Schiebereglers.</span><span class="sxs-lookup"><span data-stu-id="7aa3d-110">New logical position of the slider.</span></span> <span data-ttu-id="7aa3d-111">Gültige logische Positionen sind die ganzzahligen Werte im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen.</span><span class="sxs-lookup"><span data-stu-id="7aa3d-111">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="7aa3d-112">Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuerelements liegt, wird die Position auf den Maximal- oder Mindestwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7aa3d-112">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aa3d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7aa3d-113">Return value</span></span>

<span data-ttu-id="7aa3d-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7aa3d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aa3d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aa3d-115">Remarks</span></span>

<span data-ttu-id="7aa3d-116">Durch den Aufruf von **TBM \_ SETPOSNOTIFY** wird die Position des Trackbar-Schiebereglers wie [**bei TBM \_ SETPOS**](tbm-setpos.md) festgelegt. Dies bewirkt jedoch auch, dass die Trackleiste das übergeordnete Element über eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) über eine Verschiebung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="7aa3d-116">Calling **TBM\_SETPOSNOTIFY** will set the trackbar slider location like [**TBM\_SETPOS**](tbm-setpos.md) would, but it will also cause the trackbar to notify its parent of a move via a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa3d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aa3d-117">Requirements</span></span>



| <span data-ttu-id="7aa3d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aa3d-118">Requirement</span></span> | <span data-ttu-id="7aa3d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7aa3d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa3d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7aa3d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa3d-121">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7aa3d-121">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7aa3d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7aa3d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa3d-123">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7aa3d-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7aa3d-124">Header</span><span class="sxs-lookup"><span data-stu-id="7aa3d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aa3d-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="7aa3d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





