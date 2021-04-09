---
title: EM_GETLIMITTEXT Meldung (Winuser. h)
description: Ruft den aktuellen Text Grenzwert für ein Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- Windows-Steuerelemente für EM_GETLIMITTEXT Meldung
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858688"
---
# <a name="em_getlimittext-message"></a><span data-ttu-id="9642a-105">EM \_ getlimittext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9642a-105">EM\_GETLIMITTEXT message</span></span>

<span data-ttu-id="9642a-106">Ruft den aktuellen Text Grenzwert für ein Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="9642a-106">Gets the current text limit for an edit control.</span></span> <span data-ttu-id="9642a-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="9642a-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9642a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9642a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9642a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9642a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9642a-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9642a-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9642a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9642a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9642a-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9642a-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9642a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9642a-113">Return value</span></span>

<span data-ttu-id="9642a-114">Der Rückgabewert ist das Text Limit.</span><span class="sxs-lookup"><span data-stu-id="9642a-114">The return value is the text limit.</span></span>

## <a name="remarks"></a><span data-ttu-id="9642a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9642a-115">Remarks</span></span>

<span data-ttu-id="9642a-116">**Bearbeitungs Steuerelemente, umfassende Bearbeitung 2,0 und höher:** Das Text Limit ist die maximale Text Menge in **TCHAR** s, die das Steuerelement enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="9642a-116">**Edit controls, Rich Edit 2.0 and later:** The text limit is the maximum amount of text, in **TCHAR** s, that the control can contain.</span></span> <span data-ttu-id="9642a-117">Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9642a-117">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="9642a-118">Zwei Dokumente mit der gleichen Zeichen Beschränkung führen zu demselben Text Limit, auch wenn "ANSI" und das andere "Unicode" sind.</span><span class="sxs-lookup"><span data-stu-id="9642a-118">Two documents with the same character limit will yield the same text limit, even if one is ANSI and the other is Unicode.</span></span>

<span data-ttu-id="9642a-119">**Rich Edit 1,0:** Das Text Limit ist die maximale Menge an Text (in Bytes), die das Rich Edit-Steuerelement enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="9642a-119">**Rich Edit 1.0:** The text limit is the maximum amount of text, in bytes, that the rich edit control can contain.</span></span>

<span data-ttu-id="9642a-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9642a-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9642a-121">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="9642a-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9642a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9642a-122">Requirements</span></span>



| <span data-ttu-id="9642a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9642a-123">Requirement</span></span> | <span data-ttu-id="9642a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9642a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9642a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9642a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9642a-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9642a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9642a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9642a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9642a-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9642a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9642a-129">Header</span><span class="sxs-lookup"><span data-stu-id="9642a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9642a-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9642a-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9642a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9642a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9642a-132">**EM \_ SetLimitText**</span><span class="sxs-lookup"><span data-stu-id="9642a-132">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 





