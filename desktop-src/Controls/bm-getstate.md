---
title: BM_GETSTATE Meldung (Winuser. h)
description: Ruft den Zustand einer Schaltfläche oder eines Kontrollkästchens ab. Sie können diese Nachricht explizit senden oder das GetState-Makro der Schaltfläche verwenden \_ .
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- Windows-Steuerelemente für BM_GETSTATE Meldung
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949471"
---
# <a name="bm_getstate-message"></a><span data-ttu-id="a0d24-105">BM \_ GetState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a0d24-105">BM\_GETSTATE message</span></span>

<span data-ttu-id="a0d24-106">Ruft den Zustand einer Schaltfläche oder eines Kontrollkästchens ab.</span><span class="sxs-lookup"><span data-stu-id="a0d24-106">Retrieves the state of a button or check box.</span></span> <span data-ttu-id="a0d24-107">Sie können diese Nachricht explizit senden oder das [**\_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) -Makro der Schaltfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0d24-107">You can send this message explicitly or use the [**Button\_GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0d24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0d24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0d24-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0d24-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0d24-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a0d24-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0d24-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0d24-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0d24-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a0d24-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0d24-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0d24-113">Return value</span></span>

<span data-ttu-id="a0d24-114">Der Rückgabewert gibt den aktuellen Zustand der Schaltfläche an.</span><span class="sxs-lookup"><span data-stu-id="a0d24-114">The return value specifies the current state of the button.</span></span> <span data-ttu-id="a0d24-115">Es handelt sich um eine Kombination der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="a0d24-115">It is a combination of the following values.</span></span>



| <span data-ttu-id="a0d24-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a0d24-116">Return code</span></span>                                                                                        | <span data-ttu-id="a0d24-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0d24-117">Description</span></span>                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0d24-118"><dt>**BST \_ aktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-118"><dt>**BST\_CHECKED**</dt></span></span> </dl>        | <span data-ttu-id="a0d24-119">Die Schaltfläche ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0d24-119">The button is checked.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="a0d24-120"><dt>**BST \_ dropdownpushübertragung**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-120"><dt>**BST\_DROPDOWNPUSHED**</dt></span></span> </dl> | <span data-ttu-id="a0d24-121">[Windows Vista](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a0d24-121">[Windows Vista](common-control-versions.md).</span></span> <span data-ttu-id="a0d24-122">Die Schaltfläche befindet sich im Dropdown Zustand.</span><span class="sxs-lookup"><span data-stu-id="a0d24-122">The button is in the drop-down state.</span></span> <span data-ttu-id="a0d24-123">Gilt nur, wenn die Schaltfläche den [**tbstyle- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil aufweist.</span><span class="sxs-lookup"><span data-stu-id="a0d24-123">Applies only if the button has the [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span><br/> |
| <dl> <span data-ttu-id="a0d24-124"><dt>**BST- \_ Fokus**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-124"><dt>**BST\_FOCUS**</dt></span></span> </dl>          | <span data-ttu-id="a0d24-125">Die Schaltfläche verfügt über den Tastaturfokus.</span><span class="sxs-lookup"><span data-stu-id="a0d24-125">The button has the keyboard focus.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="a0d24-126"><dt>**BST \_ heiß**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-126"><dt>**BST\_HOT**</dt></span></span> </dl>            | <span data-ttu-id="a0d24-127">Die Schaltfläche ist "Hot". Das heißt, dass der Mauszeiger darüber bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="a0d24-127">The button is hot; that is, the mouse is hovering over it.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="a0d24-128"><dt>**BST \_ unbestimmt**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-128"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl>  | <span data-ttu-id="a0d24-129">Der Status der Schaltfläche ist unbestimmt.</span><span class="sxs-lookup"><span data-stu-id="a0d24-129">The state of the button is indeterminate.</span></span> <span data-ttu-id="a0d24-130">Gilt nur, wenn die Schaltfläche den Stil " [**\_ 3STATE**](button-styles.md) " oder " [**SB \_ AUTO3STATE**](button-styles.md) " aufweist.</span><span class="sxs-lookup"><span data-stu-id="a0d24-130">Applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/>                    |
| <dl> <span data-ttu-id="a0d24-131"><dt>**BST per \_ pushübertragung**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-131"><dt>**BST\_PUSHED**</dt></span></span> </dl>         | <span data-ttu-id="a0d24-132">Die Schaltfläche wird im gedrückten Zustand angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a0d24-132">The button is being shown in the pushed state.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="a0d24-133"><dt>**BST \_ deaktiviert**</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-133"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>      | <span data-ttu-id="a0d24-134">Kein spezieller Zustand.</span><span class="sxs-lookup"><span data-stu-id="a0d24-134">No special state.</span></span> <span data-ttu-id="a0d24-135">Entspricht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a0d24-135">Equivalent to zero.</span></span><br/>                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a0d24-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0d24-136">Requirements</span></span>



| <span data-ttu-id="a0d24-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0d24-137">Requirement</span></span> | <span data-ttu-id="a0d24-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a0d24-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d24-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0d24-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d24-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0d24-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0d24-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0d24-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d24-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0d24-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0d24-143">Header</span><span class="sxs-lookup"><span data-stu-id="a0d24-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0d24-144"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a0d24-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d24-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0d24-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="a0d24-146">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a0d24-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a0d24-147">**BM \_ getcheck**</span><span class="sxs-lookup"><span data-stu-id="a0d24-147">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="a0d24-148">**BM \_ SetState**</span><span class="sxs-lookup"><span data-stu-id="a0d24-148">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





