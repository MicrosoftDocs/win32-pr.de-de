---
title: EM_FINDTEXTW Meldung (RichEdit. h)
description: Findet Unicode-Text in einem Rich-Edit-Steuerelement.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- Windows-Steuerelemente für EM_FINDTEXTW Meldung
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
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742825"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="8210c-104">EM \_ findtextw-Meldung</span><span class="sxs-lookup"><span data-stu-id="8210c-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="8210c-105">Findet Unicode-Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8210c-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8210c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8210c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8210c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8210c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8210c-108">Gibt die Parameter für den Suchvorgang an.</span><span class="sxs-lookup"><span data-stu-id="8210c-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="8210c-109">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8210c-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8210c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8210c-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="8210c-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8210c-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="8210c-112"><dt>**Fr \_ nach unten**</dt></span><span class="sxs-lookup"><span data-stu-id="8210c-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="8210c-113">Wenn festgelegt, sucht der Vorgang vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="8210c-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="8210c-114">Wenn nicht festgelegt, wird der Vorgang vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments durchsucht.</span><span class="sxs-lookup"><span data-stu-id="8210c-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="8210c-115"><dt>**Fr \_ MatchAlefHamza**</dt></span><span class="sxs-lookup"><span data-stu-id="8210c-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="8210c-116">In der Standardeinstellung werden alle arabischen und hebräischen Alefs mit unterschiedlichen Akzenten mit dem Alef-Zeichen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8210c-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="8210c-117">Legen Sie dieses Flag fest, wenn Sie möchten, dass die Suche zwischen Alefs und unterschiedlichen Akzenten unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="8210c-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="8210c-118"><dt>**Fr \_ MatchCase**</dt></span><span class="sxs-lookup"><span data-stu-id="8210c-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="8210c-119">Wenn festgelegt, wird bei der Suche die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="8210c-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="8210c-120">Wenn nicht festgelegt, wird bei der Suche die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8210c-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="8210c-121"><dt>**Fr \_ matchdiac**</dt></span><span class="sxs-lookup"><span data-stu-id="8210c-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="8210c-122">Standardmäßig werden die diakritischen Zeichen Arabisch und Hebräisch ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8210c-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="8210c-123">Legen Sie dieses Flag fest, wenn Sie möchten, dass der Suchvorgang diakritische Zeichen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="8210c-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="8210c-124"><dt>**Fr \_ MatchKashida**</dt></span><span class="sxs-lookup"><span data-stu-id="8210c-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="8210c-125">Standardmäßig werden arabische und hebräische Kashidas ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8210c-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="8210c-126">Legen Sie dieses Flag fest, wenn der Suchvorgang Kashidas berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="8210c-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="8210c-127"><dt>**"# \_ wholeword"**</dt></span><span class="sxs-lookup"><span data-stu-id="8210c-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="8210c-128">Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8210c-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="8210c-129">Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8210c-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="8210c-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8210c-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8210c-131">Eine [**findtextw**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, die Informationen über den Suchvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="8210c-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8210c-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8210c-132">Return value</span></span>

<span data-ttu-id="8210c-133">Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="8210c-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="8210c-134">Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.</span><span class="sxs-lookup"><span data-stu-id="8210c-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="8210c-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8210c-135">Remarks</span></span>

<span data-ttu-id="8210c-136">**EM \_ Findtextw** verwendet die [**findtextw**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, während [**EM \_ findtextexw**](em-findtextexw.md) die [**findtextexw**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="8210c-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="8210c-137">Der Unterschied besteht darin, dass **findtextexw** den Textbereich zurückgibt, der gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="8210c-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="8210c-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8210c-138">Requirements</span></span>



| <span data-ttu-id="8210c-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8210c-139">Requirement</span></span> | <span data-ttu-id="8210c-140">Wert</span><span class="sxs-lookup"><span data-stu-id="8210c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8210c-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8210c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8210c-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8210c-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8210c-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8210c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8210c-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8210c-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8210c-145">Header</span><span class="sxs-lookup"><span data-stu-id="8210c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8210c-146"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8210c-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8210c-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8210c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8210c-148">**EM \_ findtextexw**</span><span class="sxs-lookup"><span data-stu-id="8210c-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





