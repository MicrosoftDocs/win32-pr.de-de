---
title: EM_FINDTEXTEX Meldung (RichEdit. h)
description: Sucht Text in einem Rich-Edit-Steuerelement.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- Windows-Steuerelemente für EM_FINDTEXTEX Meldung
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e52f7d51ee7a186a8a9e66f11884d6c2e9bca2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104223"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="f4ac2-104">EM \_ FINDTEXTEX-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f4ac2-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="f4ac2-105">Sucht Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4ac2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4ac2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ac2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4ac2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ac2-108">Gibt das Verhalten des Such Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="f4ac2-109">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="f4ac2-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f4ac2-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="f4ac2-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f4ac2-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="f4ac2-112"><dt>**Fr \_ nach unten**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ac2-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="f4ac2-113">Microsoft Rich Edit 2,0 und höher: Wenn diese Einstellung festgelegt ist, wird die Suche von **FINDTEXTEX. chrg. cpmin**; weiterleiten. Wenn nicht festgelegt, wird die Suche rückwärts von **FINDTEXTEX. chrg. cpmin** durchgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="f4ac2-114">Microsoft Rich Edit 1,0: das FR- \_ down-Flag wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="f4ac2-115">Die Suche erfolgt immer weiter.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="f4ac2-116"><dt>**Fr \_ MatchAlefHamza**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ac2-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="f4ac2-117">Microsoft Rich Edit 3,0 und höher: Wenn diese Einstellung festgelegt ist, unterscheidet die Suche zwischen arabischen und hebräischen Alefs mit unterschiedlichen Akzenten.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="f4ac2-118">Wenn nicht festgelegt, werden alle Alefs nur mit dem Alef-Zeichen abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="f4ac2-119"><dt>**Fr \_ MatchCase**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ac2-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="f4ac2-120">Wenn festgelegt, wird bei der Suche die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="f4ac2-121">Wenn nicht festgelegt, wird bei der Suche die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="f4ac2-122"><dt>**Fr \_ matchdiac**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ac2-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="f4ac2-123">Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische und hebräische diakritische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="f4ac2-124">Wenn nicht festgelegt, werden Diakritische Markierungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="f4ac2-125"><dt>**Fr \_ MatchKashida**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ac2-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="f4ac2-126">Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische und hebräische Kashidas.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="f4ac2-127">Wenn nicht festgelegt, werden Kashidas ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="f4ac2-128"><dt>**"# \_ wholeword"**</dt></span><span class="sxs-lookup"><span data-stu-id="f4ac2-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="f4ac2-129">Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="f4ac2-130">Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f4ac2-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4ac2-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4ac2-132">Eine [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, die Informationen über den Suchvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ac2-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4ac2-133">Return value</span></span>

<span data-ttu-id="f4ac2-134">Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="f4ac2-135">Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ac2-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4ac2-136">Remarks</span></span>

<span data-ttu-id="f4ac2-137">Mithilfe dieser Meldung können Sie ANSI-Zeichen folgen suchen.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="f4ac2-138">Verwenden Sie für Unicode den Eintrag [**EM \_ findtextexw**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="f4ac2-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="f4ac2-139">Der **cpmin** -Member von **FINDTEXTEX. chrg** gibt immer den Anfangspunkt der Suche an, und **cpmax** gibt den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="f4ac2-140">Bei der Rückwärtssuche muss **cpmin** größer oder gleich **cpmax** sein.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="f4ac2-141">Bei der Suche wird durch den Wert-1 in **cpmax** der Suchbereich auf das Ende des Texts erweitert.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="f4ac2-142">Wenn bei der Suche eine Übereinstimmung gefunden wird, gibt der **chrgtext** -Member der [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur den Bereich von Zeichen Positionen zurück, der den übereinstimmenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="f4ac2-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ac2-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4ac2-143">Requirements</span></span>



| <span data-ttu-id="f4ac2-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4ac2-144">Requirement</span></span> | <span data-ttu-id="f4ac2-145">Wert</span><span class="sxs-lookup"><span data-stu-id="f4ac2-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ac2-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4ac2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ac2-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4ac2-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4ac2-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4ac2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ac2-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4ac2-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4ac2-150">Header</span><span class="sxs-lookup"><span data-stu-id="f4ac2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4ac2-151"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ac2-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ac2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4ac2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ac2-153">**EM- \_ FindText**</span><span class="sxs-lookup"><span data-stu-id="f4ac2-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





