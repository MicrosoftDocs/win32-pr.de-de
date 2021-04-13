---
title: EM_GETLINECOUNT Meldung (Winuser. h)
description: Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Windows-Steuerelemente für EM_GETLINECOUNT Meldung
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475570"
---
# <a name="em_getlinecount-message-winuserh"></a><span data-ttu-id="978d2-105">EM_GETLINECOUNT Meldung (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="978d2-105">EM_GETLINECOUNT message (Winuser.h)</span></span>

<span data-ttu-id="978d2-106">Ruft die Anzahl der Zeilen in einem mehrzeiligen Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="978d2-106">Gets the number of lines in a multiline edit control.</span></span> <span data-ttu-id="978d2-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="978d2-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="978d2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="978d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978d2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="978d2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="978d2-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="978d2-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="978d2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="978d2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="978d2-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="978d2-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978d2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="978d2-113">Return value</span></span>

<span data-ttu-id="978d2-114">Der Rückgabewert ist eine ganze Zahl, die die Gesamtzahl der Textzeilen im mehrzeiligen Bearbeitungs Steuerelement oder im Rich Edit-Steuerelement angibt.</span><span class="sxs-lookup"><span data-stu-id="978d2-114">The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control.</span></span> <span data-ttu-id="978d2-115">Wenn das Steuerelement keinen Text hat, ist der Rückgabewert 1.</span><span class="sxs-lookup"><span data-stu-id="978d2-115">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="978d2-116">Der Rückgabewert ist nie kleiner als 1.</span><span class="sxs-lookup"><span data-stu-id="978d2-116">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="978d2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="978d2-117">Remarks</span></span>

<span data-ttu-id="978d2-118">Die **EM \_ getLineCount** -Nachricht Ruft die Gesamtanzahl von Textzeilen ab, nicht nur die Anzahl der Zeilen, die zurzeit sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="978d2-118">The **EM\_GETLINECOUNT** message retrieves the total number of text lines, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="978d2-119">Wenn die Funktion "WordWrap" aktiviert ist, kann sich die Anzahl der Zeilen ändern, wenn sich die Abmessungen des Bearbeitungsfensters ändern.</span><span class="sxs-lookup"><span data-stu-id="978d2-119">If the Wordwrap feature is enabled, the number of lines can change when the dimensions of the editing window change.</span></span>

<span data-ttu-id="978d2-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="978d2-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="978d2-121">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="978d2-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="978d2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="978d2-122">Requirements</span></span>



| <span data-ttu-id="978d2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="978d2-123">Requirement</span></span> | <span data-ttu-id="978d2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="978d2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="978d2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="978d2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="978d2-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="978d2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="978d2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="978d2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="978d2-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="978d2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="978d2-129">Header</span><span class="sxs-lookup"><span data-stu-id="978d2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="978d2-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="978d2-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="978d2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="978d2-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="978d2-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="978d2-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="978d2-133">**EM \_ getline**</span><span class="sxs-lookup"><span data-stu-id="978d2-133">**EM\_GETLINE**</span></span>](em-getline.md)
</dt> <dt>

[<span data-ttu-id="978d2-134">**EM- \_ LineLength**</span><span class="sxs-lookup"><span data-stu-id="978d2-134">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="978d2-135">**\_GetLineCount bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="978d2-135">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





