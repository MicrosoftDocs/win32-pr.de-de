---
title: PBM_DELTAPOS Meldung (kommstrg. h)
description: Verschiebt die aktuelle Position einer Statusleiste um ein angegebenes Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- Windows-Steuerelemente für PBM_DELTAPOS Meldung
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040799"
---
# <a name="pbm_deltapos-message"></a><span data-ttu-id="68d68-104">PBM- \_ Delta POS-Nachricht</span><span class="sxs-lookup"><span data-stu-id="68d68-104">PBM\_DELTAPOS message</span></span>

<span data-ttu-id="68d68-105">Verschiebt die aktuelle Position einer Statusleiste um ein angegebenes Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="68d68-105">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="68d68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68d68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d68-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68d68-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68d68-108">Betrag, um die Position zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="68d68-108">Amount to advance the position.</span></span>

</dd> <dt>

<span data-ttu-id="68d68-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68d68-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="68d68-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="68d68-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d68-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68d68-111">Return value</span></span>

<span data-ttu-id="68d68-112">Gibt die vorherige Position zurück.</span><span class="sxs-lookup"><span data-stu-id="68d68-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="68d68-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68d68-113">Remarks</span></span>

<span data-ttu-id="68d68-114">Wenn das Inkrement zu einem Wert außerhalb des Bereichs des Steuer Elements führt, wird die Position auf die nächstgelegene Grenze festgelegt.</span><span class="sxs-lookup"><span data-stu-id="68d68-114">If the increment results in a value outside the range of the control, the position is set to the nearest boundary.</span></span>

<span data-ttu-id="68d68-115">Das Verhalten dieser Nachricht ist nicht definiert, wenn Sie an ein Steuerelement gesendet wird, das den [**PSB- \_ Marquee**](progress-bar-control-styles.md) -Stil hat.</span><span class="sxs-lookup"><span data-stu-id="68d68-115">The behavior of this message is undefined if it is sent to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="68d68-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68d68-116">Requirements</span></span>



| <span data-ttu-id="68d68-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68d68-117">Requirement</span></span> | <span data-ttu-id="68d68-118">Wert</span><span class="sxs-lookup"><span data-stu-id="68d68-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68d68-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68d68-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68d68-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68d68-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68d68-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68d68-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68d68-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68d68-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68d68-123">Header</span><span class="sxs-lookup"><span data-stu-id="68d68-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="68d68-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="68d68-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





