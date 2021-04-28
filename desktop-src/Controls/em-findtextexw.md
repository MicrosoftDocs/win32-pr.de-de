---
title: EM_FINDTEXTEXW (Richedit.h)
description: 'EM_FINDTEXTEXW Meldung: Sucht Unicode-Text in einem Rich-Edit-Steuerelement.'
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109808"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="00b20-104">EM \_ FINDTEXTEXW-Nachricht</span><span class="sxs-lookup"><span data-stu-id="00b20-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="00b20-105">Sucht Unicode-Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="00b20-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="00b20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00b20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00b20-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00b20-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00b20-108">Gibt das Verhalten des Suchvorgang an.</span><span class="sxs-lookup"><span data-stu-id="00b20-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="00b20-109">Dieser Parameter kann einen oder mehrere der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="00b20-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="00b20-110">Wert</span><span class="sxs-lookup"><span data-stu-id="00b20-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="00b20-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="00b20-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="00b20-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="00b20-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="00b20-113">Microsoft Rich Edit 2.0 und höher: Wenn festgelegt, wird die Suche von **FINDTEXTEX.hlg.cpMin weitergeleitet.** Wenn dies nicht festgelegt ist, befindet sich die Suche rückwärts von **FINDTEXTEX.chrg.cpMin.**</span><span class="sxs-lookup"><span data-stu-id="00b20-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="00b20-114">Microsoft Rich Edit 1.0: Das FR \_ DOWN-Flag wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="00b20-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="00b20-115">Die Suche ist immer vorwärts.</span><span class="sxs-lookup"><span data-stu-id="00b20-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="00b20-116"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="00b20-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="00b20-117">Wenn festgelegt, unterscheidet die Suche zwischen Alefs mit unterschiedlichen Akzenten.</span><span class="sxs-lookup"><span data-stu-id="00b20-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="00b20-118">Wenn dies nicht festgelegt ist, werden arabische und hebräische Alefs mit unterschiedlichen Akzenten durch das Alef-Zeichen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="00b20-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="00b20-119"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="00b20-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="00b20-120">Wenn festgelegt, wird beim Suchvorgang die Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="00b20-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="00b20-121">Wenn dies nicht festgelegt ist, wird beim Suchvorgang die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="00b20-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="00b20-122"><dt>**FR \_ MATCHDMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="00b20-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="00b20-123">Wenn festgelegt, berücksichtigt der Suchvorgang diakritische Markierungen.</span><span class="sxs-lookup"><span data-stu-id="00b20-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="00b20-124">Wenn dies nicht festgelegt ist, werden arabische und hebräische diakritische Markierungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="00b20-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="00b20-125"><dt>**FR \_ MATCHKDDADA**</dt></span><span class="sxs-lookup"><span data-stu-id="00b20-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="00b20-126">Wenn diese Einstellung festgelegt ist, berücksichtigt der Suchvorgang K msidas.</span><span class="sxs-lookup"><span data-stu-id="00b20-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="00b20-127">Wenn sie nicht festgelegt ist, werden arabische und hebräische K msidas ignoriert.</span><span class="sxs-lookup"><span data-stu-id="00b20-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="00b20-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="00b20-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="00b20-129">Wenn diese Einstellung festgelegt ist, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="00b20-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="00b20-130">Wenn diese Einstellung nicht festgelegt ist, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="00b20-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="00b20-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00b20-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00b20-132">Eine [**FINDTEXTEXW-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) die Informationen zum Suchvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="00b20-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00b20-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00b20-133">Return value</span></span>

<span data-ttu-id="00b20-134">Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="00b20-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="00b20-135">Wenn das Ziel nicht gefunden wird, lautet der Rückgabewert -1.</span><span class="sxs-lookup"><span data-stu-id="00b20-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="00b20-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00b20-136">Remarks</span></span>

<span data-ttu-id="00b20-137">Verwenden Sie diese Meldung, um Unicode-Zeichenfolgen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00b20-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="00b20-138">Verwenden Sie für ANSI; [**EM \_ FINDTEXTEX**](em-findtextex.md).</span><span class="sxs-lookup"><span data-stu-id="00b20-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="00b20-139">Der **cpMin-Member** von **FINDTEXTEX.chg** gibt immer den Startpunkt der Suche und **cpMax** den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="00b20-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="00b20-140">Beim Rückwärtssuchen muss **cpMin** gleich oder größer als **cpMax** sein.</span><span class="sxs-lookup"><span data-stu-id="00b20-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="00b20-141">Bei der Vorwärtssuche erweitert der Wert -1 in **cpMax** den Suchbereich bis zum Ende des Texts.</span><span class="sxs-lookup"><span data-stu-id="00b20-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="00b20-142">Wenn der Suchvorgang eine Übereinstimmung findet, gibt der **chgText-Member** der [**FINDTEXTEX-Struktur**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) den Bereich der Zeichenpositionen zurück, der den übereinstimmenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="00b20-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="00b20-143">**EM \_ FINDTEXTEXW** verwendet die [**FINDTEXTEXW-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) [**während EM \_ FINDTEXTW**](em-findtextw.md) die [**FINDTEXTW-Struktur**](/windows/win32/api/richedit/ns-richedit-findtexta) verwendet.</span><span class="sxs-lookup"><span data-stu-id="00b20-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="00b20-144">Der Unterschied besteht darin, dass **EM \_ FINDTEXTEXW** den gefundenen Textbereich meldet.</span><span class="sxs-lookup"><span data-stu-id="00b20-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="00b20-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00b20-145">Requirements</span></span>



| <span data-ttu-id="00b20-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00b20-146">Requirement</span></span> | <span data-ttu-id="00b20-147">Wert</span><span class="sxs-lookup"><span data-stu-id="00b20-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00b20-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00b20-148">Minimum supported client</span></span><br/> | <span data-ttu-id="00b20-149">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00b20-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00b20-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00b20-150">Minimum supported server</span></span><br/> | <span data-ttu-id="00b20-151">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00b20-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00b20-152">Header</span><span class="sxs-lookup"><span data-stu-id="00b20-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="00b20-153"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="00b20-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00b20-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00b20-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b20-155">**EM \_ FINDTEXTW**</span><span class="sxs-lookup"><span data-stu-id="00b20-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





