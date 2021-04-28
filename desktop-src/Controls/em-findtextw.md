---
title: EM_FINDTEXTW (Richedit.h)
description: 'EM_FINDTEXTW Meldung: Sucht Unicode-Text in einem Rich-Edit-Steuerelement.'
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109798"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="0afef-104">EM \_ FINDTEXTW-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0afef-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="0afef-105">Sucht Unicode-Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0afef-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0afef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0afef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0afef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0afef-108">Gibt die Parameter des Suchvorgang an.</span><span class="sxs-lookup"><span data-stu-id="0afef-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="0afef-109">Dieser Parameter kann einen oder mehrere der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="0afef-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0afef-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0afef-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="0afef-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0afef-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="0afef-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="0afef-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="0afef-113">Wenn festgelegt, durchsucht der Vorgang vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0afef-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="0afef-114">Wenn nicht festgelegt, durchsucht der Vorgang vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="0afef-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="0afef-115"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="0afef-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="0afef-116">Standardmäßig werden arabische und hebräische Alefs mit unterschiedlichen Akzenten durch das Alef-Zeichen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0afef-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="0afef-117">Legen Sie dieses Flag fest, wenn bei der Suche zwischen Alefs mit unterschiedlichen Akzenten unterschieden werden soll.</span><span class="sxs-lookup"><span data-stu-id="0afef-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="0afef-118"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="0afef-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="0afef-119">Wenn festgelegt, wird beim Suchvorgang die Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="0afef-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="0afef-120">Wenn dies nicht festgelegt ist, wird beim Suchvorgang die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0afef-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="0afef-121"><dt>**FR \_ MATCHDMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="0afef-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="0afef-122">Standardmäßig werden arabische und hebräische diakritische Markierungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0afef-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="0afef-123">Legen Sie dieses Flag fest, wenn der Suchvorgang diakritische Markierungen berücksichtigen soll.</span><span class="sxs-lookup"><span data-stu-id="0afef-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="0afef-124"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="0afef-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="0afef-125">Standardmäßig werden arabische und hebräische Kashdas ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0afef-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="0afef-126">Legen Sie dieses Flag fest, wenn der Suchvorgang Kashdas berücksichtigen soll.</span><span class="sxs-lookup"><span data-stu-id="0afef-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="0afef-127"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="0afef-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="0afef-128">Wenn diese Einstellung festgelegt ist, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0afef-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="0afef-129">Wenn diese Einstellung nicht festgelegt ist, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0afef-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="0afef-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0afef-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0afef-131">Eine [**FINDTEXTW-Struktur,**](/windows/win32/api/richedit/ns-richedit-findtexta) die Informationen zum Suchvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="0afef-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afef-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0afef-132">Return value</span></span>

<span data-ttu-id="0afef-133">Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="0afef-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="0afef-134">Wenn das Ziel nicht gefunden wird, lautet der Rückgabewert -1.</span><span class="sxs-lookup"><span data-stu-id="0afef-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="0afef-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0afef-135">Remarks</span></span>

<span data-ttu-id="0afef-136">**EM \_ FINDTEXTW** verwendet die [**FINDTEXTW-Struktur,**](/windows/win32/api/richedit/ns-richedit-findtexta) [**während EM \_ FINDTEXTEXW**](em-findtextexw.md) die [**FINDTEXTEXW-Struktur**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0afef-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="0afef-137">Der Unterschied besteht darin, dass **FINDTEXTEXW** den gefundenen Textbereich zurückmeldet.</span><span class="sxs-lookup"><span data-stu-id="0afef-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="0afef-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0afef-138">Requirements</span></span>



| <span data-ttu-id="0afef-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0afef-139">Requirement</span></span> | <span data-ttu-id="0afef-140">Wert</span><span class="sxs-lookup"><span data-stu-id="0afef-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0afef-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0afef-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0afef-142">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0afef-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0afef-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0afef-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0afef-144">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0afef-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0afef-145">Header</span><span class="sxs-lookup"><span data-stu-id="0afef-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0afef-146"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="0afef-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0afef-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0afef-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afef-148">**EM \_ FINDTEXTEXW**</span><span class="sxs-lookup"><span data-stu-id="0afef-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





