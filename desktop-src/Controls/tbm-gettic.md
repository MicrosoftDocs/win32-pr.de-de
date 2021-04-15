---
title: TBM_GETTIC Meldung (kommstrg. h)
description: Ruft die logische Position eines Teil Strichs in einer TrackBar ab. Die logische Position kann ein beliebiger ganzzahliger Wert im Bereich der TrackBar sein, der den minimalen und maximalen Schieberegler-Positionen entspricht.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- Windows-Steuerelemente für TBM_GETTIC Meldung
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476797"
---
# <a name="tbm_gettic-message"></a><span data-ttu-id="0e2ed-105">TBM- \_ GetTic-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0e2ed-105">TBM\_GETTIC message</span></span>

<span data-ttu-id="0e2ed-106">Ruft die logische Position eines Teil Strichs in einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="0e2ed-106">Retrieves the logical position of a tick mark in a trackbar.</span></span> <span data-ttu-id="0e2ed-107">Die logische Position kann ein beliebiger ganzzahliger Wert im Bereich der TrackBar sein, der den minimalen und maximalen Schieberegler-Positionen entspricht.</span><span class="sxs-lookup"><span data-stu-id="0e2ed-107">The logical position can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e2ed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e2ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e2ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e2ed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e2ed-110">NULL basierter Index, der einen Teil Strich identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0e2ed-110">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="0e2ed-111">Gültige Indizes liegen im Bereich von 0 bis zwei kleiner als der von der [**TBM \_ GetNumTics**](tbm-getnumtics.md) -Nachricht zurückgegebene Tick-Zähler.</span><span class="sxs-lookup"><span data-stu-id="0e2ed-111">Valid indexes are in the range from zero to two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="0e2ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e2ed-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0e2ed-113">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0e2ed-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e2ed-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e2ed-114">Return value</span></span>

<span data-ttu-id="0e2ed-115">Gibt die logische Position des angegebenen Teil Strichs oder-1 zurück, wenn *wParam* keinen gültigen Index angibt.</span><span class="sxs-lookup"><span data-stu-id="0e2ed-115">Returns the logical position of the specified tick mark, or -1 if *wParam* does not specify a valid index.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e2ed-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e2ed-116">Requirements</span></span>



| <span data-ttu-id="0e2ed-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e2ed-117">Requirement</span></span> | <span data-ttu-id="0e2ed-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0e2ed-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2ed-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e2ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0e2ed-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e2ed-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e2ed-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e2ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0e2ed-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e2ed-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e2ed-123">Header</span><span class="sxs-lookup"><span data-stu-id="0e2ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e2ed-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e2ed-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





