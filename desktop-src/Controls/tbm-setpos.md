---
title: TBM_SETPOS (Commctrl.h)
description: 'TBM_SETPOS Meldung: Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085868"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="f1057-104">TBM \_ SETPOS-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f1057-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="f1057-105">Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.</span><span class="sxs-lookup"><span data-stu-id="f1057-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1057-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1057-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1057-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1057-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1057-108">Flag neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f1057-108">Redraw flag.</span></span> <span data-ttu-id="f1057-109">Wenn dieser Parameter **TRUE ist,** wird das Steuerelement mit dem Schieberegler an der von lParam angegebenen *Position neu gedraht.*</span><span class="sxs-lookup"><span data-stu-id="f1057-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="f1057-110">Wenn dieser Parameter **FALSE ist,** wird der Schieberegler in der Meldung nicht an der neuen Position neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f1057-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="f1057-111">Beachten Sie, dass die Meldung den Wert der Position des Schiebereglers (wie von der [**TBM \_ GETPOS-Nachricht**](tbm-getpos.md) zurückgegeben) unabhängig vom *wParam-Parameter* festgibt.</span><span class="sxs-lookup"><span data-stu-id="f1057-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f1057-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1057-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1057-113">Neue logische Position des Schiebereglers.</span><span class="sxs-lookup"><span data-stu-id="f1057-113">New logical position of the slider.</span></span> <span data-ttu-id="f1057-114">Gültige logische Positionen sind die ganzzahligen Werte im Bereich von minimalen bis maximalen Schiebereglerpositionen der Trackleiste.</span><span class="sxs-lookup"><span data-stu-id="f1057-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="f1057-115">Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuerelements liegt, wird die Position auf den höchst- oder minimalen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f1057-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1057-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1057-116">Return value</span></span>

<span data-ttu-id="f1057-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="f1057-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1057-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1057-118">Requirements</span></span>



| <span data-ttu-id="f1057-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1057-119">Requirement</span></span> | <span data-ttu-id="f1057-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f1057-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1057-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1057-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1057-122">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1057-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1057-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1057-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1057-124">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1057-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1057-125">Header</span><span class="sxs-lookup"><span data-stu-id="f1057-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1057-126"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="f1057-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





