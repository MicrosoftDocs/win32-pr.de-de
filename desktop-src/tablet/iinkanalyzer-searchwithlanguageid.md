---
description: 'IInkAnalyzer::SearchWithLanguageId-Methode: Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Kenntnis.'
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: IInkAnalyzer::SearchWithLanguageId-Methode (IACom.h)
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
ms.openlocfilehash: 201469933da10b0d68a4d3a50e63c42f8d01d2dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083658"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="222c2-103">IInkAnalyzer::SearchWithLanguageId-Methode</span><span class="sxs-lookup"><span data-stu-id="222c2-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="222c2-104">Stellt eine fuzzybasierte Suche nach analysierten Schreibstrichen und analysierten Zeichnungsstrichen mit erkannten Typen ohne Unterschiedliche Groß-/Kleinschreibung zur Unterstützung der Groß-/Kleinschreibung zur Lage.</span><span class="sxs-lookup"><span data-stu-id="222c2-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="222c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="222c2-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="222c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="222c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="222c2-107">*bstrPhraseToMatch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="222c2-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222c2-108">Der Ausdruck, der in den Alternativen für die derzeit analysierten Striche gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="222c2-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="222c2-109">*lSearchStringLanguageId* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="222c2-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222c2-110">Die LCID, die der übergebenen Zeichenfolge zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="222c2-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="222c2-111">Wird verwendet, um die Groß-/Kleinschreibung intern zu konvertieren, um Vergleiche ohne Unterscheidung nach Groß-/Kleinschreibung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="222c2-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="222c2-112">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="222c2-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="222c2-113">Die maximale Anzahl von Ergebnissen, die von der Suche zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="222c2-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="222c2-114">*ppulStrokeCountPerResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="222c2-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="222c2-115">Zeiger auf ein Array der Anzahl von Strichen in jedem Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="222c2-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="222c2-116">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="222c2-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="222c2-117">Die Anzahl der Strich-IDs in *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="222c2-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="222c2-118">*ppulStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="222c2-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="222c2-119">Zeiger auf ein Array von Strich-IDs, die einen Satz von Strichen darstellen.</span><span class="sxs-lookup"><span data-stu-id="222c2-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="222c2-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="222c2-120">Return value</span></span>

<span data-ttu-id="222c2-121">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="222c2-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="222c2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="222c2-122">Remarks</span></span>

<span data-ttu-id="222c2-123">Bei dieser Suche werden Teilzeichenfolgen mit mehreren Wörtern und einzelnen Wörtern gefunden.</span><span class="sxs-lookup"><span data-stu-id="222c2-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="222c2-124">Sowohl alternative Erkennungsergebnisse als auch alternative Segmentierungen werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="222c2-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="222c2-125">Alle eingehenden Zeichenfolgen werden für den Vergleich mithilfe der LCID des aktuellen Threads in eine einzelne Zeichenfolge konvertiert, um diese Konvertierung zur Einhaltung von Kulturfallkonventionen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="222c2-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="222c2-126">Die übergebene Zeichenfolge wird als Ausdruck behandelt.</span><span class="sxs-lookup"><span data-stu-id="222c2-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="222c2-127">Wörter und Zeichen müssen in den Alterantes für die Striche in der angegebenen Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="222c2-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="222c2-128">Das erste und das letzte Wort des Ausdrucks können als Teilzeichenfolgen übereinstimmen (das erste Wort, das am Ende eines alternativen Worts und das letzte Wort, das beim Umhügen eines Worts angezeigt wird), aber alle anderen Wörter (die innerhalb des Ausdrucks) müssen als ganze Wörter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="222c2-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="222c2-129">Wenn die übergebene Zeichenfolge keine Leerzeichen zwischen Zeichen enthält, kann die Teilzeichenfolge an einer beliebigen Stelle innerhalb eines einzelnen Worts in einem alternativen Gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="222c2-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="222c2-130">Nur das Vorhandensein oder Fehlen von Leerzeichen zwischen Zeichen ändert die Ergebnisse der Suche.</span><span class="sxs-lookup"><span data-stu-id="222c2-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="222c2-131">Leerzeichen, die nicht von Zeichen umgeben sind, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="222c2-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="222c2-132">Der Typ des Leerraums wird ignoriert (eine Registerkarte oder ein Leerzeichen zwischen Zeichen führt zu demselben Ergebnis).</span><span class="sxs-lookup"><span data-stu-id="222c2-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="222c2-133">Die Menge an Leerzeichen spielt keine Rolle. Ein oder zwei Leerzeichen zwischen Zeichen führen zu demselben Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="222c2-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="222c2-134">Die Suche generiert keine PopulateContextNode-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="222c2-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="222c2-135">Nur die Striche, die bereits aufgefüllt wurden, werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="222c2-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="222c2-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="222c2-136">Requirements</span></span>



| <span data-ttu-id="222c2-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="222c2-137">Requirement</span></span> | <span data-ttu-id="222c2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="222c2-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="222c2-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="222c2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="222c2-140">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="222c2-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="222c2-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="222c2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="222c2-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="222c2-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="222c2-143">Header</span><span class="sxs-lookup"><span data-stu-id="222c2-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="222c2-144"><dt>IACom.h (erfordert auch IACom \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="222c2-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="222c2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="222c2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="222c2-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="222c2-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="222c2-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="222c2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222c2-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="222c2-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




