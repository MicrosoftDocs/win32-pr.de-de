---
title: BCM_SETTEXTMARGIN Meldung (kommstrg. h)
description: Die BCM \_ settextmargin-Meldung legt die Ränder zum Zeichnen von Text in einem Schaltflächen-Steuerelement fest.
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- Windows-Steuerelemente für BCM_SETTEXTMARGIN Meldung
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb6653007c155a508ce4da899a7be0d8ff2ab2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476659"
---
# <a name="bcm_settextmargin-message"></a><span data-ttu-id="97dc1-104">BCM- \_ settextmargin-Meldung</span><span class="sxs-lookup"><span data-stu-id="97dc1-104">BCM\_SETTEXTMARGIN message</span></span>

<span data-ttu-id="97dc1-105">Die **BCM \_ settextmargin** -Meldung legt die Ränder zum Zeichnen von Text in einem Schaltflächen-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="97dc1-105">The **BCM\_SETTEXTMARGIN** message sets the margins for drawing text in a button control.</span></span>

## <a name="parameters"></a><span data-ttu-id="97dc1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97dc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97dc1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97dc1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97dc1-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="97dc1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="97dc1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97dc1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97dc1-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Ränder angibt, die zum Zeichnen von Text verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="97dc1-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97dc1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97dc1-111">Return value</span></span>

<span data-ttu-id="97dc1-112">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97dc1-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="97dc1-113">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97dc1-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97dc1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97dc1-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="97dc1-115">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="97dc1-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="97dc1-116">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="97dc1-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97dc1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97dc1-117">Requirements</span></span>



| <span data-ttu-id="97dc1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97dc1-118">Requirement</span></span> | <span data-ttu-id="97dc1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="97dc1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97dc1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97dc1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97dc1-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97dc1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97dc1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97dc1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97dc1-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97dc1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97dc1-124">Header</span><span class="sxs-lookup"><span data-stu-id="97dc1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97dc1-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="97dc1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97dc1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97dc1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="97dc1-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="97dc1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97dc1-128">**Schaltfläche " \_ settextmargin"**</span><span class="sxs-lookup"><span data-stu-id="97dc1-128">**Button\_SetTextMargin**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

<span data-ttu-id="97dc1-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="97dc1-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="97dc1-130">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="97dc1-130">Buttons</span></span>](buttons.md)
</dt> </dl>

 

