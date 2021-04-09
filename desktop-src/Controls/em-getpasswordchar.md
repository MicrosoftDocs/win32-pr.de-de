---
title: EM_GETPASSWORDCHAR Meldung (Winuser. h)
description: Ruft das Kenn Wort Zeichen ab, das ein Bearbeitungs Steuerelement anzeigt, wenn der Benutzer Text eingibt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- Windows-Steuerelemente für EM_GETPASSWORDCHAR Meldung
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859175"
---
# <a name="em_getpasswordchar-message"></a><span data-ttu-id="7c990-105">EM \_ getpasswordchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="7c990-105">EM\_GETPASSWORDCHAR message</span></span>

<span data-ttu-id="7c990-106">Ruft das Kenn Wort Zeichen ab, das ein Bearbeitungs Steuerelement anzeigt, wenn der Benutzer Text eingibt.</span><span class="sxs-lookup"><span data-stu-id="7c990-106">Gets the password character that an edit control displays when the user enters text.</span></span> <span data-ttu-id="7c990-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="7c990-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c990-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c990-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c990-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c990-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c990-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7c990-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7c990-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c990-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c990-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7c990-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c990-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c990-113">Return value</span></span>

<span data-ttu-id="7c990-114">Der Rückgabewert gibt das Zeichen an, das anstelle von Zeichen, die vom Benutzer eingegeben werden, angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c990-114">The return value specifies the character to be displayed in place of any characters typed by the user.</span></span> <span data-ttu-id="7c990-115">Wenn der Rückgabewert **null** ist, gibt es kein Kenn Wort Zeichen, und das Steuerelement zeigt die vom Benutzer eingegebenen Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="7c990-115">If the return value is **NULL**, there is no password character, and the control displays the characters typed by the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c990-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c990-116">Remarks</span></span>

<span data-ttu-id="7c990-117">Wenn ein Bearbeitungs Steuerelement mit dem es-Kenn [**\_ Wort**](edit-control-styles.md) Stil erstellt wird, wird das standardmäßige Kenn Wort Zeichen auf ein Sternchen () festgelegt \* .</span><span class="sxs-lookup"><span data-stu-id="7c990-117">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="7c990-118">Wenn ein Bearbeitungs Steuerelement ohne den es-Kenn **\_ Wort** Stil erstellt wird, gibt es kein Kenn Wort Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7c990-118">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="7c990-119">Um das Kenn Wort Zeichen zu ändern, senden Sie die Nachricht [**EM \_ setpasswordchar**](em-setpasswordchar.md) .</span><span class="sxs-lookup"><span data-stu-id="7c990-119">To change the password character, send the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message.</span></span>

<span data-ttu-id="7c990-120">Steuer **Elemente bearbeiten:** Mehrzeilige Bearbeitungs Steuerelemente unterstützen das Kenn Wort Format oder die Nachrichten nicht.</span><span class="sxs-lookup"><span data-stu-id="7c990-120">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="7c990-121">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 2,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7c990-121">**Rich edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="7c990-122">Sowohl einzeilige als auch mehrzeilige Bearbeitungs Steuerelemente unterstützen den Kenn Wort Stil und die Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="7c990-122">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="7c990-123">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="7c990-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c990-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c990-124">Requirements</span></span>



| <span data-ttu-id="7c990-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c990-125">Requirement</span></span> | <span data-ttu-id="7c990-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7c990-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c990-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c990-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7c990-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c990-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c990-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c990-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7c990-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c990-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c990-131">Header</span><span class="sxs-lookup"><span data-stu-id="7c990-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c990-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7c990-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c990-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c990-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c990-134">**EM \_ setpasswordchar**</span><span class="sxs-lookup"><span data-stu-id="7c990-134">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
</dt> </dl>

 

 





