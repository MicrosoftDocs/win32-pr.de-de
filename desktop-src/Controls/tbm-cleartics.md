---
title: TBM_CLEARTICS Meldung (kommstrg. h)
description: Entfernt die aktuellen Teil Striche aus einer TrackBar. Diese Meldung entfernt nicht die ersten und letzten Teil Striche, die automatisch von der TrackBar erstellt werden.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Windows-Steuerelemente für TBM_CLEARTICS Meldung
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475921"
---
# <a name="tbm_cleartics-message"></a><span data-ttu-id="d1872-105">TBM- \_ ClearTics-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d1872-105">TBM\_CLEARTICS message</span></span>

<span data-ttu-id="d1872-106">Entfernt die aktuellen Teil Striche aus einer TrackBar.</span><span class="sxs-lookup"><span data-stu-id="d1872-106">Removes the current tick marks from a trackbar.</span></span> <span data-ttu-id="d1872-107">Diese Meldung entfernt nicht die ersten und letzten Teil Striche, die automatisch von der TrackBar erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d1872-107">This message does not remove the first and last tick marks, which are created automatically by the trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1872-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1872-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1872-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1872-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1872-110">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d1872-110">Redraw flag.</span></span> <span data-ttu-id="d1872-111">Wenn dieser Parameter **true** ist, wird die TrackBar neu gezeichnet, nachdem die Teil Striche gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="d1872-111">If this parameter is **TRUE**, the trackbar is redrawn after the tick marks are cleared.</span></span> <span data-ttu-id="d1872-112">Wenn dieser Parameter **false** ist, löscht die Nachricht die Teil Striche, aber die TrackBar wird nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d1872-112">If this parameter is **FALSE**, the message clears the tick marks but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="d1872-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1872-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1872-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d1872-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1872-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1872-115">Return value</span></span>

<span data-ttu-id="d1872-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d1872-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1872-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1872-117">Requirements</span></span>



| <span data-ttu-id="d1872-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1872-118">Requirement</span></span> | <span data-ttu-id="d1872-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d1872-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1872-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1872-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1872-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1872-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1872-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1872-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1872-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1872-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1872-124">Header</span><span class="sxs-lookup"><span data-stu-id="d1872-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1872-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1872-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





