---
title: EM_SETCTFOPENSTATUS Meldung (RichEdit. h)
description: Öffnet oder schließt die TSF-Tastatur (Text Services Framework).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Windows-Steuerelemente für EM_SETCTFOPENSTATUS Meldung
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040899"
---
# <a name="em_setctfopenstatus-message"></a><span data-ttu-id="9a40b-104">EM \_ setctfopenstatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="9a40b-104">EM\_SETCTFOPENSTATUS message</span></span>

<span data-ttu-id="9a40b-105">Öffnet oder schließt die TSF-Tastatur (Text Services Framework).</span><span class="sxs-lookup"><span data-stu-id="9a40b-105">Opens or closes the Text Services Framework (TSF) keyboard.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a40b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a40b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a40b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a40b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a40b-108">Verwenden Sie " **true**", um die TSF-Tastatur zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9a40b-108">To turn on the TSF keyboard, use **TRUE**.</span></span> <span data-ttu-id="9a40b-109">Um die TSF-Tastatur zu deaktivieren, verwenden Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="9a40b-109">To turn off the TSF keyboard, use **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9a40b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a40b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a40b-111">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9a40b-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a40b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a40b-112">Return value</span></span>

<span data-ttu-id="9a40b-113">Bei erfolgreicher Ausführung gibt diese Meldung **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a40b-113">If successful, this message returns **TRUE**.</span></span> <span data-ttu-id="9a40b-114">Wenn nicht erfolgreich, gibt diese Meldung **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a40b-114">If unsuccessful, this message returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a40b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a40b-115">Requirements</span></span>



| <span data-ttu-id="9a40b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a40b-116">Requirement</span></span> | <span data-ttu-id="9a40b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9a40b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a40b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a40b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9a40b-119">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a40b-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a40b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a40b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9a40b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a40b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a40b-122">Header</span><span class="sxs-lookup"><span data-stu-id="9a40b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a40b-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a40b-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a40b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a40b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a40b-125">**EM \_ getctfopenstatus**</span><span class="sxs-lookup"><span data-stu-id="9a40b-125">**EM\_GETCTFOPENSTATUS**</span></span>](em-getctfopenstatus.md)
</dt> </dl>

 

 





