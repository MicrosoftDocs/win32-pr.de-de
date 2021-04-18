---
description: Microsoft Windows Search verbessert auf der Grundlage der SQL-92-und SQL-99-Standards die voll Textdokument basierte Suche in Dokumenten-oder Wissens Verwaltungs Anwendungen.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQL-Erweiterungen in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525490"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a><span data-ttu-id="6116b-103">SQL-Erweiterungen in Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="6116b-103">SQL Extensions in Microsoft Windows Search</span></span>

<span data-ttu-id="6116b-104">Microsoft Windows Search verbessert auf der Grundlage der SQL-92-und SQL-99-Standards die voll Textdokument basierte Suche in Dokumenten-oder Wissens Verwaltungs Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6116b-104">Microsoft Windows Search, based on the SQL-92 and SQL-99 standards, improves full-text document-based searches in document-management or knowledge-management applications.</span></span> <span data-ttu-id="6116b-105">Die Verbesserungen der Windows-Suche umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6116b-105">Windows Search improvements include the following:</span></span>

## <a name="128-character-identifier-names"></a><span data-ttu-id="6116b-106">128-Zeichen Bezeichnernamen</span><span class="sxs-lookup"><span data-stu-id="6116b-106">128-Character Identifier Names</span></span>

<span data-ttu-id="6116b-107">Während SQL-92 und SQL-99 Spalten-und andere Bezeichner auf 18 Zeichen beschränken, unterstützt Windows Search 128 Zeichen-Spaltennamen.</span><span class="sxs-lookup"><span data-stu-id="6116b-107">While SQL-92 and SQL-99 restrict column and other identifiers to 18 characters, Windows Search supports 128-character column names.</span></span> <span data-ttu-id="6116b-108">Weitere Informationen finden Sie unter [Bezeichner](-search-sql-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="6116b-108">For more information, see [Identifiers](-search-sql-identifiers.md).</span></span>

## <a name="grouping-results-by-columns"></a><span data-ttu-id="6116b-109">Gruppieren von Ergebnissen nach Spalten</span><span class="sxs-lookup"><span data-stu-id="6116b-109">Grouping Results by Columns</span></span>

<span data-ttu-id="6116b-110">Abfragen können angeben, wie Ergebnisse gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6116b-110">Queries can specify how to group results.</span></span> <span data-ttu-id="6116b-111">Sie können die Bereiche angeben, nach denen gruppiert werden soll, und Sie können mehr als eine Spalte für die Gruppierung angeben.</span><span class="sxs-lookup"><span data-stu-id="6116b-111">You can specify the ranges by which to group, and you can specify more than one column for grouping.</span></span> <span data-ttu-id="6116b-112">Beispielsweise können Sie Ergebnisse für einen Bereich von Dateigrößen gruppieren (Größe < 100, 100 <= size < 1000; 1000 <= size), und Sie können Gruppierungen Schachteln.</span><span class="sxs-lookup"><span data-stu-id="6116b-112">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size), and you can nest groupings.</span></span> <span data-ttu-id="6116b-113">Weitere Informationen finden Sie unter [Group on... Über... -Anweisung](-search-sql-group-on-over.md).</span><span class="sxs-lookup"><span data-stu-id="6116b-113">For more information, see [GROUP ON ... OVER... Statement](-search-sql-group-on-over.md).</span></span>

## <a name="diacritic-insensitive-searching"></a><span data-ttu-id="6116b-114">Diacritic-Insensitive Suche</span><span class="sxs-lookup"><span data-stu-id="6116b-114">Diacritic-Insensitive Searching</span></span>

<span data-ttu-id="6116b-115">Neben der Suche, bei der die Groß-/Kleinschreibung nicht beachtet wird, unterstützt Windows Search die Suche, die nicht von diakritischen Zeichen (Akzentzeichen) abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="6116b-115">In addition to searching that is not case-sensitive, Windows Search supports searching that is not sensitive to diacritics (accent marks).</span></span> <span data-ttu-id="6116b-116">Weitere Informationen finden Sie unter [diakritische Sensitivität bei Such](-search-sql-accentinsensitivitysearches.md)Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="6116b-116">For more information, see [Diacritic Sensitivity in Searches](-search-sql-accentinsensitivitysearches.md).</span></span>

## <a name="column-weighting"></a><span data-ttu-id="6116b-117">Spalten Gewichtung</span><span class="sxs-lookup"><span data-stu-id="6116b-117">Column Weighting</span></span>

<span data-ttu-id="6116b-118">Abfragen, die mehr als eine Spalte durchsuchen, können die Wichtigkeit der einzelnen Spalten angeben.</span><span class="sxs-lookup"><span data-stu-id="6116b-118">Queries that search more than one column can specify the importance of each column.</span></span> <span data-ttu-id="6116b-119">Die Prädikate " [enthält](-search-sql-contains.md) " und " [fretext](-search-sql-freetext.md) " unterstützen die Spalten Gewichtung.</span><span class="sxs-lookup"><span data-stu-id="6116b-119">The [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates both support column weighting.</span></span>

## <a name="null-predicate"></a><span data-ttu-id="6116b-120">NULL-Prädikat</span><span class="sxs-lookup"><span data-stu-id="6116b-120">NULL Predicate</span></span>

<span data-ttu-id="6116b-121">Obwohl die voll Text Inhalts Indizierung keinen definierten Satz von Spalten aufweist, können Abfragen erfordern, dass die Elemente des Resultsets über angegebene Spalten verfügen oder nicht.</span><span class="sxs-lookup"><span data-stu-id="6116b-121">Although full-text content indexing has no defined set of columns, queries can require that members of the result set do or do not have specified columns.</span></span> <span data-ttu-id="6116b-122">Es ist nicht möglich, zwischen einem Dokument eine angegebene Eigenschaft mit dem Wert **null** und einem Dokument, das nicht die-Eigenschaft aufweist, zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6116b-122">It is not possible to differentiate between a document has a specified property with the value set to **NULL**, and a document that does not have the property at all.</span></span>

## <a name="rank-modification"></a><span data-ttu-id="6116b-123">Änderung von Rang</span><span class="sxs-lookup"><span data-stu-id="6116b-123">Rank Modification</span></span>

<span data-ttu-id="6116b-124">Sie können die Rangfolge der Suchergebnisse mithilfe von [Gewichtungen](-search-sql-understandingrelevancevalues.md) in Eigenschaften und in Alias Gruppen Gruppen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6116b-124">You can manipulate the search results ranking by using [weights](-search-sql-understandingrelevancevalues.md) on properties and on aliased groups of properties.</span></span> <span data-ttu-id="6116b-125">Rang Koersion unterstützt die direkte Bearbeitung der Relevanzrangfolge basierend auf den von Ihnen angegebenen Kriterien.</span><span class="sxs-lookup"><span data-stu-id="6116b-125">Rank coercion supports direct manipulation of the relevance ranking based on the criteria you specify.</span></span>

 

 



