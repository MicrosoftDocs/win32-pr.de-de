---
title: BM_GETCHECK Meldung (Winuser. h)
description: Ruft den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das Schaltfläche \_ getcheck-Makro verwenden.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- Windows-Steuerelemente für BM_GETCHECK Meldung
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105770"
---
# <a name="bm_getcheck-message"></a><span data-ttu-id="1a753-105">BM- \_ getcheck-Meldung</span><span class="sxs-lookup"><span data-stu-id="1a753-105">BM\_GETCHECK message</span></span>

<span data-ttu-id="1a753-106">Ruft den Status der Überprüfung eines Options Felds oder eines Kontrollkästchens ab.</span><span class="sxs-lookup"><span data-stu-id="1a753-106">Gets the check state of a radio button or check box.</span></span> <span data-ttu-id="1a753-107">Sie können diese Nachricht explizit senden oder das [**Schaltfläche \_ getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a753-107">You can send this message explicitly or use the [**Button\_GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a753-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a753-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a753-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a753-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a753-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="1a753-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a753-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a753-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a753-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="1a753-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a753-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a753-113">Return value</span></span>

<span data-ttu-id="1a753-114">Der Rückgabewert einer Schaltfläche, die mit dem Format " [**\_ Auto Checkbox**](button-styles.md)", " [**SB \_ AUTORADIOBUTTON**](button-styles.md)", "SB [**\_ AUTO3STATE**](button-styles.md)", "SB [**", " \_**](button-styles.md) [**SB \_ RadioButton**](button-styles.md)" oder " [**SB \_ 3STATE**](button-styles.md) " erstellt wurde, kann eines der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="1a753-114">The return value from a button created with the [**BS\_AUTOCHECKBOX**](button-styles.md), [**BS\_AUTORADIOBUTTON**](button-styles.md), [**BS\_AUTO3STATE**](button-styles.md), [**BS\_CHECKBOX**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), or [**BS\_3STATE**](button-styles.md) style can be one of the following.</span></span>



| <span data-ttu-id="1a753-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1a753-115">Return code</span></span>                                                                                       | <span data-ttu-id="1a753-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a753-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a753-117"><dt>**BST \_ aktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="1a753-117"><dt>**BST\_CHECKED**</dt></span></span> </dl>       | <span data-ttu-id="1a753-118">Die Schaltfläche ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1a753-118">Button is checked.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1a753-119"><dt>**BST \_ unbestimmt**</dt></span><span class="sxs-lookup"><span data-stu-id="1a753-119"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="1a753-120">Die Schaltfläche ist abgeblendet und zeigt einen unbestimmten Zustand an (gilt nur, wenn die Schaltfläche den Typ " [**\_ 3STATE**](button-styles.md) " oder " [**SB \_ AUTO3STATE**](button-styles.md) " aufweist).</span><span class="sxs-lookup"><span data-stu-id="1a753-120">Button is grayed, indicating an indeterminate state (applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style).</span></span><br/> |
| <dl> <span data-ttu-id="1a753-121"><dt>**BST \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="1a753-121"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>     | <span data-ttu-id="1a753-122">Schaltfläche ist deaktiviert</span><span class="sxs-lookup"><span data-stu-id="1a753-122">Button is cleared</span></span><br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="1a753-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a753-123">Remarks</span></span>

<span data-ttu-id="1a753-124">Wenn die Schaltfläche einen anderen Stil als die aufgeführten hat, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1a753-124">If the button has a style other than those listed, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a753-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a753-125">Requirements</span></span>



| <span data-ttu-id="1a753-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a753-126">Requirement</span></span> | <span data-ttu-id="1a753-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1a753-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a753-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a753-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a753-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a753-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a753-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a753-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a753-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a753-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a753-132">Header</span><span class="sxs-lookup"><span data-stu-id="1a753-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a753-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1a753-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a753-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a753-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a753-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1a753-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a753-136">**BM \_ GetState**</span><span class="sxs-lookup"><span data-stu-id="1a753-136">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="1a753-137">**BM- \_ setcheck**</span><span class="sxs-lookup"><span data-stu-id="1a753-137">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





