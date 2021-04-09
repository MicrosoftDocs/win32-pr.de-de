---
title: EM_GETMODIFY Meldung (Winuser. h)
description: Ruft den Zustand des änderungsflags eines Bearbeitungs Steuer Elements ab. Das Flag gibt an, ob der Inhalt des Bearbeitungs Steuer Elements geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- Windows-Steuerelemente für EM_GETMODIFY Meldung
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858710"
---
# <a name="em_getmodify-message"></a><span data-ttu-id="2d77e-106">EM \_ getmodify-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2d77e-106">EM\_GETMODIFY message</span></span>

<span data-ttu-id="2d77e-107">Ruft den Zustand des änderungsflags eines Bearbeitungs Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="2d77e-107">Gets the state of an edit control's modification flag.</span></span> <span data-ttu-id="2d77e-108">Das Flag gibt an, ob der Inhalt des Bearbeitungs Steuer Elements geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d77e-108">The flag indicates whether the contents of the edit control have been modified.</span></span> <span data-ttu-id="2d77e-109">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="2d77e-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d77e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d77e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d77e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d77e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d77e-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2d77e-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2d77e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d77e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d77e-114">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="2d77e-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d77e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d77e-115">Return value</span></span>

<span data-ttu-id="2d77e-116">Wenn der Inhalt des Bearbeitungs Steuer Elements geändert wurde, ist der Rückgabewert ungleich 0 (null). Andernfalls ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2d77e-116">If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d77e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d77e-117">Remarks</span></span>

<span data-ttu-id="2d77e-118">Wenn das Steuerelement erstellt wird, löscht das System das Änderungsflag automatisch auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2d77e-118">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="2d77e-119">Wenn der Benutzer den Text des Steuer Elements ändert, legt das System das Flag auf einen Wert ungleich 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="2d77e-119">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="2d77e-120">Sie können die Nachricht [**EM \_ setmodify**](em-setmodify.md) an das Bearbeitungs Steuerelement senden, um das Flag festzulegen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2d77e-120">You can send the [**EM\_SETMODIFY**](em-setmodify.md) message to the edit control to set or clear the flag.</span></span>

<span data-ttu-id="2d77e-121">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d77e-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2d77e-122">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="2d77e-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d77e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d77e-123">Requirements</span></span>



| <span data-ttu-id="2d77e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d77e-124">Requirement</span></span> | <span data-ttu-id="2d77e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2d77e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d77e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d77e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2d77e-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d77e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2d77e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d77e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2d77e-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d77e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2d77e-130">Header</span><span class="sxs-lookup"><span data-stu-id="2d77e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d77e-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2d77e-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d77e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d77e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d77e-133">**EM \_ setmodify**</span><span class="sxs-lookup"><span data-stu-id="2d77e-133">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
</dt> </dl>

 

 





