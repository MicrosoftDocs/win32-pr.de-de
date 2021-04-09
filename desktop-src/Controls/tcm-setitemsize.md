---
title: TCM_SETITEMSIZE Meldung (kommstrg. h)
description: Legt die Breite und Höhe von Registerkarten in einem Registerkarten-Steuerelement mit fester Breite oder einem vom Besitzer gezeichneten Steuerelement fest Sie können diese Nachricht explizit oder mithilfe des tabctrl-Objekts tabstrg * senden \_ .
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- Windows-Steuerelemente für TCM_SETITEMSIZE Meldung
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858632"
---
# <a name="tcm_setitemsize-message"></a><span data-ttu-id="f39b2-105">TCM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="f39b2-105">TCM\_SETITEMSIZE message</span></span>

<span data-ttu-id="f39b2-106">Legt die Breite und Höhe von Registerkarten in einem Registerkarten-Steuerelement mit fester Breite oder einem vom Besitzer gezeichneten Steuerelement fest</span><span class="sxs-lookup"><span data-stu-id="f39b2-106">Sets the width and height of tabs in a fixed-width or owner-drawn tab control.</span></span> <span data-ttu-id="f39b2-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Objekts \_ tabstrg**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) \* senden.</span><span class="sxs-lookup"><span data-stu-id="f39b2-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f39b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f39b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f39b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f39b2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f39b2-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f39b2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f39b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f39b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f39b2-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **int** -Wert, der die neue Breite in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="f39b2-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the new width, in pixels.</span></span> <span data-ttu-id="f39b2-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **int** -Wert, der die neue Höhe in Pixel angibt.</span><span class="sxs-lookup"><span data-stu-id="f39b2-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the new height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f39b2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f39b2-114">Return value</span></span>

<span data-ttu-id="f39b2-115">Gibt die alte Breite und Höhe zurück.</span><span class="sxs-lookup"><span data-stu-id="f39b2-115">Returns the old width and height.</span></span> <span data-ttu-id="f39b2-116">Die Breite liegt im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des Rückgabewerts, und die Höhe liegt im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))-Wert.</span><span class="sxs-lookup"><span data-stu-id="f39b2-116">The width is in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the height is in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="f39b2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f39b2-117">Remarks</span></span>

<span data-ttu-id="f39b2-118">Wenn die Breite auf einen Wert festgelegt ist, der kleiner als die von [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)festgelegte Bildbreite ist, wird die Breite der Registerkarte auf den niedrigsten Wert festgelegt, der größer ist als die Breite des Bilds.</span><span class="sxs-lookup"><span data-stu-id="f39b2-118">If the width is set to a value less than the image width set by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), the width of the tab is set to the lowest value that is greater than the image width.</span></span>

## <a name="requirements"></a><span data-ttu-id="f39b2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f39b2-119">Requirements</span></span>



| <span data-ttu-id="f39b2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f39b2-120">Requirement</span></span> | <span data-ttu-id="f39b2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f39b2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f39b2-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f39b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f39b2-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f39b2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f39b2-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f39b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f39b2-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f39b2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f39b2-126">Header</span><span class="sxs-lookup"><span data-stu-id="f39b2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f39b2-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f39b2-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

