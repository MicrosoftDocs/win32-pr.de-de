---
title: TBM_GETPOS Meldung (kommstrg. h)
description: Ruft die aktuelle logische Position des Schiebereglers in einer TrackBar ab. Die logischen Positionen sind die ganzzahligen Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- Windows-Steuerelemente für TBM_GETPOS Meldung
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476806"
---
# <a name="tbm_getpos-message"></a><span data-ttu-id="888f7-105">TBM- \_ GetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="888f7-105">TBM\_GETPOS message</span></span>

<span data-ttu-id="888f7-106">Ruft die aktuelle logische Position des Schiebereglers in einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="888f7-106">Retrieves the current logical position of the slider in a trackbar.</span></span> <span data-ttu-id="888f7-107">Die logischen Positionen sind die ganzzahligen Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen.</span><span class="sxs-lookup"><span data-stu-id="888f7-107">The logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="888f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="888f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="888f7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="888f7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="888f7-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="888f7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="888f7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="888f7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="888f7-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="888f7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="888f7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="888f7-113">Return value</span></span>

<span data-ttu-id="888f7-114">Gibt einen 32-Bit-Wert zurück, der die aktuelle logische Position des Schiebereglers der Trackleiste angibt.</span><span class="sxs-lookup"><span data-stu-id="888f7-114">Returns a 32-bit value that specifies the current logical position of the trackbar's slider.</span></span>

## <a name="requirements"></a><span data-ttu-id="888f7-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="888f7-115">Requirements</span></span>



| <span data-ttu-id="888f7-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="888f7-116">Requirement</span></span> | <span data-ttu-id="888f7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="888f7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="888f7-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="888f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="888f7-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="888f7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="888f7-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="888f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="888f7-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="888f7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="888f7-122">Header</span><span class="sxs-lookup"><span data-stu-id="888f7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="888f7-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="888f7-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888f7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="888f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888f7-125">**TBM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="888f7-125">**TBM\_SETPOS**</span></span>](tbm-setpos.md)
</dt> </dl>

 

 





