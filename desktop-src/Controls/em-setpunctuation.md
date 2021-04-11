---
title: EM_SETPUNCTUATION Meldung (RichEdit. h)
description: Legt die Interpunktions Zeichen für ein Rich-Edit-Steuerelement fest.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- Windows-Steuerelemente für EM_SETPUNCTUATION Meldung
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105567"
---
# <a name="em_setpunctuation-message"></a><span data-ttu-id="69078-104">EM- \_ setinterpunktions-Nachricht</span><span class="sxs-lookup"><span data-stu-id="69078-104">EM\_SETPUNCTUATION message</span></span>

<span data-ttu-id="69078-105">Legt die Interpunktions Zeichen für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="69078-105">Sets the punctuation characters for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="69078-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="69078-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="69078-107">Sie wird in späteren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="69078-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="69078-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69078-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69078-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69078-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69078-110">Gibt den Interpunktions Typ an, bei dem es sich um einen der folgenden Werte handeln kann.</span><span class="sxs-lookup"><span data-stu-id="69078-110">Specifies the punctuation type, which can be one of the following values.</span></span>



| <span data-ttu-id="69078-111">Wert</span><span class="sxs-lookup"><span data-stu-id="69078-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="69078-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="69078-112">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="69078-113"><dt>**PC- \_ führend**</dt></span><span class="sxs-lookup"><span data-stu-id="69078-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="69078-114">Führende Interpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="69078-114">Leading punctuation characters.</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="69078-115"><dt>**PC \_ nach**</dt></span><span class="sxs-lookup"><span data-stu-id="69078-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="69078-116">Die folgenden Interpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="69078-116">Following punctuation characters.</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="69078-117"><dt>**PC- \_ Trennzeichen**</dt></span><span class="sxs-lookup"><span data-stu-id="69078-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="69078-118">Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="69078-118">Delimiter.</span></span><br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <span data-ttu-id="69078-119"><dt>**PC \_ Überlauf**</dt></span><span class="sxs-lookup"><span data-stu-id="69078-119"><dt>**PC\_OVERFLOW** </dt></span></span> </dl> | <span data-ttu-id="69078-120">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="69078-120">Not supported.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="69078-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69078-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69078-122">Zeiger auf eine [**Interpunktions**](/windows/desktop/api/Richedit/ns-richedit-punctuation) Struktur, die die Interpunktions Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="69078-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that contains the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69078-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69078-123">Return value</span></span>

<span data-ttu-id="69078-124">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="69078-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="69078-125">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="69078-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="69078-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69078-126">Requirements</span></span>



| <span data-ttu-id="69078-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69078-127">Requirement</span></span> | <span data-ttu-id="69078-128">Wert</span><span class="sxs-lookup"><span data-stu-id="69078-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69078-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69078-129">Minimum supported client</span></span><br/> | <span data-ttu-id="69078-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69078-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69078-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69078-131">Minimum supported server</span></span><br/> | <span data-ttu-id="69078-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69078-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69078-133">Header</span><span class="sxs-lookup"><span data-stu-id="69078-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="69078-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="69078-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69078-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69078-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="69078-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="69078-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69078-137">**EM- \_ Zeichensatz**</span><span class="sxs-lookup"><span data-stu-id="69078-137">**EM\_GETPUNCTUATION**</span></span>](em-getpunctuation.md)
</dt> <dt>

[<span data-ttu-id="69078-138">**Interpunktions**</span><span class="sxs-lookup"><span data-stu-id="69078-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





