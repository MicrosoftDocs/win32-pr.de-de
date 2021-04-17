---
title: CB_SETEXTENDEDUI Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ setextendedui-Nachricht, um entweder die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche für ein Kombinations Feld mit dem Format CBS \_ Dropdown oder CBS \_ DropDownList auszuwählen.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- Windows-Steuerelemente für CB_SETEXTENDEDUI Meldung
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476635"
---
# <a name="cb_setextendedui-message"></a><span data-ttu-id="79f4c-104">CB- \_ messagetendedui-Nachricht</span><span class="sxs-lookup"><span data-stu-id="79f4c-104">CB\_SETEXTENDEDUI message</span></span>

<span data-ttu-id="79f4c-105">Eine Anwendung sendet eine **CB \_ setextendedui** -Nachricht, um entweder die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche für ein Kombinations Feld mit dem Format [**CBS \_ Dropdown**](combo-box-styles.md) oder [**CBS \_ DropDownList**](combo-box-styles.md) auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="79f4c-105">An application sends a **CB\_SETEXTENDEDUI** message to select either the default UI or the extended UI for a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="79f4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79f4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f4c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79f4c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79f4c-108">Ein **boolescher** Wert, der angibt, ob für das Kombinations Feld die erweiterte Benutzeroberfläche (**true**) oder die Standardbenutzer Oberfläche (**false**) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79f4c-108">A **BOOL** that specifies whether the combo box uses the extended UI (**TRUE**) or the default UI (**FALSE**).</span></span>

</dd> <dt>

<span data-ttu-id="79f4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79f4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79f4c-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="79f4c-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f4c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79f4c-111">Return value</span></span>

<span data-ttu-id="79f4c-112">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert CB \_ okay.</span><span class="sxs-lookup"><span data-stu-id="79f4c-112">If the operation succeeds, the return value is CB\_OKAY.</span></span> <span data-ttu-id="79f4c-113">Wenn ein Fehler auftritt, ist es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="79f4c-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="79f4c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79f4c-114">Remarks</span></span>

<span data-ttu-id="79f4c-115">Standardmäßig wird die Liste mit dem F4-Schlüssel geöffnet oder geschlossen, und der nach-unten-Pfeil ändert die aktuelle Auswahl.</span><span class="sxs-lookup"><span data-stu-id="79f4c-115">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="79f4c-116">In der erweiterten Benutzeroberfläche ist die F4-Taste deaktiviert, und die nach-unten-Taste öffnet die Dropdown Liste.</span><span class="sxs-lookup"><span data-stu-id="79f4c-116">In the extended UI, the F4 key is disabled and the DOWN ARROW key opens the drop-down list.</span></span> <span data-ttu-id="79f4c-117">Das Mausrad, das normalerweise durch die Elemente in der Liste führt, hat keine Auswirkung, wenn die erweiterte Benutzeroberfläche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79f4c-117">The mouse wheel, which normally scrolls through the items in the list, has no effect when the extended UI is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="79f4c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79f4c-118">Requirements</span></span>



| <span data-ttu-id="79f4c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79f4c-119">Requirement</span></span> | <span data-ttu-id="79f4c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="79f4c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79f4c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79f4c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="79f4c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79f4c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="79f4c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79f4c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="79f4c-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79f4c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79f4c-125">Header</span><span class="sxs-lookup"><span data-stu-id="79f4c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="79f4c-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="79f4c-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f4c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79f4c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="79f4c-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="79f4c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="79f4c-129">**CB \_ getextendedui**</span><span class="sxs-lookup"><span data-stu-id="79f4c-129">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
</dt> <dt>

<span data-ttu-id="79f4c-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="79f4c-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="79f4c-131">Kombinations Feld-Features</span><span class="sxs-lookup"><span data-stu-id="79f4c-131">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





