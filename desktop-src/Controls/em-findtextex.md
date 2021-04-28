---
title: EM_FINDTEXTEX (Richedit.h)
description: 'EM_FINDTEXTEX Meldung: Sucht Text in einem Rich-Edit-Steuerelement.'
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 2158dabf9ea17d1bd4cac48454bdbb4056765752
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109838"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="a6f26-104">EM \_ FINDTEXTEX-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a6f26-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="a6f26-105">Sucht Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a6f26-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6f26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6f26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f26-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6f26-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6f26-108">Gibt das Verhalten des Suchvorgang an.</span><span class="sxs-lookup"><span data-stu-id="a6f26-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="a6f26-109">Dieser Parameter kann einen oder mehrere der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="a6f26-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a6f26-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a6f26-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="a6f26-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a6f26-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="a6f26-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="a6f26-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="a6f26-113">Microsoft Rich Edit 2.0 und höher: Wenn festgelegt, wird die Suche von **FINDTEXTEX.hlg.cpMin weitergeleitet.** Wenn dies nicht festgelegt ist, befindet sich die Suche rückwärts von **FINDTEXTEX.chrg.cpMin.**</span><span class="sxs-lookup"><span data-stu-id="a6f26-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="a6f26-114">Microsoft Rich Edit 1.0: Das FR \_ DOWN-Flag wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a6f26-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="a6f26-115">Die Suche ist immer vorwärts.</span><span class="sxs-lookup"><span data-stu-id="a6f26-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="a6f26-116"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="a6f26-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="a6f26-117">Microsoft Rich Edit 3.0 und höher: Wenn festgelegt, unterscheidet die Suche zwischen arabischen und hebräischen Alefs mit unterschiedlichen Akzenten.</span><span class="sxs-lookup"><span data-stu-id="a6f26-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="a6f26-118">Wenn nicht festgelegt, werden alle Alefs allein durch das Alef-Zeichen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a6f26-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="a6f26-119"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="a6f26-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="a6f26-120">Wenn festgelegt, wird beim Suchvorgang die Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="a6f26-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="a6f26-121">Wenn dies nicht festgelegt ist, wird beim Suchvorgang die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a6f26-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="a6f26-122"><dt>**FR \_ MATCHDMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="a6f26-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="a6f26-123">Microsoft Rich Edit 3.0 und höher: Wenn festgelegt, berücksichtigt der Suchvorgang arabische und hebräische diakritische Markierungen.</span><span class="sxs-lookup"><span data-stu-id="a6f26-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="a6f26-124">Wenn nicht festgelegt, werden diakritische Markierungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a6f26-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="a6f26-125"><dt>**FR \_ MATCHKDDADA**</dt></span><span class="sxs-lookup"><span data-stu-id="a6f26-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="a6f26-126">Microsoft Rich Edit 3.0 und höher: Falls festgelegt, berücksichtigt der Suchvorgang arabische und hebräische Kashdas.</span><span class="sxs-lookup"><span data-stu-id="a6f26-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="a6f26-127">Wenn diese Einstellung nicht festgelegt ist, werden Kblenden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a6f26-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="a6f26-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="a6f26-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="a6f26-129">Wenn diese Einstellung festgelegt ist, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a6f26-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="a6f26-130">Wenn diese Einstellung nicht festgelegt ist, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a6f26-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="a6f26-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6f26-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6f26-132">Eine [**FINDTEXTEX-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) die Informationen zum Suchvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="a6f26-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f26-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6f26-133">Return value</span></span>

<span data-ttu-id="a6f26-134">Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="a6f26-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="a6f26-135">Wenn das Ziel nicht gefunden wird, lautet der Rückgabewert -1.</span><span class="sxs-lookup"><span data-stu-id="a6f26-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f26-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6f26-136">Remarks</span></span>

<span data-ttu-id="a6f26-137">Verwenden Sie diese Meldung, um ANSI-Zeichenfolgen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a6f26-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="a6f26-138">Verwenden Sie für Unicode [**EM \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="a6f26-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="a6f26-139">Der **cpMin-Member** von **FINDTEXTEX.chg** gibt immer den Startpunkt der Suche und **cpMax** den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="a6f26-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="a6f26-140">Beim Rückwärtssuchen muss **cpMin** gleich oder größer als **cpMax** sein.</span><span class="sxs-lookup"><span data-stu-id="a6f26-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="a6f26-141">Bei der Vorwärtssuche erweitert der Wert -1 in **cpMax** den Suchbereich bis zum Ende des Texts.</span><span class="sxs-lookup"><span data-stu-id="a6f26-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="a6f26-142">Wenn der Suchvorgang eine Übereinstimmung findet, gibt der **chgText-Member** der [**FINDTEXTEX-Struktur**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) den Bereich der Zeichenpositionen zurück, der den übereinstimmenden Text enthält.</span><span class="sxs-lookup"><span data-stu-id="a6f26-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f26-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6f26-143">Requirements</span></span>



| <span data-ttu-id="a6f26-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6f26-144">Requirement</span></span> | <span data-ttu-id="a6f26-145">Wert</span><span class="sxs-lookup"><span data-stu-id="a6f26-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f26-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6f26-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f26-147">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6f26-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6f26-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6f26-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f26-149">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6f26-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6f26-150">Header</span><span class="sxs-lookup"><span data-stu-id="a6f26-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6f26-151"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f26-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f26-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a6f26-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f26-153">**EM \_ FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="a6f26-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





