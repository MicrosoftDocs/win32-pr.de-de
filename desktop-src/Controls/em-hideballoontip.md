---
title: EM_HIDEBALLOONTIP Meldung (kommstrg. h)
description: Blendet jede Sprechblase aus, die einem Bearbeitungs Steuerelement zugeordnet ist.
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- Windows-Steuerelemente für EM_HIDEBALLOONTIP Meldung
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949491"
---
# <a name="em_hideballoontip-message"></a><span data-ttu-id="2f466-104">EM \_ hideballoontip-Meldung</span><span class="sxs-lookup"><span data-stu-id="2f466-104">EM\_HIDEBALLOONTIP message</span></span>

<span data-ttu-id="2f466-105">Blendet jede Sprechblase aus, die einem Bearbeitungs Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2f466-105">Hides any balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f466-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f466-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f466-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f466-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f466-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2f466-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2f466-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f466-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f466-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2f466-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f466-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f466-111">Return value</span></span>

<span data-ttu-id="2f466-112">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f466-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="2f466-113">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2f466-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f466-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f466-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2f466-115">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="2f466-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2f466-116">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2f466-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f466-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f466-117">Requirements</span></span>



| <span data-ttu-id="2f466-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f466-118">Requirement</span></span> | <span data-ttu-id="2f466-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2f466-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f466-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f466-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f466-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f466-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f466-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f466-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f466-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f466-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f466-124">Header</span><span class="sxs-lookup"><span data-stu-id="2f466-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f466-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f466-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f466-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f466-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f466-127">**\_Hideballoontip bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="2f466-127">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





