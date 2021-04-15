---
title: EM_SETTEXTEX Meldung (RichEdit. h)
description: Kombiniert die Funktionalität der WM- \_ Meldungen "SetText" und "em \_ replacesel" und bietet die Möglichkeit, Text mithilfe einer Codepage festzulegen und entweder Rich-Text oder nur-Text zu verwenden.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- Windows-Steuerelemente für EM_SETTEXTEX Meldung
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477310"
---
# <a name="em_settextex-message"></a><span data-ttu-id="f0c06-104">EM \_ settextex-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f0c06-104">EM\_SETTEXTEX message</span></span>

<span data-ttu-id="f0c06-105">Kombiniert die Funktionalität der WM-Meldungen " [**\_ SetText**](/windows/desktop/winmsg/wm-settext) " und " [**EM \_ replacesel**](em-replacesel.md) " und bietet die Möglichkeit, Text mithilfe einer Codepage festzulegen und entweder Rich-Text oder nur-Text zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0c06-105">Combines the functionality of the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) and [**EM\_REPLACESEL**](em-replacesel.md) messages, and adds the ability to set text using a code page and to use either rich text or plain text.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0c06-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0c06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c06-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0c06-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c06-108">Ein Zeiger auf eine [**settextex**](/windows/desktop/api/Richedit/ns-richedit-settextex) -Struktur, die Flags und eine optionale Codepage angibt, die bei der Übersetzung in Unicode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0c06-108">Pointer to a [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) structure that specifies flags and an optional code page to use in translating to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="f0c06-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0c06-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c06-110">Ein Zeiger auf den einzufügenden null-terminierten Text.</span><span class="sxs-lookup"><span data-stu-id="f0c06-110">Pointer to the null-terminated text to insert.</span></span> <span data-ttu-id="f0c06-111">Dieser Text ist eine ANSI-Zeichenfolge, es sei denn, die Codepage ist 1200 (Unicode).</span><span class="sxs-lookup"><span data-stu-id="f0c06-111">This text is an ANSI string, unless the code page is 1200 (Unicode).</span></span> <span data-ttu-id="f0c06-112">Wenn *LPARAM* mit einer gültigen RTF-ASCII-Sequenz beginnt, z. b. "{ \\ RTF" oder "{urtf", wird der Text mit dem RTF-Reader gelesen.</span><span class="sxs-lookup"><span data-stu-id="f0c06-112">If *lParam* starts with a valid RTF ASCII sequence for example, "{\\rtf" or "{urtf" the text is read in using the RTF reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c06-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0c06-113">Return value</span></span>

<span data-ttu-id="f0c06-114">Wenn der Vorgang den gesamten Text festlegt und erfolgreich ist, lautet der Rückgabewert 1.</span><span class="sxs-lookup"><span data-stu-id="f0c06-114">If the operation is setting all of the text and succeeds, the return value is 1.</span></span>

<span data-ttu-id="f0c06-115">Wenn der Vorgang die Auswahl festlegt und erfolgreich ist, ist der Rückgabewert die Anzahl der kopierten Bytes oder Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f0c06-115">If the operation is setting the selection and succeeds, the return value is the number of bytes or characters copied.</span></span>

<span data-ttu-id="f0c06-116">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f0c06-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c06-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0c06-117">Requirements</span></span>



| <span data-ttu-id="f0c06-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0c06-118">Requirement</span></span> | <span data-ttu-id="f0c06-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f0c06-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c06-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0c06-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c06-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0c06-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0c06-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0c06-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c06-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0c06-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0c06-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="f0c06-124">Redistributable</span></span><br/>          | <span data-ttu-id="f0c06-125">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="f0c06-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="f0c06-126">Header</span><span class="sxs-lookup"><span data-stu-id="f0c06-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0c06-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c06-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c06-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0c06-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0c06-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f0c06-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f0c06-130">**EM \_ gettextex**</span><span class="sxs-lookup"><span data-stu-id="f0c06-130">**EM\_GETTEXTEX**</span></span>](em-gettextex.md)
</dt> <dt>

[<span data-ttu-id="f0c06-131">**Settextex**</span><span class="sxs-lookup"><span data-stu-id="f0c06-131">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

