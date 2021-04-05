---
title: EM_LINELENGTH Meldung (Winuser. h)
description: Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement in Zeichen ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Windows-Steuerelemente für EM_LINELENGTH Meldung
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859130"
---
# <a name="em_linelength-message"></a><span data-ttu-id="6c8de-105">EM- \_ LineLength-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6c8de-105">EM\_LINELENGTH message</span></span>

<span data-ttu-id="6c8de-106">Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement in Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="6c8de-106">Retrieves the length, in characters, of a line in an edit control.</span></span> <span data-ttu-id="6c8de-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="6c8de-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c8de-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c8de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8de-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c8de-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8de-110">Der Zeichen Index eines Zeichens in der Zeile, deren Länge abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c8de-110">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="6c8de-111">Wenn dieser Parameter größer als die Anzahl der Zeichen im-Steuerelement ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6c8de-111">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="6c8de-112">Dieser Parameter kann-1 sein.</span><span class="sxs-lookup"><span data-stu-id="6c8de-112">This parameter can be -1.</span></span> <span data-ttu-id="6c8de-113">In diesem Fall gibt die Nachricht die Anzahl der nicht ausgewählten Zeichen in Zeilen zurück, die ausgewählte Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c8de-113">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="6c8de-114">Wenn die Auswahl z. b. vom vierten Zeichen einer Zeile bis zum achten Zeichen vom Ende der nächsten Zeile aus verlängert wird, wäre der Rückgabewert 10 (drei Zeichen in der ersten Zeile und sieben bei der nächsten Zeile).</span><span class="sxs-lookup"><span data-stu-id="6c8de-114">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="6c8de-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c8de-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8de-116">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c8de-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8de-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c8de-117">Return value</span></span>

<span data-ttu-id="6c8de-118">Für mehrzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge in **TCHAR** s der durch den *wParam* -Parameter angegebenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="6c8de-118">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter.</span></span> <span data-ttu-id="6c8de-119">Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6c8de-119">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="6c8de-120">Das Wagen Rücklauf Zeichen am Ende der Zeile ist nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c8de-120">It does not include the carriage-return character at the end of the line.</span></span>

<span data-ttu-id="6c8de-121">Für einzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge des Texts im Bearbeitungs Steuerelement in **TCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="6c8de-121">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="6c8de-122">Wenn *wParam* größer als die Anzahl der Zeichen im-Steuerelement ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6c8de-122">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8de-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c8de-123">Remarks</span></span>

<span data-ttu-id="6c8de-124">Verwenden Sie die [**EM \_ lineindex**](em-lineindex.md) -Nachricht, um einen Zeichen Index für eine bestimmte Zeilennummer innerhalb eines mehrzeiligen Bearbeitungs Steuer Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6c8de-124">Use the [**EM\_LINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control.</span></span>

<span data-ttu-id="6c8de-125">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c8de-125">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="6c8de-126">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="6c8de-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8de-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c8de-127">Requirements</span></span>



| <span data-ttu-id="6c8de-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c8de-128">Requirement</span></span> | <span data-ttu-id="6c8de-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6c8de-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8de-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c8de-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8de-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c8de-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c8de-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c8de-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8de-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c8de-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c8de-134">Header</span><span class="sxs-lookup"><span data-stu-id="6c8de-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c8de-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6c8de-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8de-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c8de-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8de-137">**EM \_ Linan DEX**</span><span class="sxs-lookup"><span data-stu-id="6c8de-137">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





