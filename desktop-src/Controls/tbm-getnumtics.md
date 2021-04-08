---
title: TBM_GETNUMTICS Meldung (kommstrg. h)
description: Ruft die Anzahl der Teil Striche in einer TrackBar ab.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Windows-Steuerelemente für TBM_GETNUMTICS Meldung
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949591"
---
# <a name="tbm_getnumtics-message"></a><span data-ttu-id="9caf9-104">TBM \_ GetNumTics-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9caf9-104">TBM\_GETNUMTICS message</span></span>

<span data-ttu-id="9caf9-105">Ruft die Anzahl der Teil Striche in einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="9caf9-105">Retrieves the number of tick marks in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9caf9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9caf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9caf9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9caf9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9caf9-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9caf9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9caf9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9caf9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9caf9-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9caf9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9caf9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9caf9-111">Return value</span></span>

<span data-ttu-id="9caf9-112">Wenn kein [Tick-Flag](trackbar-control-styles.md) festgelegt ist, gibt es für den Anfangs-und den endticks den Wert 2 zurück.</span><span class="sxs-lookup"><span data-stu-id="9caf9-112">If no [tick flag](trackbar-control-styles.md) is set, it returns 2 for the beginning and ending ticks.</span></span> <span data-ttu-id="9caf9-113">Wenn " [**TSB \_ noticks**](trackbar-control-styles.md) " festgelegt ist, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9caf9-113">If [**TBS\_NOTICKS**](trackbar-control-styles.md) is set, it returns zero.</span></span> <span data-ttu-id="9caf9-114">Andernfalls nimmt Sie den Unterschied zwischen dem minimal-und Maximalwert des Bereichs, dividiert durch die Taktfrequenz und addiert 2.</span><span class="sxs-lookup"><span data-stu-id="9caf9-114">Otherwise, it takes the difference between the range minimum and maximum, divides by the tick frequency, and adds 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="9caf9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9caf9-115">Remarks</span></span>

<span data-ttu-id="9caf9-116">Die **TBM \_ GetNumTics** -Nachricht zählt alle Teil Striche, einschließlich der ersten und letzten Teil Striche, die von der TrackBar erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9caf9-116">The **TBM\_GETNUMTICS** message counts all of the tick marks, including the first and last tick marks created by the trackbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="9caf9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9caf9-117">Requirements</span></span>



| <span data-ttu-id="9caf9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9caf9-118">Requirement</span></span> | <span data-ttu-id="9caf9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9caf9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9caf9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9caf9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9caf9-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9caf9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9caf9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9caf9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9caf9-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9caf9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9caf9-124">Header</span><span class="sxs-lookup"><span data-stu-id="9caf9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9caf9-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9caf9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





