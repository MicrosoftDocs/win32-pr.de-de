---
title: EM_FINDTEXT Nachricht (Richedit.h)
description: 'EM_FINDTEXT Meldung: Sucht Text in einem Rich Edit-Steuerelement.'
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 452d4e2534fb05cbbbf4c02ac4146f2f8914c9bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109848"
---
# <a name="em_findtext-message"></a><span data-ttu-id="11aca-104">\_EM-FINDTEXT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="11aca-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="11aca-105">Sucht Text in einem Rich-Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="11aca-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="11aca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11aca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11aca-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11aca-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11aca-108">Geben Sie die Parameter des Suchvorgangs an.</span><span class="sxs-lookup"><span data-stu-id="11aca-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="11aca-109">Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="11aca-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="11aca-110">Wert</span><span class="sxs-lookup"><span data-stu-id="11aca-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="11aca-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="11aca-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="11aca-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="11aca-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="11aca-113">Microsoft Rich Edit 2.0 und höher: Bei Festlegung erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="11aca-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="11aca-114">Wenn diese Option nicht festgelegt ist, erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="11aca-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="11aca-115">Microsoft Rich Edit 1.0: Das FR \_ DOWN-Flag wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="11aca-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="11aca-116">Die Suche erfolgt immer vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="11aca-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="11aca-117"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="11aca-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="11aca-118">Microsoft Rich Edit 3.0 und höher: Bei Festlegung unterscheidet die Suche zwischen arabischen Alefs mit unterschiedlichen Akzenten.</span><span class="sxs-lookup"><span data-stu-id="11aca-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="11aca-119">Wenn sie nicht festgelegt ist, werden alle Alefs allein durch das Alef-Zeichen abgegleichen.</span><span class="sxs-lookup"><span data-stu-id="11aca-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="11aca-120"><dt>**FR \_ MATCHDAKA**</dt></span><span class="sxs-lookup"><span data-stu-id="11aca-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="11aca-121">Microsoft Rich Edit 3.0 und höher: Wenn festgelegt, berücksichtigt der Suchvorgang arabische und hebräische diakritische Markierungen.</span><span class="sxs-lookup"><span data-stu-id="11aca-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="11aca-122">Wenn sie nicht festgelegt ist, werden diakritische Markierungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="11aca-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="11aca-123"><dt>**FR \_ MATCHKDDADA**</dt></span><span class="sxs-lookup"><span data-stu-id="11aca-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="11aca-124">Microsoft Rich Edit 3.0 und höher: Falls festgelegt, berücksichtigt der Suchvorgang arabische Kashdas.</span><span class="sxs-lookup"><span data-stu-id="11aca-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="11aca-125">Wenn dies nicht festgelegt ist, werden k seit dem Festlegen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="11aca-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="11aca-126"><dt>**FR \_ MATCHWIDTH**</dt></span><span class="sxs-lookup"><span data-stu-id="11aca-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="11aca-127">Windows 8: Wenn festgelegt, werden Einzel-Byte- und Doppel-Byte-Versionen desselben Zeichens als nicht gleich betrachtet.</span><span class="sxs-lookup"><span data-stu-id="11aca-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="11aca-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="11aca-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="11aca-129">Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="11aca-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="11aca-130">Wenn nicht festgelegt, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="11aca-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="11aca-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11aca-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11aca-132">Eine [**FINDTEXT-Struktur,**](/windows/win32/api/richedit/ns-richedit-findtexta) die Informationen zum Find-Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="11aca-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11aca-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11aca-133">Return value</span></span>

<span data-ttu-id="11aca-134">Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="11aca-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="11aca-135">Wenn das Ziel nicht gefunden wird, ist der Rückgabewert -1.</span><span class="sxs-lookup"><span data-stu-id="11aca-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="11aca-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11aca-136">Remarks</span></span>

<span data-ttu-id="11aca-137">Der **cpMin-Member** **von FINDTEXT.chrg** gibt immer den Ausgangspunkt der Suche an, und **cpMax** gibt den Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="11aca-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="11aca-138">Bei der Rückwärtssuche **muss cpMin** gleich oder größer als **cpMax sein.**</span><span class="sxs-lookup"><span data-stu-id="11aca-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="11aca-139">Bei der Vorwärtssuche erweitert der Wert -1 in **cpMax** den Suchbereich bis zum Ende des Texts.</span><span class="sxs-lookup"><span data-stu-id="11aca-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="11aca-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11aca-140">Requirements</span></span>



| <span data-ttu-id="11aca-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11aca-141">Requirement</span></span> | <span data-ttu-id="11aca-142">Wert</span><span class="sxs-lookup"><span data-stu-id="11aca-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11aca-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11aca-143">Minimum supported client</span></span><br/> | <span data-ttu-id="11aca-144">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11aca-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11aca-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11aca-145">Minimum supported server</span></span><br/> | <span data-ttu-id="11aca-146">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11aca-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11aca-147">Header</span><span class="sxs-lookup"><span data-stu-id="11aca-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="11aca-148"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="11aca-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11aca-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11aca-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11aca-150">**Findtext**</span><span class="sxs-lookup"><span data-stu-id="11aca-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





