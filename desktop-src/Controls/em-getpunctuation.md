---
title: EM_GETPUNCTUATION Meldung (RichEdit. h)
description: Ruft die aktuellen Interpunktions Zeichen für das Rich Edit-Steuerelement ab.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Windows-Steuerelemente für EM_GETPUNCTUATION Meldung
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105297"
---
# <a name="em_getpunctuation-message"></a><span data-ttu-id="d0a0c-104">EM \_ getinterinterationmeldung</span><span class="sxs-lookup"><span data-stu-id="d0a0c-104">EM\_GETPUNCTUATION message</span></span>

<span data-ttu-id="d0a0c-105">Ruft die aktuellen Interpunktions Zeichen für das Rich Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="d0a0c-105">Gets the current punctuation characters for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="d0a0c-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0a0c-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="d0a0c-107">Sie wird in höheren Versionen der Rich-Edit-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0a0c-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="d0a0c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a0c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0a0c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a0c-110">Der Interpunktions Typ kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="d0a0c-110">The punctuation type can be one of the following values.</span></span>



| <span data-ttu-id="d0a0c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d0a0c-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="d0a0c-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d0a0c-112">Meaning</span></span>                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="d0a0c-113"><dt>**PC- \_ führend**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a0c-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="d0a0c-114">Führende Interpunktions Zeichen</span><span class="sxs-lookup"><span data-stu-id="d0a0c-114">Leading punctuation characters</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="d0a0c-115"><dt>**PC \_ nach**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a0c-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="d0a0c-116">Die folgenden Interpunktions Zeichen</span><span class="sxs-lookup"><span data-stu-id="d0a0c-116">Following punctuation characters</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="d0a0c-117"><dt>**PC- \_ Trennzeichen**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a0c-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="d0a0c-118">Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="d0a0c-118">Delimiter</span></span><br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <span data-ttu-id="d0a0c-119"><dt>**PC- \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a0c-119"><dt>**PC\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="d0a0c-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d0a0c-120">Not supported</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="d0a0c-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0a0c-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a0c-122">Zeiger auf eine [**Interpunktions**](/windows/desktop/api/Richedit/ns-richedit-punctuation) Struktur, die die Interpunktions Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="d0a0c-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that receives the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a0c-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0a0c-123">Return value</span></span>

<span data-ttu-id="d0a0c-124">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d0a0c-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d0a0c-125">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d0a0c-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a0c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0a0c-126">Requirements</span></span>



| <span data-ttu-id="d0a0c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0a0c-127">Requirement</span></span> | <span data-ttu-id="d0a0c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d0a0c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a0c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0a0c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a0c-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a0c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0a0c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0a0c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a0c-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a0c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0a0c-133">Header</span><span class="sxs-lookup"><span data-stu-id="d0a0c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a0c-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a0c-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a0c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0a0c-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0a0c-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d0a0c-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d0a0c-137">**EM- \_ setinterpunktions Zeichen**</span><span class="sxs-lookup"><span data-stu-id="d0a0c-137">**EM\_SETPUNCTUATION**</span></span>](em-setpunctuation.md)
</dt> <dt>

[<span data-ttu-id="d0a0c-138">**Interpunktions**</span><span class="sxs-lookup"><span data-stu-id="d0a0c-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





