---
description: In einer relationalen Datenbank müssen Zeilen, die von einer Suchabfrage zurückgegeben werden, alle Bedingungen erfüllen, die von der Abfrage aufgerufen werden. Im Gegensatz dazu kann eine Windows Search-Abfrage Dokumente zurückgeben, die die Suchbedingungen in variierender Grad erfüllen.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Verstehen von relevanzwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862151"
---
# <a name="understanding-relevance-values"></a><span data-ttu-id="e4110-104">Verstehen von relevanzwerten</span><span class="sxs-lookup"><span data-stu-id="e4110-104">Understanding Relevance Values</span></span>

<span data-ttu-id="e4110-105">In einer relationalen Datenbank müssen Zeilen, die von einer Suchabfrage zurückgegeben werden, alle Bedingungen erfüllen, die von der Abfrage aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e4110-105">In a relational database, rows that are returned by a search query must meet all the conditions called for by the query.</span></span> <span data-ttu-id="e4110-106">Im Gegensatz dazu kann eine Windows Search-Abfrage Dokumente zurückgeben, die die Suchbedingungen in variierender Grad erfüllen.</span><span class="sxs-lookup"><span data-stu-id="e4110-106">In contrast, a Windows Search query can return documents that meet the search conditions to varying degrees.</span></span>

<span data-ttu-id="e4110-107">Eine Suche nach dem Begriff "Program" in einer relationalen Datenbank erzeugt z. b. Datensätze, die die jeweilige Schreibweise des Worts enthalten.</span><span class="sxs-lookup"><span data-stu-id="e4110-107">For example, a search for the term "program" in a relational database produces records that contain that specific spelling of the word.</span></span> <span data-ttu-id="e4110-108">Ob ein Datensatz eine oder 100 Instanzen des Worts enthält, hat keine Auswirkung auf die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="e4110-108">Whether a record contains one or one hundred instances of the word has no impact on the results.</span></span> <span data-ttu-id="e4110-109">Im Gegensatz dazu gibt Windows Search einen relevanzwert zurück, der mit den übereinstimmenden Dokumenten verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e4110-109">In contrast, Windows Search returns a relevance value associated with the matching documents.</span></span> <span data-ttu-id="e4110-110">Die Relevanz von Dokumenten mit dem Titel "Program" im Titel ist höher als diejenigen, die das Wort nur im letzten Absatz enthalten.</span><span class="sxs-lookup"><span data-stu-id="e4110-110">The relevance of documents having "program" in the title is higher than those that contain the word only in the last paragraph.</span></span> <span data-ttu-id="e4110-111">Ebenso Stimmen Dokumente, die Variationen des Suchbegriffs enthalten, z. b. "Programme" und "Programming", auch mit der Abfrage zurück.</span><span class="sxs-lookup"><span data-stu-id="e4110-111">Similarly, documents containing variations of the search term, for example "programs" and "programming" also match and are returned by the query.</span></span>

<span data-ttu-id="e4110-112">Windows Search-Abfragen geben ganzzahlige Relevanzwerte in der Spalte mit dem Namen "Rank" zurück.</span><span class="sxs-lookup"><span data-stu-id="e4110-112">Windows Search queries return integer relevance values in the column named "rank".</span></span>

<span data-ttu-id="e4110-113">Zusätzlich:</span><span class="sxs-lookup"><span data-stu-id="e4110-113">In addition:</span></span>

-   <span data-ttu-id="e4110-114">Von der Abfrage zurückgegebene Rang Werte sind ganze Zahlen zwischen 0 und 1000.</span><span class="sxs-lookup"><span data-stu-id="e4110-114">Rank values returned by the query are integers ranging from 0 to 1000.</span></span>
-   <span data-ttu-id="e4110-115">Höhere Rang Werte geben Dokumente an, die den Suchbedingungen besser entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e4110-115">Higher rank values indicate documents that better match the search conditions.</span></span>
-   <span data-ttu-id="e4110-116">Rang Werte gelten nur für die aktuelle Abfrage und können daher nicht für Abfragen über Abfragen hinweg verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="e4110-116">Rank values apply only to the current query, so they cannot be compared for results across queries.</span></span>
-   <span data-ttu-id="e4110-117">Rang Werte sind relativ zu den anderen Dokumenten, die mit der Abfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e4110-117">Rank values are relative to the other documents matching the query.</span></span> <span data-ttu-id="e4110-118">Der Rangwert eines bestimmten Dokuments hängt daher von den anderen Dokumenten ab, die ebenfalls der Abfrage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e4110-118">Therefore, the rank value of a particular document depends on the other documents that also match the query.</span></span>
-   <span data-ttu-id="e4110-119">Rang Werte für Elemente, die mit einem rein relationalen Prädikat übereinstimmen, sind 1000.</span><span class="sxs-lookup"><span data-stu-id="e4110-119">Rank values for items matching a purely relational predicate are 1000.</span></span>

<span data-ttu-id="e4110-120">Sie können die zurückgegebenen Rang Werte mithilfe von Spalten Gewichtungen in den WHERE-Klausel-Prädikaten " [enthält](-search-sql-contains.md) " und " [fretext](-search-sql-freetext.md) " und der Rang-nach-Klausel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e4110-120">You can manipulate the returned rank values by using column weights in the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) WHERE clause predicates, and the RANK BY clause.</span></span>

 

 



