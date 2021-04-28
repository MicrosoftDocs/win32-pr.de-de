---
description: 'IInkAnalyzer::Search-Methode: Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Lage.'
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: IInkAnalyzer::Search-Methode (IACom.h)
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
ms.openlocfilehash: 94ccdebf8c8a134a845ff3df3017d710d1da93f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113728"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="69b16-103">IInkAnalyzer::Search-Methode</span><span class="sxs-lookup"><span data-stu-id="69b16-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="69b16-104">Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Lage.</span><span class="sxs-lookup"><span data-stu-id="69b16-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69b16-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="69b16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69b16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b16-107">*bstrPhraseToMatch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="69b16-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b16-108">Der Ausdruck, der in den Alternativen für die derzeit analysierten Striche gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="69b16-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="69b16-109">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="69b16-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69b16-110">Die maximale Anzahl von Ergebnissen, die von der Suche zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="69b16-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="69b16-111">*ppulStrokeCountPerResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69b16-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69b16-112">Zeiger auf ein Array der Anzahl von Strichen in jedem Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="69b16-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="69b16-113">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="69b16-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69b16-114">Die Anzahl der Strich-IDs in *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="69b16-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="69b16-115">*ppulStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69b16-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69b16-116">Zeiger auf ein Array von Strich-IDs, die einen Satz von Strichen darstellen.</span><span class="sxs-lookup"><span data-stu-id="69b16-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b16-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69b16-117">Return value</span></span>

<span data-ttu-id="69b16-118">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="69b16-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69b16-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69b16-119">Remarks</span></span>

<span data-ttu-id="69b16-120">Bei dieser Suche werden Teilzeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gefunden.</span><span class="sxs-lookup"><span data-stu-id="69b16-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="69b16-121">Sowohl alternative Erkennungsergebnisse als auch alternative Segmentierungen werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="69b16-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="69b16-122">Alle eingehenden Zeichenfolgen werden für den Vergleich mithilfe der LCID des aktuellen Threads in eine einzelne Zeichenfolge konvertiert, um diese Konvertierung zur Einhaltung von Kulturfallkonventionen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="69b16-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="69b16-123">Die übergebene Zeichenfolge wird als Ausdruck behandelt.</span><span class="sxs-lookup"><span data-stu-id="69b16-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="69b16-124">Wörter und Zeichen müssen in den Alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="69b16-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="69b16-125">Die ersten und letzten Wörter des Ausdrucks können als Teilzeichenfolgen abgeglichen werden (das erste Wort, das am Ende eines alternativen und das letzte Wort beim Umbetten eines worts angezeigt wird), aber alle anderen Wörter (innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="69b16-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="69b16-126">Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teilzeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einer alternativen Zeichenfolge gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="69b16-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="69b16-127">Nur das Vorhandensein oder Fehlen von Leerzeichen zwischen Zeichen ändert die Ergebnisse der Suche.</span><span class="sxs-lookup"><span data-stu-id="69b16-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="69b16-128">Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="69b16-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="69b16-129">Der Typ des Leerraums wird ignoriert (eine Registerkarte oder ein Leerzeichen zwischen Zeichen führt zum gleichen Ergebnis).</span><span class="sxs-lookup"><span data-stu-id="69b16-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="69b16-130">Die Leerraummenge spielt keine Rolle. Ein leerzeichen oder zwei Leerzeichen zwischen Zeichen ergeben das gleiche Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="69b16-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="69b16-131">Die Suche generiert keine PopulateContextNode-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="69b16-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="69b16-132">Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="69b16-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b16-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69b16-133">Requirements</span></span>



| <span data-ttu-id="69b16-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69b16-134">Requirement</span></span> | <span data-ttu-id="69b16-135">Wert</span><span class="sxs-lookup"><span data-stu-id="69b16-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b16-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69b16-136">Minimum supported client</span></span><br/> | <span data-ttu-id="69b16-137">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="69b16-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69b16-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69b16-138">Minimum supported server</span></span><br/> | <span data-ttu-id="69b16-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="69b16-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="69b16-140">Header</span><span class="sxs-lookup"><span data-stu-id="69b16-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b16-141"><dt>IACom.h (erfordert auch IACom \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="69b16-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69b16-142">DLL</span><span class="sxs-lookup"><span data-stu-id="69b16-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69b16-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69b16-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="69b16-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="69b16-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b16-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="69b16-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




