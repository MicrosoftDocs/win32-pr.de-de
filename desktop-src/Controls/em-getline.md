---
title: EM_GETLINE Meldung (Winuser. h)
description: Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement und platziert Sie in einem angegebenen Puffer. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Windows-Steuerelemente für EM_GETLINE Meldung
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949495"
---
# <a name="em_getline-message-winuserh"></a><span data-ttu-id="86637-105">EM_GETLINE Meldung (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="86637-105">EM_GETLINE message (Winuser.h)</span></span>

<span data-ttu-id="86637-106">Kopiert eine Textzeile aus einem Bearbeitungs Steuerelement und platziert Sie in einem angegebenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="86637-106">Copies a line of text from an edit control and places it in a specified buffer.</span></span> <span data-ttu-id="86637-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="86637-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="86637-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="86637-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86637-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86637-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86637-110">Der null basierte Index der Zeile, die aus einem mehrzeiligen Bearbeitungs Steuerelement abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="86637-110">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="86637-111">Der Wert 0 (null) gibt die oberste Zeile an.</span><span class="sxs-lookup"><span data-stu-id="86637-111">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="86637-112">Dieser Parameter wird von einem einzeiligen Bearbeitungs Steuerelement ignoriert.</span><span class="sxs-lookup"><span data-stu-id="86637-112">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="86637-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86637-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86637-114">Ein Zeiger auf den Puffer, der eine Kopie der Zeile empfängt.</span><span class="sxs-lookup"><span data-stu-id="86637-114">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="86637-115">Legen Sie vor dem Senden der Nachricht das erste Wort dieses Puffers auf die Größe des Puffers in **TCHAR** s fest.</span><span class="sxs-lookup"><span data-stu-id="86637-115">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="86637-116">Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="86637-116">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="86637-117">Die Größe im ersten Wort wird von der kopierten Zeile überschrieben.</span><span class="sxs-lookup"><span data-stu-id="86637-117">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86637-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86637-118">Return value</span></span>

<span data-ttu-id="86637-119">Der Rückgabewert ist die Anzahl der kopierten **TCHAR**-s.</span><span class="sxs-lookup"><span data-stu-id="86637-119">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="86637-120">Der Rückgabewert ist 0 (null), wenn die durch den *wParam* -Parameter angegebene Zeilennummer größer als die Anzahl der Zeilen im Bearbeitungs Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="86637-120">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="86637-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86637-121">Remarks</span></span>

<span data-ttu-id="86637-122">Steuer **Elemente bearbeiten:** Die kopierte Zeile enthält kein abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="86637-122">**Edit controls:** The copied line does not contain a terminating null character.</span></span>

<span data-ttu-id="86637-123">**Rich Edit-Steuerelemente:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86637-123">**Rich edit controls:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="86637-124">Die kopierte Zeile enthält kein abschließendes NULL Zeichen, es sei denn, es wurde kein Text kopiert.</span><span class="sxs-lookup"><span data-stu-id="86637-124">The copied line does not contain a terminating null character, unless no text was copied.</span></span> <span data-ttu-id="86637-125">Wenn kein Text kopiert wurde, legt die Nachricht am Anfang des Puffers ein NULL-Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="86637-125">If no text was copied, the message places a null character at the beginning of the buffer.</span></span> <span data-ttu-id="86637-126">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="86637-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86637-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86637-127">Requirements</span></span>



| <span data-ttu-id="86637-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86637-128">Requirement</span></span> | <span data-ttu-id="86637-129">Wert</span><span class="sxs-lookup"><span data-stu-id="86637-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86637-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86637-130">Minimum supported client</span></span><br/> | <span data-ttu-id="86637-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86637-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="86637-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86637-132">Minimum supported server</span></span><br/> | <span data-ttu-id="86637-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86637-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86637-134">Header</span><span class="sxs-lookup"><span data-stu-id="86637-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="86637-135"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="86637-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86637-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86637-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="86637-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="86637-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86637-138">**EM- \_ LineLength**</span><span class="sxs-lookup"><span data-stu-id="86637-138">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="86637-139">**\_Getline bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="86637-139">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

<span data-ttu-id="86637-140">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="86637-140">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="86637-141">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="86637-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

