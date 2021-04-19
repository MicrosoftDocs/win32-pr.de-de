---
title: PBM_SETSTEP Meldung (kommstrg. h)
description: Gibt das Schritt Inkrement für eine Statusanzeige an. Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer PBM-StepIt-Nachricht die aktuelle Position vergrößert \_ . Standardmäßig ist das Schritt Inkrement auf 10 festgelegt.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- Windows-Steuerelemente für PBM_SETSTEP Meldung
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346513"
---
# <a name="pbm_setstep-message"></a><span data-ttu-id="fa34e-106">PBM- \_ SetStep-Nachricht</span><span class="sxs-lookup"><span data-stu-id="fa34e-106">PBM\_SETSTEP message</span></span>

<span data-ttu-id="fa34e-107">Gibt das Schritt Inkrement für eine Statusanzeige an.</span><span class="sxs-lookup"><span data-stu-id="fa34e-107">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="fa34e-108">Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer [**PBM- \_ StepIt**](pbm-stepit.md) -Nachricht die aktuelle Position vergrößert.</span><span class="sxs-lookup"><span data-stu-id="fa34e-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="fa34e-109">Standardmäßig ist das Schritt Inkrement auf 10 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fa34e-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa34e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa34e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa34e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa34e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa34e-112">Neuer Schritt Inkrement.</span><span class="sxs-lookup"><span data-stu-id="fa34e-112">New step increment.</span></span>

</dd> <dt>

<span data-ttu-id="fa34e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa34e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fa34e-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fa34e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa34e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa34e-115">Return value</span></span>

<span data-ttu-id="fa34e-116">Gibt das vorherige Schritt Inkrement zurück.</span><span class="sxs-lookup"><span data-stu-id="fa34e-116">Returns the previous step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa34e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa34e-117">Requirements</span></span>



| <span data-ttu-id="fa34e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa34e-118">Requirement</span></span> | <span data-ttu-id="fa34e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fa34e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa34e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa34e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa34e-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa34e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa34e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa34e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa34e-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa34e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa34e-124">Header</span><span class="sxs-lookup"><span data-stu-id="fa34e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa34e-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa34e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





