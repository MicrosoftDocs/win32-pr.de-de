---
title: TBM_SETTIPSIDE Meldung (kommstrg. h)
description: Positioniert ein QuickInfo-Steuerelement von einem TrackBar-Steuerelement. TrackBar-Steuerelemente, die den TSB-Tooltips-Stil verwenden, zeigen Quick Infos an \_ .
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- Windows-Steuerelemente für TBM_SETTIPSIDE Meldung
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391714"
---
# <a name="tbm_settipside-message"></a><span data-ttu-id="87209-105">TBM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="87209-105">TBM\_SETTIPSIDE message</span></span>

<span data-ttu-id="87209-106">Positioniert ein QuickInfo-Steuerelement von einem TrackBar-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="87209-106">Positions a tooltip control used by a trackbar control.</span></span> <span data-ttu-id="87209-107">TrackBar-Steuerelemente, die den [**TSB- \_ Tooltips**](trackbar-control-styles.md) -Stil verwenden, zeigen Quick Infos an.</span><span class="sxs-lookup"><span data-stu-id="87209-107">Trackbar controls that use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style display tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="87209-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="87209-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87209-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87209-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87209-110">Wert, der die Position darstellt, an der das QuickInfo-Steuerelement angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="87209-110">Value representing the location at which to display the tooltip control.</span></span> <span data-ttu-id="87209-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="87209-111">This value can be one of the following:</span></span>



| <span data-ttu-id="87209-112">Wert</span><span class="sxs-lookup"><span data-stu-id="87209-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="87209-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="87209-113">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <span data-ttu-id="87209-114"><dt>**tbts- \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="87209-114"><dt>**TBTS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="87209-115">Das QuickInfo-Steuerelement befindet sich über der TrackBar.</span><span class="sxs-lookup"><span data-stu-id="87209-115">The tooltip control will be positioned above the trackbar.</span></span> <span data-ttu-id="87209-116">Dieses Flag ist für die Verwendung mit horizontalen trackbars vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="87209-116">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <span data-ttu-id="87209-117"><dt>**tbts \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="87209-117"><dt>**TBTS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="87209-118">Das ToolTip-Steuerelement wird auf der linken Seite der TrackBar positioniert.</span><span class="sxs-lookup"><span data-stu-id="87209-118">The tooltip control will be positioned to the left of the trackbar.</span></span> <span data-ttu-id="87209-119">Dieses Flag ist für die Verwendung mit vertikalen trackbars vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="87209-119">This flag is for use with vertical trackbars.</span></span><br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <span data-ttu-id="87209-120"><dt>**tbts \_ unten**</dt></span><span class="sxs-lookup"><span data-stu-id="87209-120"><dt>**TBTS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="87209-121">Das QuickInfo-Steuerelement befindet sich unterhalb der TrackBar.</span><span class="sxs-lookup"><span data-stu-id="87209-121">The tooltip control will be positioned below the trackbar.</span></span> <span data-ttu-id="87209-122">Dieses Flag ist für die Verwendung mit horizontalen trackbars vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="87209-122">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <span data-ttu-id="87209-123"><dt>**tbts \_ right**</dt></span><span class="sxs-lookup"><span data-stu-id="87209-123"><dt>**TBTS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="87209-124">Das QuickInfo-Steuerelement wird auf der rechten Seite der TrackBar positioniert.</span><span class="sxs-lookup"><span data-stu-id="87209-124">The tooltip control will be positioned to the right of the trackbar.</span></span> <span data-ttu-id="87209-125">Dieses Flag ist für die Verwendung mit vertikalen trackbars vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="87209-125">This flag is for use with vertical trackbars.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="87209-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87209-126">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87209-127">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="87209-127">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87209-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87209-128">Return value</span></span>

<span data-ttu-id="87209-129">Gibt einen Wert zurück, der die vorherige Position des QuickInfo-Steuer Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="87209-129">Returns a value that represents the tooltip control's previous location.</span></span> <span data-ttu-id="87209-130">Der Rückgabewert ist mit einem der möglichen Werte für *wParam* gleich.</span><span class="sxs-lookup"><span data-stu-id="87209-130">The return value equals one of the possible values for *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="87209-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87209-131">Requirements</span></span>



| <span data-ttu-id="87209-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87209-132">Requirement</span></span> | <span data-ttu-id="87209-133">Wert</span><span class="sxs-lookup"><span data-stu-id="87209-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87209-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87209-134">Minimum supported client</span></span><br/> | <span data-ttu-id="87209-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87209-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87209-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87209-136">Minimum supported server</span></span><br/> | <span data-ttu-id="87209-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87209-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87209-138">Header</span><span class="sxs-lookup"><span data-stu-id="87209-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="87209-139"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="87209-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





