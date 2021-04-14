---
title: EM_SETPASSWORDCHAR Meldung (Winuser. h)
description: Legt das Kenn Wort Zeichen für ein Bearbeitungs Steuerelement fest oder entfernt dieses. Wenn ein Kenn Wort Zeichen festgelegt ist, wird dieses Zeichen anstelle der vom Benutzer eingegebenen Zeichen angezeigt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- Windows-Steuerelemente für EM_SETPASSWORDCHAR Meldung
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476335"
---
# <a name="em_setpasswordchar-message"></a><span data-ttu-id="64101-106">EM \_ setpasswordchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="64101-106">EM\_SETPASSWORDCHAR message</span></span>

<span data-ttu-id="64101-107">Legt das Kenn Wort Zeichen für ein Bearbeitungs Steuerelement fest oder entfernt dieses.</span><span class="sxs-lookup"><span data-stu-id="64101-107">Sets or removes the password character for an edit control.</span></span> <span data-ttu-id="64101-108">Wenn ein Kenn Wort Zeichen festgelegt ist, wird dieses Zeichen anstelle der vom Benutzer eingegebenen Zeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="64101-108">When a password character is set, that character is displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="64101-109">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="64101-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="64101-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64101-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64101-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64101-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64101-112">Das Zeichen, das anstelle der vom Benutzer eingegebenen Zeichen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64101-112">The character to be displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="64101-113">Wenn dieser Parameter NULL ist, entfernt das Steuerelement das aktuelle Kenn Wort Zeichen und zeigt die vom Benutzer eingegebenen Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="64101-113">If this parameter is zero, the control removes the current password character and displays the characters typed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="64101-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64101-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64101-115">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="64101-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64101-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64101-116">Return value</span></span>

<span data-ttu-id="64101-117">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="64101-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64101-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64101-118">Remarks</span></span>

<span data-ttu-id="64101-119">Wenn ein Bearbeitungs Steuerelement die **EM \_ setpasswordchar** -Nachricht empfängt, zeichnet das Steuerelement alle sichtbaren Zeichen mithilfe des vom *wParam* -Parameter angegebenen Zeichens neu.</span><span class="sxs-lookup"><span data-stu-id="64101-119">When an edit control receives the **EM\_SETPASSWORDCHAR** message, the control redraws all visible characters using the character specified by the *wParam* parameter.</span></span> <span data-ttu-id="64101-120">Wenn *wParam* gleich 0 (null) ist, zeichnet das Steuerelement alle sichtbaren Zeichen mithilfe der Zeichen, die vom Benutzer eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="64101-120">If *wParam* is zero, the control redraws all visible characters using the characters typed by the user.</span></span>

<span data-ttu-id="64101-121">Wenn ein Bearbeitungs Steuerelement mit dem es-Kenn [**\_ Wort**](edit-control-styles.md) Stil erstellt wird, wird das standardmäßige Kenn Wort Zeichen auf ein Sternchen () festgelegt \* .</span><span class="sxs-lookup"><span data-stu-id="64101-121">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="64101-122">Wenn ein Bearbeitungs Steuerelement ohne den es-Kenn **\_ Wort** Stil erstellt wird, gibt es kein Kenn Wort Zeichen.</span><span class="sxs-lookup"><span data-stu-id="64101-122">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="64101-123">Der **es \_** -Kenn Wort Stil wird entfernt, wenn eine **EM \_ setpasswordchar** -Nachricht mit dem *wParam* -Parameter auf 0 (null) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="64101-123">The **ES\_PASSWORD** style is removed if an **EM\_SETPASSWORDCHAR** message is sent with the *wParam* parameter set to zero.</span></span>

<span data-ttu-id="64101-124">Steuer **Elemente bearbeiten:** Mehrzeilige Bearbeitungs Steuerelemente unterstützen das Kenn Wort Format oder die Nachrichten nicht.</span><span class="sxs-lookup"><span data-stu-id="64101-124">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="64101-125">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 2,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64101-125">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="64101-126">Sowohl einzeilige als auch mehrzeilige Bearbeitungs Steuerelemente unterstützen den Kenn Wort Stil und die Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="64101-126">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="64101-127">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="64101-127">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64101-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64101-128">Requirements</span></span>



| <span data-ttu-id="64101-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64101-129">Requirement</span></span> | <span data-ttu-id="64101-130">Wert</span><span class="sxs-lookup"><span data-stu-id="64101-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64101-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64101-131">Minimum supported client</span></span><br/> | <span data-ttu-id="64101-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64101-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64101-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64101-133">Minimum supported server</span></span><br/> | <span data-ttu-id="64101-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64101-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64101-135">Header</span><span class="sxs-lookup"><span data-stu-id="64101-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="64101-136"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="64101-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64101-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64101-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64101-138">**EM \_ getpasswordchar**</span><span class="sxs-lookup"><span data-stu-id="64101-138">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
</dt> </dl>

 

 





