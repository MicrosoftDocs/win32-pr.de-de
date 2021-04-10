---
title: PBM_GETSTEP Meldung (kommstrg. h)
description: Ruft das Schritt Inkrement von einer Statusanzeige ab. Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer PBM-StepIt-Nachricht die aktuelle Position vergrößert \_ . Standardmäßig ist das Schritt Inkrement auf 10 festgelegt.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- Windows-Steuerelemente für PBM_GETSTEP Meldung
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956812"
---
# <a name="pbm_getstep-message"></a><span data-ttu-id="59f0a-106">PBM- \_ getstep-Nachricht</span><span class="sxs-lookup"><span data-stu-id="59f0a-106">PBM\_GETSTEP message</span></span>

<span data-ttu-id="59f0a-107">Ruft das Schritt Inkrement von einer Statusanzeige ab.</span><span class="sxs-lookup"><span data-stu-id="59f0a-107">Retrieves the step increment from a progress bar.</span></span> <span data-ttu-id="59f0a-108">Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer [**PBM- \_ StepIt**](pbm-stepit.md) -Nachricht die aktuelle Position vergrößert.</span><span class="sxs-lookup"><span data-stu-id="59f0a-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="59f0a-109">Standardmäßig ist das Schritt Inkrement auf 10 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="59f0a-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="59f0a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59f0a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f0a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59f0a-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="59f0a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="59f0a-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="59f0a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59f0a-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="59f0a-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="59f0a-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f0a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59f0a-115">Return value</span></span>

<span data-ttu-id="59f0a-116">Gibt das aktuelle Schritt Inkrement zurück.</span><span class="sxs-lookup"><span data-stu-id="59f0a-116">Returns the current step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="59f0a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59f0a-117">Requirements</span></span>



| <span data-ttu-id="59f0a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59f0a-118">Requirement</span></span> | <span data-ttu-id="59f0a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="59f0a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59f0a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59f0a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59f0a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59f0a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59f0a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59f0a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59f0a-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59f0a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59f0a-124">Header</span><span class="sxs-lookup"><span data-stu-id="59f0a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59f0a-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="59f0a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





