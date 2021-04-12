---
title: EM_GETCTFOPENSTATUS Meldung (RichEdit. h)
description: Bestimmt, ob die TSF-Tastatur (Text Services Framework) geöffnet oder geschlossen ist.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- Windows-Steuerelemente für EM_GETCTFOPENSTATUS Meldung
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956581"
---
# <a name="em_getctfopenstatus-message"></a><span data-ttu-id="905a8-104">EM \_ getctfopenstatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="905a8-104">EM\_GETCTFOPENSTATUS message</span></span>

<span data-ttu-id="905a8-105">Bestimmt, ob die TSF-Tastatur (Text Services Framework) geöffnet oder geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="905a8-105">Determines if the Text Services Framework (TSF) keyboard is open or closed.</span></span>

## <a name="parameters"></a><span data-ttu-id="905a8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="905a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905a8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="905a8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="905a8-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="905a8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="905a8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="905a8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="905a8-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="905a8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="905a8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="905a8-111">Return value</span></span>

<span data-ttu-id="905a8-112">Wenn die TSF-Tastatur geöffnet ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="905a8-112">If the TSF keyboard is open, the return value is **TRUE**.</span></span> <span data-ttu-id="905a8-113">Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="905a8-113">Otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="905a8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="905a8-114">Requirements</span></span>



| <span data-ttu-id="905a8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="905a8-115">Requirement</span></span> | <span data-ttu-id="905a8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="905a8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="905a8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="905a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="905a8-118">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="905a8-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="905a8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="905a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="905a8-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="905a8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="905a8-121">Header</span><span class="sxs-lookup"><span data-stu-id="905a8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="905a8-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="905a8-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="905a8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="905a8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905a8-124">**EM \_ setctfopenstatus**</span><span class="sxs-lookup"><span data-stu-id="905a8-124">**EM\_SETCTFOPENSTATUS**</span></span>](em-setctfopenstatus.md)
</dt> </dl>

 

 





