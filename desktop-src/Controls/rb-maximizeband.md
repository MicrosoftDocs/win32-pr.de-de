---
title: RB_MAXIMIZEBAND Meldung (kommstrg. h)
description: Ändert die Größe eines Bands in einem Grund leisten-Steuerelement entweder auf seine ideale oder größte Größe.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- Windows-Steuerelemente für RB_MAXIMIZEBAND Meldung
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859070"
---
# <a name="rb_maximizeband-message"></a><span data-ttu-id="bbf4e-104">RB \_ maximizeband-Meldung</span><span class="sxs-lookup"><span data-stu-id="bbf4e-104">RB\_MAXIMIZEBAND message</span></span>

<span data-ttu-id="bbf4e-105">Ändert die Größe eines Bands in einem Grund leisten-Steuerelement entweder auf seine ideale oder größte Größe.</span><span class="sxs-lookup"><span data-stu-id="bbf4e-105">Resizes a band in a rebar control to either its ideal or largest size.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbf4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbf4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf4e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbf4e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf4e-108">Der null basierte Index des zu maximier enden Bands.</span><span class="sxs-lookup"><span data-stu-id="bbf4e-108">Zero-based index of the band to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="bbf4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbf4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf4e-110">Gibt an, ob die ideale Breite des Bands verwendet werden soll, wenn das Band maximiert ist.</span><span class="sxs-lookup"><span data-stu-id="bbf4e-110">Indicates if the ideal width of the band should be used when the band is maximized.</span></span> <span data-ttu-id="bbf4e-111">Wenn dieser Wert ungleich 0 (null) ist, wird die ideale Breite verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbf4e-111">If this value is nonzero, the ideal width will be used.</span></span> <span data-ttu-id="bbf4e-112">Wenn dieser Wert 0 (null) ist, wird das Band so groß wie möglich gemacht.</span><span class="sxs-lookup"><span data-stu-id="bbf4e-112">If this value is zero, the band will be made as large as possible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf4e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbf4e-113">Return value</span></span>

<span data-ttu-id="bbf4e-114">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbf4e-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf4e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbf4e-115">Requirements</span></span>



| <span data-ttu-id="bbf4e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbf4e-116">Requirement</span></span> | <span data-ttu-id="bbf4e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bbf4e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf4e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbf4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf4e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbf4e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbf4e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbf4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf4e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbf4e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbf4e-122">Header</span><span class="sxs-lookup"><span data-stu-id="bbf4e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf4e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf4e-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf4e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbf4e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbf4e-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="bbf4e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bbf4e-126">**RB \_ SetBandInfo**</span><span class="sxs-lookup"><span data-stu-id="bbf4e-126">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





