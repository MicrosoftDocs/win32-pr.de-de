---
title: TBM_GETPTICS Meldung (kommstrg. h)
description: Ruft die Adresse eines Arrays ab, das die Positionen der Teil Striche für eine TrackBar enthält.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- Windows-Steuerelemente für TBM_GETPTICS Meldung
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956501"
---
# <a name="tbm_getptics-message"></a><span data-ttu-id="74493-104">TBM- \_ getptics-Nachricht</span><span class="sxs-lookup"><span data-stu-id="74493-104">TBM\_GETPTICS message</span></span>

<span data-ttu-id="74493-105">Ruft die Adresse eines Arrays ab, das die Positionen der Teil Striche für eine TrackBar enthält.</span><span class="sxs-lookup"><span data-stu-id="74493-105">Retrieves the address of an array that contains the positions of the tick marks for a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="74493-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74493-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74493-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74493-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="74493-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="74493-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="74493-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74493-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74493-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="74493-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74493-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74493-111">Return value</span></span>

<span data-ttu-id="74493-112">Gibt die Adresse eines Arrays von **DWORD** -Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="74493-112">Returns the address of an array of **DWORD** values.</span></span> <span data-ttu-id="74493-113">Die Elemente des Arrays geben die logischen Positionen der TrackBar-Teil Striche an, ohne die ersten und letzten Teil Striche, die von der TrackBar erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="74493-113">The elements of the array specify the logical positions of the trackbar's tick marks, not including the first and last tick marks created by the trackbar.</span></span> <span data-ttu-id="74493-114">Bei den logischen Positionen kann es sich um beliebige ganzzahlige Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen handeln.</span><span class="sxs-lookup"><span data-stu-id="74493-114">The logical positions can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="remarks"></a><span data-ttu-id="74493-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74493-115">Remarks</span></span>

<span data-ttu-id="74493-116">Die Anzahl der Elemente im Array ist kleiner als die von der [**TBM \_ GetNumTics**](tbm-getnumtics.md) -Nachricht zurückgegebene Tick-Anzahl.</span><span class="sxs-lookup"><span data-stu-id="74493-116">The number of elements in the array is two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span> <span data-ttu-id="74493-117">Beachten Sie, dass die Werte im Array doppelte Positionen enthalten können und möglicherweise nicht in sequenzieller Reihenfolge vorliegen.</span><span class="sxs-lookup"><span data-stu-id="74493-117">Note that the values in the array may include duplicate positions and may not be in sequential order.</span></span> <span data-ttu-id="74493-118">Der zurückgegebene Zeiger ist gültig, bis die Teil Striche der TrackBar geändert werden.</span><span class="sxs-lookup"><span data-stu-id="74493-118">The returned pointer is valid until you change the trackbar's tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="74493-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74493-119">Requirements</span></span>



| <span data-ttu-id="74493-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74493-120">Requirement</span></span> | <span data-ttu-id="74493-121">Wert</span><span class="sxs-lookup"><span data-stu-id="74493-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74493-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74493-122">Minimum supported client</span></span><br/> | <span data-ttu-id="74493-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74493-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74493-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74493-124">Minimum supported server</span></span><br/> | <span data-ttu-id="74493-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74493-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74493-126">Header</span><span class="sxs-lookup"><span data-stu-id="74493-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="74493-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="74493-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





