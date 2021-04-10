---
title: BM_SETCHECK Meldung (Winuser. h)
description: Legt den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens fest. Sie können diese Nachricht explizit oder mithilfe des Schaltflächen \_ setcheck-Makros senden.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- Windows-Steuerelemente für BM_SETCHECK Meldung
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040188"
---
# <a name="bm_setcheck-message"></a><span data-ttu-id="593e1-105">BM- \_ setcheck-Meldung</span><span class="sxs-lookup"><span data-stu-id="593e1-105">BM\_SETCHECK message</span></span>

<span data-ttu-id="593e1-106">Legt den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens fest.</span><span class="sxs-lookup"><span data-stu-id="593e1-106">Sets the check state of a radio button or check box.</span></span> <span data-ttu-id="593e1-107">Sie können diese Nachricht explizit oder mithilfe des Schaltflächen [**\_ setcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="593e1-107">You can send this message explicitly or by using the [**Button\_SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="593e1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="593e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="593e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="593e1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="593e1-110">Der Status der Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="593e1-110">The check state.</span></span> <span data-ttu-id="593e1-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="593e1-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="593e1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="593e1-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="593e1-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="593e1-113">Meaning</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <span data-ttu-id="593e1-114"><dt>**BST \_ aktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="593e1-114"><dt>**BST\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="593e1-115">Legt den Schaltflächen Zustand auf aktiviert fest.</span><span class="sxs-lookup"><span data-stu-id="593e1-115">Sets the button state to checked.</span></span><br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <span data-ttu-id="593e1-116"><dt>**BST \_ unbestimmt**</dt></span><span class="sxs-lookup"><span data-stu-id="593e1-116"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="593e1-117">Legt den Zustand der Schaltfläche auf abgeblendet fest und gibt einen unbestimmten Zustand an.</span><span class="sxs-lookup"><span data-stu-id="593e1-117">Sets the button state to grayed, indicating an indeterminate state.</span></span> <span data-ttu-id="593e1-118">Verwenden Sie diesen Wert nur, wenn die Schaltfläche den Stil " [**\_ 3STATE**](button-styles.md) " oder " [**SB \_ AUTO3STATE**](button-styles.md) " aufweist.</span><span class="sxs-lookup"><span data-stu-id="593e1-118">Use this value only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <span data-ttu-id="593e1-119"><dt>**BST \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="593e1-119"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>             | <span data-ttu-id="593e1-120">Legt den Schaltflächen Zustand auf "deaktiviert" fest.</span><span class="sxs-lookup"><span data-stu-id="593e1-120">Sets the button state to cleared.</span></span><br/>                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="593e1-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="593e1-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="593e1-122">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="593e1-122">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="593e1-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="593e1-123">Return value</span></span>

<span data-ttu-id="593e1-124">Diese Meldung gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="593e1-124">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="593e1-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="593e1-125">Remarks</span></span>

<span data-ttu-id="593e1-126">Die **BM- \_ setcheck** -Nachricht hat keine Auswirkung auf die pushschaltflächen.</span><span class="sxs-lookup"><span data-stu-id="593e1-126">The **BM\_SETCHECK** message has no effect on push buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="593e1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="593e1-127">Requirements</span></span>



| <span data-ttu-id="593e1-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="593e1-128">Requirement</span></span> | <span data-ttu-id="593e1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="593e1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="593e1-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="593e1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="593e1-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="593e1-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="593e1-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="593e1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="593e1-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="593e1-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="593e1-134">Header</span><span class="sxs-lookup"><span data-stu-id="593e1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="593e1-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="593e1-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="593e1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="593e1-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="593e1-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="593e1-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="593e1-138">**BM \_ getcheck**</span><span class="sxs-lookup"><span data-stu-id="593e1-138">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="593e1-139">**BM \_ GetState**</span><span class="sxs-lookup"><span data-stu-id="593e1-139">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="593e1-140">**BM \_ SetState**</span><span class="sxs-lookup"><span data-stu-id="593e1-140">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





