---
title: PBM_STEPIT Meldung (kommstrg. h)
description: Verschiebt die aktuelle Position für eine Statusanzeige um das Schritt Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln. Eine Anwendung legt das Schritt Inkrement fest, indem die PBM- \_ SetStep-Nachricht gesendet wird.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- Windows-Steuerelemente für PBM_STEPIT Meldung
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956808"
---
# <a name="pbm_stepit-message"></a><span data-ttu-id="2f3b5-105">PBM- \_ StepIt-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2f3b5-105">PBM\_STEPIT message</span></span>

<span data-ttu-id="2f3b5-106">Verschiebt die aktuelle Position für eine Statusanzeige um das Schritt Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-106">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="2f3b5-107">Eine Anwendung legt das Schritt Inkrement fest, indem die [**PBM- \_ SetStep**](pbm-setstep.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-107">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f3b5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f3b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f3b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f3b5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f3b5-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f3b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f3b5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f3b5-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f3b5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f3b5-113">Return value</span></span>

<span data-ttu-id="2f3b5-114">Gibt die vorherige Position zurück.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-114">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f3b5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f3b5-115">Remarks</span></span>

<span data-ttu-id="2f3b5-116">Wenn die Position den maximalen Bereichs Wert überschreitet, setzt diese Nachricht die aktuelle Position zurück, sodass die Statusanzeige von Anfang an erneut beginnt.</span><span class="sxs-lookup"><span data-stu-id="2f3b5-116">When the position exceeds the maximum range value, this message resets the current position so that the progress indicator starts over again from the beginning.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3b5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f3b5-117">Requirements</span></span>



| <span data-ttu-id="2f3b5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f3b5-118">Requirement</span></span> | <span data-ttu-id="2f3b5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3b5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3b5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f3b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f3b5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f3b5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f3b5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f3b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f3b5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f3b5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f3b5-124">Header</span><span class="sxs-lookup"><span data-stu-id="2f3b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f3b5-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3b5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





