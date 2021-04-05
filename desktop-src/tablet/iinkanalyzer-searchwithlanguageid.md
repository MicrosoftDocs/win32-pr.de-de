---
description: Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'Iinkanalyzer:: searchwithlanguageid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 829878a6fd326abb8a685b644cfc222ba6921385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751793"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="f5478-103">Iinkanalyzer:: searchwithlanguageid-Methode</span><span class="sxs-lookup"><span data-stu-id="f5478-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="f5478-104">Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.</span><span class="sxs-lookup"><span data-stu-id="f5478-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5478-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5478-105">Syntax</span></span>


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="f5478-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5478-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5478-107">*bstrauphrattomatch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5478-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5478-108">Der Ausdruck, der in den Alternativen für die aktuell analysierten Striche zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="f5478-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="f5478-109">*lsearchstringlanguageid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5478-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5478-110">Die LCID, die der bestandenen Zeichenfolge zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f5478-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="f5478-111">Wird zum internen Konvertieren der Groß-/Kleinschreibung verwendet</span><span class="sxs-lookup"><span data-stu-id="f5478-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="f5478-112">*pulsearchresultcount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f5478-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5478-113">Die maximale Anzahl von Ergebnissen, die von der Suche zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f5478-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="f5478-114">*ppulstrokezähltperresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f5478-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5478-115">Zeiger auf ein Array mit der Anzahl der Striche in jedem Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="f5478-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="f5478-116">*pulstrokeidscount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f5478-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5478-117">Die Anzahl der Strich-IDs in *ppulstrokeids*.</span><span class="sxs-lookup"><span data-stu-id="f5478-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="f5478-118">*ppulstrokeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f5478-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5478-119">Ein Zeiger auf ein Array von Strich-IDs, das einen Satz von Strichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5478-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5478-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5478-120">Return value</span></span>

<span data-ttu-id="f5478-121">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f5478-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5478-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5478-122">Remarks</span></span>

<span data-ttu-id="f5478-123">Bei dieser Suche werden Teil Zeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gefunden.</span><span class="sxs-lookup"><span data-stu-id="f5478-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="f5478-124">Sowohl alternative Erkennungsergebnisse als auch alternative Segmentationen werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="f5478-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="f5478-125">Alle eingehenden Zeichen folgen werden für Vergleiche in eine einzelne Schreibweise konvertiert, wobei die LCID des aktuellen Threads verwendet wird, um diese Konvertierung durchzuführen, um kulturelle Fälle zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="f5478-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="f5478-126">Die Übergabe Zeichenfolge wird als Ausdruck behandelt.</span><span class="sxs-lookup"><span data-stu-id="f5478-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="f5478-127">Wörter und Zeichen müssen in alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5478-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="f5478-128">Das erste und das letzte Wort des Ausdrucks können als Teil Zeichenfolgen abgeglichen werden (das erste Wort, das am Ende einer alternativen angezeigt wird, und das letzte Wort, das bei der beginginging-Darstellung auftritt), aber alle anderen Wörter (die innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5478-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="f5478-129">Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teil Zeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einer alternativen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="f5478-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="f5478-130">Die Ergebnisse der Suche werden nur durch das vorhanden sein oder Fehlen von Leerzeichen zwischen Zeichen geändert.</span><span class="sxs-lookup"><span data-stu-id="f5478-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="f5478-131">Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f5478-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="f5478-132">Der Typ des Leerraums wird ignoriert (ein Tabstopp-oder Leerzeichen zwischen Zeichen gibt das gleiche Ergebnis aus).</span><span class="sxs-lookup"><span data-stu-id="f5478-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="f5478-133">Die Menge an Leerzeichen ist nicht von Bedeutung-ein Leerzeichen oder zwei Leerzeichen zwischen Zeichen haben das gleiche Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="f5478-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="f5478-134">Die Suche generiert keine Ereignisse von "PopulateContextNode".</span><span class="sxs-lookup"><span data-stu-id="f5478-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="f5478-135">Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="f5478-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5478-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5478-136">Requirements</span></span>



| <span data-ttu-id="f5478-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5478-137">Requirement</span></span> | <span data-ttu-id="f5478-138">Wert</span><span class="sxs-lookup"><span data-stu-id="f5478-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5478-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5478-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f5478-140">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5478-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5478-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5478-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f5478-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f5478-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f5478-143">Header</span><span class="sxs-lookup"><span data-stu-id="f5478-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5478-144"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5478-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5478-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f5478-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5478-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5478-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f5478-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5478-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5478-148">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="f5478-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




