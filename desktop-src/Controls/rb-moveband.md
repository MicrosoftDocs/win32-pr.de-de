---
title: RB_MOVEBAND Meldung (kommstrg. h)
description: Verschiebt ein Band von einem Index zu einem anderen.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- Windows-Steuerelemente für RB_MOVEBAND Meldung
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475342"
---
# <a name="rb_moveband-message"></a><span data-ttu-id="c3954-104">RB- \_ Message-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c3954-104">RB\_MOVEBAND message</span></span>

<span data-ttu-id="c3954-105">Verschiebt ein Band von einem Index zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="c3954-105">Moves a band from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3954-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3954-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3954-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3954-108">Der null basierte Index des zu bewegenden Bands.</span><span class="sxs-lookup"><span data-stu-id="c3954-108">Zero-based index of the band to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="c3954-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3954-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3954-110">NULL basierter Index der neuen Bandposition.</span><span class="sxs-lookup"><span data-stu-id="c3954-110">Zero-based index of the new band position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3954-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3954-111">Return value</span></span>

<span data-ttu-id="c3954-112">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="c3954-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3954-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3954-113">Remarks</span></span>

<span data-ttu-id="c3954-114">Diese Meldung ändert höchstwahrscheinlich den Index anderer Bänder im Grund leisten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c3954-114">This message will most likely change the index of other bands in the rebar control.</span></span> <span data-ttu-id="c3954-115">Wenn ein Band von Index 6 in Index 0 verschoben wird, wird der Index aller Bänder dazwischen um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="c3954-115">If a band is moved from index 6 to index 0, all of the bands in between will have their index incremented by one.</span></span>

<span data-ttu-id="c3954-116">*LPARAM* darf nie größer als die Anzahl der Bänder minus 1 sein.</span><span class="sxs-lookup"><span data-stu-id="c3954-116">*lParam* must never be greater than the number of bands minus one.</span></span> <span data-ttu-id="c3954-117">Die Anzahl der Bänder kann mit der [**RB \_ GetBandCount**](rb-getbandcount.md) -Nachricht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c3954-117">The number of bands can be obtained with the [**RB\_GETBANDCOUNT**](rb-getbandcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3954-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3954-118">Requirements</span></span>



| <span data-ttu-id="c3954-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3954-119">Requirement</span></span> | <span data-ttu-id="c3954-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c3954-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3954-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3954-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c3954-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3954-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3954-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3954-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c3954-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3954-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3954-125">Header</span><span class="sxs-lookup"><span data-stu-id="c3954-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3954-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3954-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





