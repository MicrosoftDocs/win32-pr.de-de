---
title: Funktionsweise der tupelindizierung
description: Tupelindizes werden verwendet, um Suchvorgänge zu optimieren, die 0 oder mehr mediensuchzeichenfolgen und 0 oder 1 Final-Search-Zeichen folgen haben. Sie können auch verwendet werden, um Suchvorgänge nach einer anfänglichen Such Zeichenfolge zu optimieren, wenn für dieses Attribut kein normaler Index verfügbar ist.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- tupelindizierung
- Suchen Active Directory Active Directory, Optimierung
- Active Directory, Such Optimierungs Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724488"
---
# <a name="how-tuple-indexing-works"></a><span data-ttu-id="b0063-107">Funktionsweise der tupelindizierung</span><span class="sxs-lookup"><span data-stu-id="b0063-107">How Tuple Indexing Works</span></span>

<span data-ttu-id="b0063-108">Tupelindizes werden verwendet, um Suchvorgänge zu optimieren, die 0 oder mehr [mediensuchzeichenfolgen](search-string-types.md) und 0 oder 1 Final-Search-Zeichen folgen haben.</span><span class="sxs-lookup"><span data-stu-id="b0063-108">Tuple indices are used to optimize searches that have 0 or more [medial-search strings](search-string-types.md) and 0 or 1 final-search strings.</span></span> <span data-ttu-id="b0063-109">Sie können auch verwendet werden, um Suchvorgänge nach einer anfänglichen Such Zeichenfolge zu optimieren, wenn für dieses Attribut kein normaler Index verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b0063-109">They can also be used to optimize searches for an initial search string if no ordinary index is available over that attribute.</span></span>

<span data-ttu-id="b0063-110">Sie können die tupelindizierung für ein Attribut aktivieren, indem Sie im [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Attribut Bit 5 festlegen, das dem Wert 32 entspricht.</span><span class="sxs-lookup"><span data-stu-id="b0063-110">You can turn on tuple indexing for an attribute by setting bit 5, which corresponds to the value 32, in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span> <span data-ttu-id="b0063-111">Dieses Attribut wird im Schema Objekt festgelegt, das das Attribut darstellt, das den Tupelindex benötigt.</span><span class="sxs-lookup"><span data-stu-id="b0063-111">This attribute is set in the schema object that represents the attribute that needs the tuple index.</span></span> <span data-ttu-id="b0063-112">Die Leistungseinbußen beim Aktivieren der tupelindizierung besteht darin, dass jeder für dieses Attribut festgelegte Zeichen folgen Wert in eine große Anzahl von Fragmenten im Tupelindex erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="b0063-112">The performance impact of turning on tuple indexing is that any string value that is set for that attribute will be expanded into a large number of fragments in the tuple index.</span></span> <span data-ttu-id="b0063-113">Wenn ein Attribut erweitert wird, verbraucht es eine größere Menge an Speicherplatz in der Verzeichnis Informationsstruktur und wird auch langsamer aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b0063-113">When an attribute expands, it consumes a larger amount of disk space in the Directory Information Tree file, and also gets updated more slowly.</span></span>

<span data-ttu-id="b0063-114">Tupelindizes sind so konzipiert, dass die Suchvorgänge im Formular beschleunigt werden `*string*` .</span><span class="sxs-lookup"><span data-stu-id="b0063-114">Tuple indices are designed to accelerate searches of the form `*string*`.</span></span> <span data-ttu-id="b0063-115">Die Beschleunigung kann beträchtlich sein, da diese Art von Suche nicht auf andere Weise optimiert werden kann. in der nicht optimierten Form erzwingt Sie, dass der Active Directory Server jedes Objekt im Bereich der Suche durchläuft, um die Abfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b0063-115">The acceleration can be considerable because this form of search cannot be optimized in any other way, and in its un-optimized form, it forces the Active Directory server to walk every object in the scope of the search to perform the query.</span></span> <span data-ttu-id="b0063-116">Daher würde eine Basis Suche nur ein Objekt durchsuchen. Wenn Sie weniger Ressourcen benötigen, werden bei einer untergeordneten Suche nur die untergeordneten Elemente eines Objekts durchsucht (was je nach Containergröße weniger Ressourcen oder mehr Ressourcen verbrauchen kann), und eine Unterstruktur Suche durchläuft die gesamte Teilstruktur unter dem Basisobjekt, was normalerweise viele Ressourcen benötigt und aufgrund der Größe der Unterstruktur sehr langsam ist.</span><span class="sxs-lookup"><span data-stu-id="b0063-116">Thus, a base search would just search one object, which would use fewer resources, an immediate children search would search just the children of an object (which could use fewer resources or more resources depending on the container size), and a subtree search will walk the entire subtree under the base object, which would usually require a lot of resources and be very slow because of the subtree size.</span></span>

<span data-ttu-id="b0063-117">Tupelindizes funktionieren durch das Aufteilen einer Zeichenfolge in *Tupel*.</span><span class="sxs-lookup"><span data-stu-id="b0063-117">Tuple indices work by breaking a string into *tuples*.</span></span> <span data-ttu-id="b0063-118">Beispielsweise würde die Zeichenfolge "Active Directory" in die folgenden Tupel unterteilt:</span><span class="sxs-lookup"><span data-stu-id="b0063-118">For example, the string "Active Directory" would be broken into the following tuples:</span></span>

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> <span data-ttu-id="b0063-119">Wenn eine Zeichenfolge für die tupelindizierung erweitert wird, wird das Verzeichnis bei 32767 Zeichen angehalten.</span><span class="sxs-lookup"><span data-stu-id="b0063-119">The directory will stop at 32767 characters when expanding a string for tuple indexing.</span></span>

 

<span data-ttu-id="b0063-120">Ein Tupelindex würde einen Eintrag für jedes dieser Tupel enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0063-120">A tuple index would contain an entry for each one of these tuples.</span></span> <span data-ttu-id="b0063-121">Wenn ein Benutzer beispielsweise nach sucht `*cto*` , sucht der Active Directory Server nach allen Übereinstimmungen für "CTO" im Index und sucht in diesem Fall einen Zeiger zurück auf den Datensatz, der ein (tupelindiziertes)-Attribut mit dem Wert "Directory" enthielt.</span><span class="sxs-lookup"><span data-stu-id="b0063-121">So, if a user searches for `*cto*`, then the Active Directory server will look up all the matches for "cto" in the index and, in this case, find a pointer back to the record that had a (tuple indexed) attribute with a value of "Directory".</span></span>

<span data-ttu-id="b0063-122">Wenn die mediale Such Zeichenfolge ( `*cto*` im vorherigen Beispiel) spezifisch genug ist, ist die Suche Recht effizient, da Sie die Anzahl der Objekte, die der Active Directory Server überprüfen muss, um die Abfrage auszuführen, erheblich reduziert.</span><span class="sxs-lookup"><span data-stu-id="b0063-122">If the medial search string (`*cto*` in the previous example) is specific enough, then the search will be quite efficient because it greatly reduces the number of objects that the Active Directory server must inspect to perform the query.</span></span>

 

 