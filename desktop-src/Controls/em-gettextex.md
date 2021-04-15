---
title: EM_GETTEXTEX Meldung (RichEdit. h)
description: Ruft den Text aus einem Rich-Edit-Steuerelement ab.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Windows-Steuerelemente für EM_GETTEXTEX Meldung
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476479"
---
# <a name="em_gettextex-message"></a><span data-ttu-id="c10f6-104">EM \_ gettextex-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c10f6-104">EM\_GETTEXTEX message</span></span>

<span data-ttu-id="c10f6-105">Ruft den Text aus einem Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="c10f6-105">Gets the text from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c10f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c10f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c10f6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c10f6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c10f6-108">Zeiger auf eine [**gettextex**](/windows/desktop/api/Richedit/ns-richedit-gettextex) -Struktur, die angibt, wie der Text übersetzt werden soll, bevor er in den Ausgabepuffer versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c10f6-108">Pointer to a [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure, which indicates how to translate the text before putting it into the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c10f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c10f6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c10f6-110">Zeiger auf den Puffer, in den der Text empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c10f6-110">Pointer to the buffer to receive the text.</span></span> <span data-ttu-id="c10f6-111">Die Größe dieses Puffers in Bytes wird vom **CB** -Member der [**gettextex**](/windows/desktop/api/Richedit/ns-richedit-gettextex) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="c10f6-111">The size of this buffer, in bytes, is specified by the **cb** member of the [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure.</span></span> <span data-ttu-id="c10f6-112">Verwenden Sie die Nachricht [**EM \_ gettextverlänex**](em-gettextlengthex.md) , um die erforderliche Größe des Puffers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c10f6-112">Use the [**EM\_GETTEXTLENGTHEX**](em-gettextlengthex.md) message to get the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c10f6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c10f6-113">Return value</span></span>

<span data-ttu-id="c10f6-114">Der Rückgabewert ist die Anzahl von **TCHAR**-s, die in den Ausgabepuffer kopiert werden, einschließlich des NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="c10f6-114">The return value is the number of **TCHAR** s copied into the output buffer, including the null terminator.</span></span>

## <a name="remarks"></a><span data-ttu-id="c10f6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c10f6-115">Remarks</span></span>

<span data-ttu-id="c10f6-116">Wenn die Größe des Ausgabepuffers kleiner ist als die Größe des Texts im-Steuerelement, kopiert das Bearbeitungs Steuerelement Text von seinem Anfang und platziert ihn im Puffer, bis der Puffer voll ist.</span><span class="sxs-lookup"><span data-stu-id="c10f6-116">If the size of the output buffer is less than the size of the text in the control, the edit control will copy text from its beginning and place it in the buffer until the buffer is full.</span></span> <span data-ttu-id="c10f6-117">Ein abschließende Null-Zeichen wird immer noch am Ende des Puffers platziert.</span><span class="sxs-lookup"><span data-stu-id="c10f6-117">A terminating null character will still be placed at the end of the buffer.</span></span>

<span data-ttu-id="c10f6-118">Wenn ANSI-Text angefordert wird, verwendet **EM \_ gettextex** die [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) -Funktion, um die Unicode-Zeichen in ANSI zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="c10f6-118">If ANSI text is requested, **EM\_GETTEXTEX** uses the [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function to translate the Unicode characters to ANSI.</span></span> <span data-ttu-id="c10f6-119">Sie können mit einer bestimmten Codepage von Unicode zu ANSI wechseln.</span><span class="sxs-lookup"><span data-stu-id="c10f6-119">It allows you to go from Unicode to ANSI using a particular code page.</span></span> <span data-ttu-id="c10f6-120">Die [**gettextex**](/windows/desktop/api/Richedit/ns-richedit-gettextex) -Struktur enthält Elemente (**lpdefaultchar** und **lpuseddefchar**), die bei der Übersetzung von Unicode in ANSI verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c10f6-120">The [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure contains members (**lpDefaultChar** and **lpUsedDefChar**) that are used in the translation from Unicode to ANSI.</span></span>

## <a name="requirements"></a><span data-ttu-id="c10f6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c10f6-121">Requirements</span></span>



| <span data-ttu-id="c10f6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c10f6-122">Requirement</span></span> | <span data-ttu-id="c10f6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c10f6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c10f6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c10f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c10f6-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c10f6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c10f6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c10f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c10f6-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c10f6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c10f6-128">Header</span><span class="sxs-lookup"><span data-stu-id="c10f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c10f6-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c10f6-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c10f6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c10f6-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="c10f6-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c10f6-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c10f6-132">**EM \_ settextex**</span><span class="sxs-lookup"><span data-stu-id="c10f6-132">**EM\_SETTEXTEX**</span></span>](em-settextex.md)
</dt> <dt>

[<span data-ttu-id="c10f6-133">**Gettextex**</span><span class="sxs-lookup"><span data-stu-id="c10f6-133">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

<span data-ttu-id="c10f6-134">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c10f6-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c10f6-135">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="c10f6-135">**WideCharToMultiByte**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[<span data-ttu-id="c10f6-136">**WM- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="c10f6-136">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

