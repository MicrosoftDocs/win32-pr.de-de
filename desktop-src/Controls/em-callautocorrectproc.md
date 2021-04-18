---
title: EM_CALLAUTOCORRECTPROC Meldung (RichEdit. h)
description: Ruft die AutoKorrektur-Rückruffunktion auf, die von der EM-Nachricht "* \_ taudecorrectproc" gespeichert wird, vorausgesetzt, dass der Text vor der Einfügemarke ein Kandidat für die automatische Korrektur ist.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- Windows-Steuerelemente für EM_CALLAUTOCORRECTPROC Meldung
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477625"
---
# <a name="em_callautocorrectproc-message"></a><span data-ttu-id="32aed-104">EM \_ callautocorrectproc-Meldung</span><span class="sxs-lookup"><span data-stu-id="32aed-104">EM\_CALLAUTOCORRECTPROC message</span></span>

<span data-ttu-id="32aed-105">Ruft die AutoKorrektur-Rückruffunktion auf, die von der EM-Nachricht "\* [**\_ taudecorrectproc**](em-setautocorrectproc.md) " gespeichert wird, vorausgesetzt, dass der Text vor der Einfügemarke ein Kandidat für die automatische Korrektur ist.</span><span class="sxs-lookup"><span data-stu-id="32aed-105">Calls the autocorrect callback function that is stored by the [**EM\_SETAUTOCORRECTPROC**](em-setautocorrectproc.md) message, provided that the text preceding the insertion point is a candidate for autocorrection.</span></span>


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a><span data-ttu-id="32aed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="32aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32aed-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32aed-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32aed-108">Ein Zeichen vom Typ **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="32aed-108">A character of type **WCHAR**.</span></span> <span data-ttu-id="32aed-109">Wenn dieses Zeichen ein Tabulator Zeichen (U + 0009) ist und das Zeichen, das der Einfügemarke vorangestellt ist, ein Tabulator ist, wird das vor der Einfügemarke vorangehende Zeichen als Teil der AutoKorrektur Candidate-Zeichenfolge und nicht als Zeichen folgen Trennzeichen behandelt. Andernfalls hat *wParam* keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="32aed-109">If this character is a tab (U+0009), and the character preceding the insertion point isn t a tab, then the character preceding the insertion point is treated as part of the autocorrect candidate string instead of as a string delimiter; otherwise, *wParam* has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="32aed-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32aed-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32aed-111">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="32aed-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32aed-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32aed-112">Return value</span></span>

<span data-ttu-id="32aed-113">Der Rückgabewert ist 0 (null), wenn die Nachricht erfolgreich ist, oder ungleich NULL, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="32aed-113">The return value is zero if the message succeeds, or nonzero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="32aed-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32aed-114">Requirements</span></span>



| <span data-ttu-id="32aed-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32aed-115">Requirement</span></span> | <span data-ttu-id="32aed-116">Wert</span><span class="sxs-lookup"><span data-stu-id="32aed-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32aed-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32aed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32aed-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32aed-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="32aed-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32aed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32aed-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32aed-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32aed-121">Header</span><span class="sxs-lookup"><span data-stu-id="32aed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32aed-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="32aed-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32aed-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32aed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32aed-124">*Autocorrectproc*</span><span class="sxs-lookup"><span data-stu-id="32aed-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="32aed-125">**EM \_ getautocorrectproc**</span><span class="sxs-lookup"><span data-stu-id="32aed-125">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="32aed-126">**EM- \_ tautkorrigitproc**</span><span class="sxs-lookup"><span data-stu-id="32aed-126">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





