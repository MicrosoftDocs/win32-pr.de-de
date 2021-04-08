---
title: TBM_SETSEL Meldung (kommstrg. h)
description: Legt die Anfangs-und Endpositionen für den verfügbaren Auswahlbereich in einer TrackBar fest.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- Windows-Steuerelemente für TBM_SETSEL Meldung
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739904"
---
# <a name="tbm_setsel-message"></a><span data-ttu-id="860dc-104">TBM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="860dc-104">TBM\_SETSEL message</span></span>

<span data-ttu-id="860dc-105">Legt die Anfangs-und Endpositionen für den verfügbaren Auswahlbereich in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="860dc-105">Sets the starting and ending positions for the available selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="860dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="860dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="860dc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="860dc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="860dc-108">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="860dc-108">Redraw flag.</span></span> <span data-ttu-id="860dc-109">Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Auswahlbereich festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="860dc-109">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="860dc-110">Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Auswahlbereich fest, aber die TrackBar wird nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="860dc-110">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="860dc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="860dc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="860dc-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die logische Startposition für den Auswahlbereich an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die logische Endposition an.</span><span class="sxs-lookup"><span data-stu-id="860dc-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the starting logical position for the selection range, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the ending logical position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="860dc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="860dc-113">Return value</span></span>

<span data-ttu-id="860dc-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="860dc-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="860dc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="860dc-115">Remarks</span></span>

<span data-ttu-id="860dc-116">Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt.</span><span class="sxs-lookup"><span data-stu-id="860dc-116">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

<span data-ttu-id="860dc-117">**TBM \_** Mithilfe von "-tsel" können Sie den Zeiger auf einen Teil des Bereichs beschränken, der für die Statusanzeige verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="860dc-117">**TBM\_SETSEL** allows you to restrict the pointer to only a portion of the range available to the progress bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="860dc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="860dc-118">Requirements</span></span>



| <span data-ttu-id="860dc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="860dc-119">Requirement</span></span> | <span data-ttu-id="860dc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="860dc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="860dc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="860dc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="860dc-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="860dc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="860dc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="860dc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="860dc-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="860dc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="860dc-125">Header</span><span class="sxs-lookup"><span data-stu-id="860dc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="860dc-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="860dc-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="860dc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="860dc-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="860dc-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="860dc-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="860dc-129">**TBM- \_ getselend**</span><span class="sxs-lookup"><span data-stu-id="860dc-129">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="860dc-130">**TBM \_ getselstart**</span><span class="sxs-lookup"><span data-stu-id="860dc-130">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="860dc-131">**TBM- \_ setselend**</span><span class="sxs-lookup"><span data-stu-id="860dc-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="860dc-132">**TBM- \_ setselstart**</span><span class="sxs-lookup"><span data-stu-id="860dc-132">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

