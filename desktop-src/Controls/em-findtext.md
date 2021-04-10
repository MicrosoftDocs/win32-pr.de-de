---
title: EM_FINDTEXT Meldung (RichEdit. h)
description: Sucht Text in einem Rich-Edit-Steuerelement.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- Windows-Steuerelemente für EM_FINDTEXT Meldung
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956644"
---
# <a name="em_findtext-message"></a><span data-ttu-id="42d98-104">EM \_ FindText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="42d98-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="42d98-105">Sucht Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="42d98-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="42d98-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42d98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42d98-108">Geben Sie die Parameter für den Suchvorgang an.</span><span class="sxs-lookup"><span data-stu-id="42d98-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="42d98-109">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="42d98-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="42d98-110">Wert</span><span class="sxs-lookup"><span data-stu-id="42d98-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="42d98-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="42d98-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="42d98-112"><dt>**Fr \_ nach unten**</dt></span><span class="sxs-lookup"><span data-stu-id="42d98-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="42d98-113">Microsoft Rich Edit 2,0 und höher: Wenn festgelegt, erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="42d98-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="42d98-114">Wenn nicht festgelegt, erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="42d98-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="42d98-115">Microsoft Rich Edit 1,0: das FR- \_ down-Flag wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="42d98-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="42d98-116">Die Suche erfolgt immer vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="42d98-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="42d98-117"><dt>**Fr \_ MatchAlefHamza**</dt></span><span class="sxs-lookup"><span data-stu-id="42d98-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="42d98-118">Microsoft Rich Edit 3,0 und höher: Wenn diese Einstellung festgelegt ist, unterscheidet die Suche zwischen arabischen Alefs und unterschiedlichen Akzenten.</span><span class="sxs-lookup"><span data-stu-id="42d98-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="42d98-119">Wenn nicht festgelegt, werden alle Alefs nur mit dem Alef-Zeichen abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="42d98-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="42d98-120"><dt>**Fr \_ matchdiac**</dt></span><span class="sxs-lookup"><span data-stu-id="42d98-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="42d98-121">Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische und hebräische diakritische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="42d98-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="42d98-122">Wenn nicht festgelegt, werden Diakritische Markierungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="42d98-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="42d98-123"><dt>**Fr \_ MatchKashida**</dt></span><span class="sxs-lookup"><span data-stu-id="42d98-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="42d98-124">Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische Kashidas.</span><span class="sxs-lookup"><span data-stu-id="42d98-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="42d98-125">Wenn nicht festgelegt, werden Kashidas ignoriert.</span><span class="sxs-lookup"><span data-stu-id="42d98-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="42d98-126"><dt>**Fr \_ matchwidth**</dt></span><span class="sxs-lookup"><span data-stu-id="42d98-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="42d98-127">Windows 8: Wenn Set, werden Einzel Byte-und Doppelbyte Versionen desselben Zeichens als ungleich betrachtet.</span><span class="sxs-lookup"><span data-stu-id="42d98-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="42d98-128"><dt>**"# \_ wholeword"**</dt></span><span class="sxs-lookup"><span data-stu-id="42d98-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="42d98-129">Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="42d98-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="42d98-130">Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="42d98-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="42d98-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42d98-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42d98-132">Eine [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, die Informationen über den Suchvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="42d98-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d98-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42d98-133">Return value</span></span>

<span data-ttu-id="42d98-134">Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="42d98-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="42d98-135">Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.</span><span class="sxs-lookup"><span data-stu-id="42d98-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d98-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42d98-136">Remarks</span></span>

<span data-ttu-id="42d98-137">Der **cpmin** -Member von **FindText. chrg** gibt immer den Anfangspunkt der Suche an, und **cpmax** gibt den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="42d98-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="42d98-138">Bei der Rückwärtssuche muss **cpmin** größer oder gleich **cpmax** sein.</span><span class="sxs-lookup"><span data-stu-id="42d98-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="42d98-139">Bei der Suche wird durch den Wert-1 in **cpmax** der Suchbereich auf das Ende des Texts erweitert.</span><span class="sxs-lookup"><span data-stu-id="42d98-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d98-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42d98-140">Requirements</span></span>



| <span data-ttu-id="42d98-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42d98-141">Requirement</span></span> | <span data-ttu-id="42d98-142">Wert</span><span class="sxs-lookup"><span data-stu-id="42d98-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42d98-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42d98-143">Minimum supported client</span></span><br/> | <span data-ttu-id="42d98-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42d98-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42d98-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42d98-145">Minimum supported server</span></span><br/> | <span data-ttu-id="42d98-146">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42d98-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42d98-147">Header</span><span class="sxs-lookup"><span data-stu-id="42d98-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d98-148"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d98-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42d98-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42d98-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d98-150">**FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="42d98-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





