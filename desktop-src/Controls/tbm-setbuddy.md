---
title: TBM_SETBUDDY Meldung (kommstrg. h)
description: Weist ein Fenster als Buddy-Fenster für ein TrackBar-Steuerelement zu. TrackBar-Buddy-Fenster werden automatisch an einem Speicherort relativ zur Ausrichtung des Steuer Elements angezeigt (horizontal oder vertikal).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- Windows-Steuerelemente für TBM_SETBUDDY Meldung
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040308"
---
# <a name="tbm_setbuddy-message"></a><span data-ttu-id="e6e4a-105">TBM- \_ SetBuddy-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e6e4a-105">TBM\_SETBUDDY message</span></span>

<span data-ttu-id="e6e4a-106">Weist ein Fenster als Buddy-Fenster für ein TrackBar-Steuerelement zu.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-106">Assigns a window as the buddy window for a trackbar control.</span></span> <span data-ttu-id="e6e4a-107">TrackBar-Buddy-Fenster werden automatisch an einem Speicherort relativ zur Ausrichtung des Steuer Elements angezeigt (horizontal oder vertikal).</span><span class="sxs-lookup"><span data-stu-id="e6e4a-107">Trackbar buddy windows are automatically displayed in a location relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="e6e4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6e4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e4a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6e4a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e4a-110">-Wert, der die Position angibt, an der das Buddy-Fenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-110">Value specifying the location at which to display the buddy window.</span></span> <span data-ttu-id="e6e4a-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e6e4a-111">This value can be one of the following:</span></span>



| <span data-ttu-id="e6e4a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e6e4a-112">Value</span></span>                                                                                                                                | <span data-ttu-id="e6e4a-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e6e4a-113">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="e6e4a-114"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e4a-114"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="e6e4a-115">Der Kumpel wird links neben der TrackBar angezeigt, wenn das TrackBar-Steuerelement den [**TSB- \_ Horz**](trackbar-control-styles.md) -Stil verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-115">The buddy will appear to the left of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="e6e4a-116">Wenn die TrackBar den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, wird der Kumpel oberhalb des TrackBar-Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-116">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears above the trackbar control.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="e6e4a-117"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e4a-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="e6e4a-118">Der Kumpel wird rechts von der TrackBar angezeigt, wenn das TrackBar-Steuerelement den Stil von " [**TSB \_ Horz**](trackbar-control-styles.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-118">The buddy will appear to the right of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="e6e4a-119">Wenn die TrackBar den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, wird der Buddy unterhalb des TrackBar-Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-119">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears below the trackbar control.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6e4a-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6e4a-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e4a-121">Handle für das Fenster, das als Buddy des TrackBar-Steuer Elements festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-121">Handle to the window that will be set as the trackbar control's buddy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e4a-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6e4a-122">Return value</span></span>

<span data-ttu-id="e6e4a-123">Gibt das Handle für das Fenster zurück, das zuvor dem Steuerelement an dieser Position zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-123">Returns the handle to the window that was previously assigned to the control at that location.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e4a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6e4a-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6e4a-125">TrackBar-Steuerelemente unterstützen bis zu zwei Buddy-Fenster.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-125">Trackbar controls support up to two buddy windows.</span></span> <span data-ttu-id="e6e4a-126">Dies kann hilfreich sein, wenn Sie Text oder Bilder an jedem Ende des Steuer Elements anzeigen müssen.</span><span class="sxs-lookup"><span data-stu-id="e6e4a-126">This can be useful when you must display text or images at each end of the control.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6e4a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6e4a-127">Requirements</span></span>



| <span data-ttu-id="e6e4a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6e4a-128">Requirement</span></span> | <span data-ttu-id="e6e4a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e6e4a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e4a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6e4a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e4a-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e4a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6e4a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6e4a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e4a-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6e4a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6e4a-134">Header</span><span class="sxs-lookup"><span data-stu-id="e6e4a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e4a-135"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e4a-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





