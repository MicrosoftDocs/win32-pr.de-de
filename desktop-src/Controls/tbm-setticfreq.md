---
title: TBM_SETTICFREQ Meldung (kommstrg. h)
description: Legt die Intervall Häufigkeit für Teil Striche in einer TrackBar fest.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Windows-Steuerelemente für TBM_SETTICFREQ Meldung
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040358"
---
# <a name="tbm_setticfreq-message"></a><span data-ttu-id="ddb57-104">TBM- \_ mescfreq-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ddb57-104">TBM\_SETTICFREQ message</span></span>

<span data-ttu-id="ddb57-105">Legt die Intervall Häufigkeit für Teil Striche in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="ddb57-105">Sets the interval frequency for tick marks in a trackbar.</span></span> <span data-ttu-id="ddb57-106">Wenn die Häufigkeit z. b. auf zwei festgelegt ist, wird für jedes andere Inkrement im Bereich der TrackBar ein Teil Strich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ddb57-106">For example, if the frequency is set to two, a tick mark is displayed for every other increment in the trackbar's range.</span></span> <span data-ttu-id="ddb57-107">Die Standardeinstellung für die Häufigkeit ist 1. Das heißt, jedes Inkrement im Bereich ist einem Teil Strich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ddb57-107">The default setting for the frequency is one; that is, every increment in the range is associated with a tick mark.</span></span>

## <a name="parameters"></a><span data-ttu-id="ddb57-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddb57-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ddb57-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddb57-110">Häufigkeit der Teil Striche.</span><span class="sxs-lookup"><span data-stu-id="ddb57-110">Frequency of the tick marks.</span></span>

</dd> <dt>

<span data-ttu-id="ddb57-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ddb57-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ddb57-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ddb57-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddb57-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddb57-113">Return value</span></span>

<span data-ttu-id="ddb57-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ddb57-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb57-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddb57-115">Remarks</span></span>

<span data-ttu-id="ddb57-116">Die TrackBar muss den TSB-Stil " [**\_ autoticks**](trackbar-control-styles.md) " aufweisen, um diese Meldung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddb57-116">The trackbar must have the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) style to use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb57-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddb57-117">Requirements</span></span>



| <span data-ttu-id="ddb57-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddb57-118">Requirement</span></span> | <span data-ttu-id="ddb57-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ddb57-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb57-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddb57-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb57-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddb57-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ddb57-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddb57-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb57-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddb57-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ddb57-124">Header</span><span class="sxs-lookup"><span data-stu-id="ddb57-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddb57-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddb57-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





