---
title: EM_FINDTEXTEXW Meldung (RichEdit. h)
description: Findet Unicode-Text in einem Rich-Edit-Steuerelement.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- Windows-Steuerelemente für EM_FINDTEXTEXW Meldung
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957006"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="a227b-104">EM \_ findtextexw-Meldung</span><span class="sxs-lookup"><span data-stu-id="a227b-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="a227b-105">Findet Unicode-Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a227b-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a227b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a227b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a227b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a227b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a227b-108">Gibt das Verhalten des Such Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="a227b-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="a227b-109">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a227b-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a227b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a227b-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="a227b-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a227b-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="a227b-112"><dt>**Fr \_ nach unten**</dt></span><span class="sxs-lookup"><span data-stu-id="a227b-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="a227b-113">Microsoft Rich Edit 2,0 und höher: Wenn diese Einstellung festgelegt ist, wird die Suche von **FINDTEXTEX. chrg. cpmin**; weiterleiten. Wenn nicht festgelegt, wird die Suche rückwärts von **FINDTEXTEX. chrg. cpmin** durchgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a227b-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="a227b-114">Microsoft Rich Edit 1,0: das FR- \_ down-Flag wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a227b-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="a227b-115">Die Suche erfolgt immer weiter.</span><span class="sxs-lookup"><span data-stu-id="a227b-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="a227b-116"><dt>**Fr \_ MatchAlefHamza**</dt></span><span class="sxs-lookup"><span data-stu-id="a227b-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="a227b-117">Wenn festgelegt, unterscheidet die Suche zwischen Alefs und unterschiedlichen Akzenten.</span><span class="sxs-lookup"><span data-stu-id="a227b-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="a227b-118">Wenn diese Einstellung nicht festgelegt ist, werden alle arabischen und hebräischen Alefs mit unterschiedlichen Akzenten mit dem Alef-Zeichen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a227b-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="a227b-119"><dt>**Fr \_ MatchCase**</dt></span><span class="sxs-lookup"><span data-stu-id="a227b-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="a227b-120">Wenn festgelegt, wird bei der Suche die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="a227b-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="a227b-121">Wenn nicht festgelegt, wird bei der Suche die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a227b-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="a227b-122"><dt>**Fr \_ matchdiac**</dt></span><span class="sxs-lookup"><span data-stu-id="a227b-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="a227b-123">Wenn festgelegt, berücksichtigt der Suchvorgang Diakritische Markierungen.</span><span class="sxs-lookup"><span data-stu-id="a227b-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="a227b-124">Wenn nicht festgelegt, werden die diakritischen Zeichen Arabisch und Hebräisch ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a227b-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="a227b-125"><dt>**Fr \_ MatchKashida**</dt></span><span class="sxs-lookup"><span data-stu-id="a227b-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="a227b-126">Wenn festgelegt, berücksichtigt der Suchvorgang Kashidas.</span><span class="sxs-lookup"><span data-stu-id="a227b-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="a227b-127">Wenn nicht festgelegt, werden arabische und hebräische Kashidas ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a227b-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="a227b-128"><dt>**"# \_ wholeword"**</dt></span><span class="sxs-lookup"><span data-stu-id="a227b-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="a227b-129">Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a227b-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="a227b-130">Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a227b-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="a227b-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a227b-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a227b-132">Eine [**findtextexw**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, die Informationen über den Suchvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="a227b-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a227b-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a227b-133">Return value</span></span>

<span data-ttu-id="a227b-134">Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="a227b-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="a227b-135">Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.</span><span class="sxs-lookup"><span data-stu-id="a227b-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a227b-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a227b-136">Remarks</span></span>

<span data-ttu-id="a227b-137">Verwenden Sie diese Meldung, um Unicode-Zeichen folgen zu suchen</span><span class="sxs-lookup"><span data-stu-id="a227b-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="a227b-138">Verwenden Sie für ANSI; [**EM \_ FINDTEXTEX**](em-findtextex.md).</span><span class="sxs-lookup"><span data-stu-id="a227b-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="a227b-139">Der **cpmin** -Member von **FINDTEXTEX. chrg** gibt immer den Anfangspunkt der Suche an, und **cpmax** gibt den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="a227b-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="a227b-140">Bei der Rückwärtssuche muss **cpmin** größer oder gleich **cpmax** sein.</span><span class="sxs-lookup"><span data-stu-id="a227b-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="a227b-141">Bei der Suche wird durch den Wert-1 in **cpmax** der Suchbereich auf das Ende des Texts erweitert.</span><span class="sxs-lookup"><span data-stu-id="a227b-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="a227b-142">Wenn bei der Suche eine Übereinstimmung gefunden wird, gibt der **chrgtext** -Member der [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur den Bereich von Zeichen Positionen zurück, der den übereinstimmenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="a227b-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="a227b-143">**EM \_ Findtextexw** verwendet die [**findtextexw**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, während [**EM \_ findtextw**](em-findtextw.md) die [**findtextw**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="a227b-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="a227b-144">Der Unterschied besteht darin, dass **EM \_ findtextexw** den Textbereich meldet, der gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a227b-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="a227b-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a227b-145">Requirements</span></span>



| <span data-ttu-id="a227b-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a227b-146">Requirement</span></span> | <span data-ttu-id="a227b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="a227b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a227b-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a227b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a227b-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a227b-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a227b-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a227b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a227b-151">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a227b-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a227b-152">Header</span><span class="sxs-lookup"><span data-stu-id="a227b-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a227b-153"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a227b-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a227b-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a227b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a227b-155">**EM \_ findtextw**</span><span class="sxs-lookup"><span data-stu-id="a227b-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





