---
title: ACM_PLAY Meldung (kommstrg. h)
description: Gibt einen AVI-Clip in einem Animations Steuerelement wieder. Das-Steuerelement spielt den Clip im Hintergrund, während der Thread weiterhin ausgeführt wird. Sie können diese Nachricht explizit oder mit dem animieren Play- \_ Makro senden.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- Windows-Steuerelemente für ACM_PLAY Meldung
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475759"
---
# <a name="acm_play-message"></a><span data-ttu-id="87759-106">ACM- \_ Wiedergabe Meldung</span><span class="sxs-lookup"><span data-stu-id="87759-106">ACM\_PLAY message</span></span>

<span data-ttu-id="87759-107">Gibt einen AVI-Clip in einem Animations Steuerelement wieder.</span><span class="sxs-lookup"><span data-stu-id="87759-107">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="87759-108">Das-Steuerelement spielt den Clip im Hintergrund, während der Thread weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87759-108">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="87759-109">Sie können diese Nachricht explizit oder mit dem [**animieren \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="87759-109">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="87759-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="87759-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87759-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87759-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87759-112">Ein **uint** , das angibt, wie oft der AVI-Clip wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="87759-112">A **UINT** that specifies the number of times to replay the AVI clip.</span></span> <span data-ttu-id="87759-113">Der Wert-1 bedeutet, dass der Clip unbegrenzt wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="87759-113">A value of -1 means replay the clip indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="87759-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87759-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87759-115">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der null basierte Index des Frames, bei dem die Wiedergabe beginnt.</span><span class="sxs-lookup"><span data-stu-id="87759-115">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the zero-based index of the frame where playing begins.</span></span> <span data-ttu-id="87759-116">Der Wert muss kleiner als 65.536 sein.</span><span class="sxs-lookup"><span data-stu-id="87759-116">The value must be less than 65,536.</span></span> <span data-ttu-id="87759-117">Der Wert NULL bedeutet, mit dem ersten Frame im AVI-Clip zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="87759-117">A value of zero means begin with the first frame in the AVI clip.</span></span>

<span data-ttu-id="87759-118">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist der null basierte Index des Frames, bei dem die Wiedergabe beendet wird.</span><span class="sxs-lookup"><span data-stu-id="87759-118">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the zero-based index of the frame where playing ends.</span></span> <span data-ttu-id="87759-119">Der Wert muss kleiner als 65.536 sein.</span><span class="sxs-lookup"><span data-stu-id="87759-119">The value must be less than 65,536.</span></span> <span data-ttu-id="87759-120">Der Wert-1 bedeutet, dass er mit dem letzten Frame im AVI-Clip endet.</span><span class="sxs-lookup"><span data-stu-id="87759-120">A value of -1 means end with the last frame in the AVI clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87759-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87759-121">Return value</span></span>

<span data-ttu-id="87759-122">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="87759-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87759-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87759-123">Remarks</span></span>

<span data-ttu-id="87759-124">Mithilfe von [**animieren \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) können Sie das Animations Steuerelement so anleiten, dass ein bestimmter Frame des AVI-Clips angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="87759-124">You can use [**Animate\_Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) to direct the animation control to display a particular frame of the AVI clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="87759-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87759-125">Requirements</span></span>



| <span data-ttu-id="87759-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87759-126">Requirement</span></span> | <span data-ttu-id="87759-127">Wert</span><span class="sxs-lookup"><span data-stu-id="87759-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87759-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="87759-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87759-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87759-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87759-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="87759-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87759-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="87759-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87759-132">Header</span><span class="sxs-lookup"><span data-stu-id="87759-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="87759-133"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="87759-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

