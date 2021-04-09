---
description: Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'Iinkanalyzer:: Search-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129441"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="4d82d-103">Iinkanalyzer:: Search-Methode</span><span class="sxs-lookup"><span data-stu-id="4d82d-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="4d82d-104">Stellt eine Fuzzysuche, bei der die Groß-/Kleinschreibung beachtet wird, nach analysierten Schreibvorgängen und analysierten Zeichnungs Strichen mit erkannten Typen bereit.</span><span class="sxs-lookup"><span data-stu-id="4d82d-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d82d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d82d-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="4d82d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d82d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d82d-107">*bstrauphrattomatch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d82d-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d82d-108">Der Ausdruck, der in den Alternativen für die aktuell analysierten Striche zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="4d82d-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="4d82d-109">*pulsearchresultcount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4d82d-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d82d-110">Die maximale Anzahl von Ergebnissen, die von der Suche zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4d82d-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="4d82d-111">*ppulstrokezähltperresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4d82d-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d82d-112">Zeiger auf ein Array mit der Anzahl der Striche in jedem Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="4d82d-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="4d82d-113">*pulstrokeidscount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4d82d-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d82d-114">Die Anzahl der Strich-IDs in *ppulstrokeids*.</span><span class="sxs-lookup"><span data-stu-id="4d82d-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="4d82d-115">*ppulstrokeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4d82d-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d82d-116">Ein Zeiger auf ein Array von Strich-IDs, das einen Satz von Strichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="4d82d-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d82d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d82d-117">Return value</span></span>

<span data-ttu-id="4d82d-118">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4d82d-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d82d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d82d-119">Remarks</span></span>

<span data-ttu-id="4d82d-120">Bei dieser Suche werden Teil Zeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gefunden.</span><span class="sxs-lookup"><span data-stu-id="4d82d-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="4d82d-121">Sowohl alternative Erkennungsergebnisse als auch alternative Segmentationen werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="4d82d-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="4d82d-122">Alle eingehenden Zeichen folgen werden für Vergleiche in eine einzelne Schreibweise konvertiert, wobei die LCID des aktuellen Threads verwendet wird, um diese Konvertierung durchzuführen, um kulturelle Fälle zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="4d82d-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="4d82d-123">Die Übergabe Zeichenfolge wird als Ausdruck behandelt.</span><span class="sxs-lookup"><span data-stu-id="4d82d-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="4d82d-124">Wörter und Zeichen müssen in alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4d82d-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="4d82d-125">Das erste und das letzte Wort des Ausdrucks können als Teil Zeichenfolgen abgeglichen werden (das erste Wort, das am Ende einer alternativen angezeigt wird, und das letzte Wort, das bei der beginginging-Darstellung auftritt), aber alle anderen Wörter (die innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4d82d-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="4d82d-126">Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teil Zeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einer alternativen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="4d82d-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="4d82d-127">Die Ergebnisse der Suche werden nur durch das vorhanden sein oder Fehlen von Leerzeichen zwischen Zeichen geändert.</span><span class="sxs-lookup"><span data-stu-id="4d82d-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="4d82d-128">Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4d82d-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="4d82d-129">Der Typ des Leerraums wird ignoriert (ein Tabstopp-oder Leerzeichen zwischen Zeichen gibt das gleiche Ergebnis aus).</span><span class="sxs-lookup"><span data-stu-id="4d82d-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="4d82d-130">Die Menge an Leerzeichen ist nicht von Bedeutung-ein Leerzeichen oder zwei Leerzeichen zwischen Zeichen haben das gleiche Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="4d82d-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="4d82d-131">Die Suche generiert keine Ereignisse von "PopulateContextNode".</span><span class="sxs-lookup"><span data-stu-id="4d82d-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="4d82d-132">Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="4d82d-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d82d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d82d-133">Requirements</span></span>



| <span data-ttu-id="4d82d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d82d-134">Requirement</span></span> | <span data-ttu-id="4d82d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4d82d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d82d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d82d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4d82d-137">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d82d-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d82d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d82d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4d82d-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d82d-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4d82d-140">Header</span><span class="sxs-lookup"><span data-stu-id="4d82d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d82d-141"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4d82d-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4d82d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4d82d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d82d-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d82d-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4d82d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d82d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d82d-145">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="4d82d-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




