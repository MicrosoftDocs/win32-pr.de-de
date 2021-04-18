---
title: PBM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle Position für eine Statusanzeige fest und zeichnet den Balken neu, um die neue Position widerzuspiegeln.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Windows-Steuerelemente für PBM_SETPOS Meldung
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337530"
---
# <a name="pbm_setpos-message"></a><span data-ttu-id="5949d-104">PBM- \_ SetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5949d-104">PBM\_SETPOS message</span></span>

<span data-ttu-id="5949d-105">Legt die aktuelle Position für eine Statusanzeige fest und zeichnet den Balken neu, um die neue Position widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="5949d-105">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="5949d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5949d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5949d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5949d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5949d-108">Ganzzahl mit Vorzeichen, die zur neuen Position wird.</span><span class="sxs-lookup"><span data-stu-id="5949d-108">Signed integer that becomes the new position.</span></span>

</dd> <dt>

<span data-ttu-id="5949d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5949d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5949d-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5949d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5949d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5949d-111">Return value</span></span>

<span data-ttu-id="5949d-112">Gibt die vorherige Position zurück.</span><span class="sxs-lookup"><span data-stu-id="5949d-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="5949d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5949d-113">Remarks</span></span>

<span data-ttu-id="5949d-114">Wenn sich *wParam* außerhalb des Bereichs des Steuer Elements befindet, wird die Position auf die nächstgelegene Grenze festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5949d-114">If *wParam* is outside the range of the control, the position is set to the closest boundary.</span></span>

<span data-ttu-id="5949d-115">Senden Sie diese Nachricht nicht an ein Steuerelement, das den [**PSB- \_ Marquee**](progress-bar-control-styles.md) -Stil hat.</span><span class="sxs-lookup"><span data-stu-id="5949d-115">Do not send this message to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5949d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5949d-116">Requirements</span></span>



| <span data-ttu-id="5949d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5949d-117">Requirement</span></span> | <span data-ttu-id="5949d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5949d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5949d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5949d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5949d-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5949d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5949d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5949d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5949d-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5949d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5949d-123">Header</span><span class="sxs-lookup"><span data-stu-id="5949d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5949d-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5949d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





