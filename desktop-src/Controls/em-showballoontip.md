---
title: EM_SHOWBALLOONTIP Meldung (kommstrg. h)
description: Die "em \_ ShowBalloonTip"-Meldung zeigt eine Sprechblase an, die einem Bearbeitungs Steuerelement zugeordnet ist.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- Windows-Steuerelemente für EM_SHOWBALLOONTIP Meldung
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104205"
---
# <a name="em_showballoontip-message"></a><span data-ttu-id="87271-104">EM \_ ShowBalloonTip-Meldung</span><span class="sxs-lookup"><span data-stu-id="87271-104">EM\_SHOWBALLOONTIP message</span></span>

<span data-ttu-id="87271-105">Die " **EM \_ ShowBalloonTip** "-Meldung zeigt eine Sprechblase an, die einem Bearbeitungs Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87271-105">The **EM\_SHOWBALLOONTIP** message displays a balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="87271-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87271-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87271-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87271-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="87271-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="87271-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87271-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87271-110">Ein Zeiger auf eine [**editballoontip**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) -Struktur, die Informationen über die anzuzeigende Sprechblasen info enthält.</span><span class="sxs-lookup"><span data-stu-id="87271-110">A pointer to an [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) structure that contains information about the balloon tip to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87271-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87271-111">Return value</span></span>

<span data-ttu-id="87271-112">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87271-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="87271-113">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87271-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="87271-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87271-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87271-115">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="87271-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="87271-116">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="87271-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87271-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87271-117">Requirements</span></span>



| <span data-ttu-id="87271-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87271-118">Requirement</span></span> | <span data-ttu-id="87271-119">Wert</span><span class="sxs-lookup"><span data-stu-id="87271-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87271-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87271-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87271-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87271-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87271-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87271-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87271-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87271-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87271-124">Header</span><span class="sxs-lookup"><span data-stu-id="87271-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87271-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="87271-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87271-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87271-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="87271-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="87271-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="87271-128">**Editballoontip**</span><span class="sxs-lookup"><span data-stu-id="87271-128">**EDITBALLOONTIP**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[<span data-ttu-id="87271-129">**\_ShowBalloonTip bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="87271-129">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





