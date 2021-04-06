---
title: EM_GETTEXTLENGTHEX Meldung (RichEdit. h)
description: Berechnet die Textlänge auf verschiedene Weise. Sie wird in der Regel vor dem Erstellen eines Puffers aufgerufen, um den Text aus dem Steuerelement zu empfangen.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Windows-Steuerelemente für EM_GETTEXTLENGTHEX Meldung
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858848"
---
# <a name="em_gettextlengthex-message"></a><span data-ttu-id="2b76a-105">EM \_ gettextverlänex-Meldung</span><span class="sxs-lookup"><span data-stu-id="2b76a-105">EM\_GETTEXTLENGTHEX message</span></span>

<span data-ttu-id="2b76a-106">Berechnet die Textlänge auf verschiedene Weise.</span><span class="sxs-lookup"><span data-stu-id="2b76a-106">Calculates text length in various ways.</span></span> <span data-ttu-id="2b76a-107">Sie wird in der Regel vor dem Erstellen eines Puffers aufgerufen, um den Text aus dem Steuerelement zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2b76a-107">It is usually called before creating a buffer to receive the text from the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b76a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b76a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b76a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b76a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b76a-110">Zeiger auf eine [**gettextverlänex**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) -Struktur, die die Textlängen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="2b76a-110">Pointer to a [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure that receives the text length information.</span></span>

</dd> <dt>

<span data-ttu-id="2b76a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b76a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b76a-112">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2b76a-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b76a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b76a-113">Return value</span></span>

<span data-ttu-id="2b76a-114">Die Meldung gibt die Anzahl von **TCHAR** s im Bearbeitungs Steuerelement zurück, abhängig von der Einstellung der Flags in der [**gettextverlänex**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2b76a-114">The message returns the number of **TCHAR** s in the edit control, depending on the setting of the flags in the [**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) structure.</span></span> <span data-ttu-id="2b76a-115">Wenn inkompatible Flags im **Flags** -Member festgelegt wurden, gibt die Nachricht E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="2b76a-115">If incompatible flags were set in the **flags** member, the message returns E\_INVALIDARG .</span></span>

## <a name="remarks"></a><span data-ttu-id="2b76a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b76a-116">Remarks</span></span>

<span data-ttu-id="2b76a-117">Diese Meldung ist eine schnelle und einfache Möglichkeit, die Anzahl der Zeichen in der Unicode-Version des Rich Edit-Steuer Elements zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2b76a-117">This message is a fast and easy way to determine the number of characters in the Unicode version of the rich edit control.</span></span> <span data-ttu-id="2b76a-118">Für eine nicht-Unicode-Ziel Codepage können Sie jedoch möglicherweise in eine Kombination aus Einzel Byte-und Doppelbyte Zeichen wandeln.</span><span class="sxs-lookup"><span data-stu-id="2b76a-118">However, for a non-Unicode target code page you will potentially be converting to a combination of single-byte and double-byte characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b76a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b76a-119">Requirements</span></span>



| <span data-ttu-id="2b76a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b76a-120">Requirement</span></span> | <span data-ttu-id="2b76a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2b76a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b76a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b76a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b76a-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b76a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b76a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b76a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b76a-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b76a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b76a-126">Header</span><span class="sxs-lookup"><span data-stu-id="2b76a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b76a-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b76a-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b76a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b76a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b76a-129">**Gettextverlänex**</span><span class="sxs-lookup"><span data-stu-id="2b76a-129">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





