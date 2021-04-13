---
title: EM_GETFIRSTVISIBLELINE Meldung (Winuser. h)
description: Ruft den NULL basierten Index der obersten sichtbaren Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- Windows-Steuerelemente für EM_GETFIRSTVISIBLELINE Meldung
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518302"
---
# <a name="em_getfirstvisibleline-message"></a><span data-ttu-id="a167e-105">EM \_ getfirstvisibleline-Meldung</span><span class="sxs-lookup"><span data-stu-id="a167e-105">EM\_GETFIRSTVISIBLELINE message</span></span>

<span data-ttu-id="a167e-106">Ruft den NULL basierten Index der obersten sichtbaren Zeile in einem mehrzeiligen Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="a167e-106">Gets the zero-based index of the uppermost visible line in a multiline edit control.</span></span> <span data-ttu-id="a167e-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="a167e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a167e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a167e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a167e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a167e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a167e-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a167e-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a167e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a167e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a167e-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="a167e-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a167e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a167e-113">Return value</span></span>

<span data-ttu-id="a167e-114">Der Rückgabewert ist der null basierte Index der obersten sichtbaren Zeile in einem mehrzeiligen Bearbeitungs Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a167e-114">The return value is the zero-based index of the uppermost visible line in a multiline edit control.</span></span>

<span data-ttu-id="a167e-115">Steuer **Elemente bearbeiten:** Der Rückgabewert für einzeilige Bearbeitungs Steuerelemente ist der null basierte Index des ersten sichtbaren Zeichens.</span><span class="sxs-lookup"><span data-stu-id="a167e-115">**Edit controls:** For single-line edit controls, the return value is the zero-based index of the first visible character.</span></span>

<span data-ttu-id="a167e-116">**Rich Edit-Steuerelemente:** Für einzeilige Rich Edit-Steuerelemente ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a167e-116">**Rich edit controls:** For single-line rich edit controls, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a167e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a167e-117">Remarks</span></span>

<span data-ttu-id="a167e-118">Die Anzahl der Zeilen und die Länge der Zeilen in einem Bearbeitungs Steuerelement hängen von der Breite des Steuer Elements und der aktuellen WordWrap-Einstellung ab.</span><span class="sxs-lookup"><span data-stu-id="a167e-118">The number of lines and the length of the lines in an edit control depend on the width of the control and the current Wordwrap setting.</span></span>

<span data-ttu-id="a167e-119">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a167e-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a167e-120">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="a167e-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a167e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a167e-121">Requirements</span></span>



| <span data-ttu-id="a167e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a167e-122">Requirement</span></span> | <span data-ttu-id="a167e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a167e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a167e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a167e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a167e-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a167e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a167e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a167e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a167e-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a167e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a167e-128">Header</span><span class="sxs-lookup"><span data-stu-id="a167e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a167e-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a167e-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





