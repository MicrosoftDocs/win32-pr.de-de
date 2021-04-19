---
description: Uniwriter bietet APIs, um Typografiefunktionen zu unterstützen und die Anzeige und Bearbeitung von internationalem Text zu unterstützen, einschließlich der komplexen Regeln von Nahen und ostasiatischen Skripts.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Verwenden von uniscri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369099"
---
# <a name="using-uniscribe"></a><span data-ttu-id="cf41b-103">Verwenden von uniscri</span><span class="sxs-lookup"><span data-stu-id="cf41b-103">Using Uniscribe</span></span>

<span data-ttu-id="cf41b-104">Uniwriter bietet APIs, um Typografiefunktionen zu unterstützen und die Anzeige und Bearbeitung von internationalem Text zu unterstützen, einschließlich der komplexen Regeln von Nahen und ostasiatischen Skripts.</span><span class="sxs-lookup"><span data-stu-id="cf41b-104">Uniscribe provides APIs to support typography and to support the display and editing of international text, including the complex rules of Middle Eastern and Asian scripts.</span></span> <span data-ttu-id="cf41b-105">Uniwriter stellt Routinen auf niedriger Ebene für die Verarbeitung von vollständig formatiertem Text und einen einfachen scriptstring-API-Satz für unformatierten Text bereit.</span><span class="sxs-lookup"><span data-stu-id="cf41b-105">Uniscribe provides low-level routines for handling fully formatted text, and a simple ScriptString API set for unformatted text.</span></span>

<span data-ttu-id="cf41b-106">Bei Verwendung von unischreiber müssen Anwendungen nur einen Sicherungs Speicher von Unicode-Zeichen Codes verwalten.</span><span class="sxs-lookup"><span data-stu-id="cf41b-106">Using Uniscribe, applications only have to manage a backing store of Unicode character codes.</span></span> <span data-ttu-id="cf41b-107">Textlayoutanwendungen müssen keine andere Puffer-oder Mapping-Tabelle verwalten, um die Reihenfolge der Zeichen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="cf41b-107">Text layout applications do not have to maintain any other buffer or mapping table to track character order.</span></span> <span data-ttu-id="cf41b-108">Jede Anwendung muss nur die Reihenfolge speichern und verwalten, in der die Zeichen vom Benutzer eingegeben werden. Dies ist dieselbe logische Reihenfolge wie durch Unicode definiert.</span><span class="sxs-lookup"><span data-stu-id="cf41b-108">Each application only has to store and manage the order in which the characters are entered by the user, which is the same logical order as defined by Unicode.</span></span> <span data-ttu-id="cf41b-109">Der Sicherungs Speicher ändert sich nie aufgrund von Layoutvorgängen.</span><span class="sxs-lookup"><span data-stu-id="cf41b-109">The backing store never changes as a result of layout operations.</span></span> <span data-ttu-id="cf41b-110">Uniscribehält einen Index von den neu bestellten Clustern an den ursprünglichen Zeichen Grenzen bei, die von der Anwendung weitergegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="cf41b-110">Uniscribe maintains an index from the reordered clusters to the original character boundaries passed by the application.</span></span>

<span data-ttu-id="cf41b-111">Die folgenden Themen werden in diesem Abschnitt behandelt.</span><span class="sxs-lookup"><span data-stu-id="cf41b-111">The following topics are covered in this section.</span></span>

<span data-ttu-id="cf41b-112">**Strukturierung**</span><span class="sxs-lookup"><span data-stu-id="cf41b-112">**Shaping**</span></span>

-   [<span data-ttu-id="cf41b-113">Bestimmen, ob ein Skript eine Symbol Strukturierung erfordert</span><span class="sxs-lookup"><span data-stu-id="cf41b-113">Determining If a Script Requires Glyph Shaping</span></span>](determining-if-a-script-requires-glyph-shaping.md)
-   [<span data-ttu-id="cf41b-114">Verwenden von Strukturierungs Modulen</span><span class="sxs-lookup"><span data-stu-id="cf41b-114">Using Shaping Engines</span></span>](using-shaping-engines.md)

<span data-ttu-id="cf41b-115">**Andere Verarbeitung**</span><span class="sxs-lookup"><span data-stu-id="cf41b-115">**Other Processing**</span></span>

-   [<span data-ttu-id="cf41b-116">Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="cf41b-116">Caching</span></span>](caching.md)
-   [<span data-ttu-id="cf41b-117">Anzeigen von Text mit uniwriter</span><span class="sxs-lookup"><span data-stu-id="cf41b-117">Displaying Text with Uniscribe</span></span>](displaying-text-with-uniscribe.md)
-   [<span data-ttu-id="cf41b-118">Verarbeiten komplexer Skripts</span><span class="sxs-lookup"><span data-stu-id="cf41b-118">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
-   [<span data-ttu-id="cf41b-119">Verwenden eines Schriftart-Fallbacks</span><span class="sxs-lookup"><span data-stu-id="cf41b-119">Using Font Fallback</span></span>](using-font-fallback.md)
-   [<span data-ttu-id="cf41b-120">Verwenden der scriptstring-Funktionen</span><span class="sxs-lookup"><span data-stu-id="cf41b-120">Using the ScriptString Functions</span></span>](using-the-scriptstring-functions.md)

<span data-ttu-id="cf41b-121">**Einfügemarke**</span><span class="sxs-lookup"><span data-stu-id="cf41b-121">**Caret**</span></span>

-   [<span data-ttu-id="cf41b-122">Anzeigen des Caretzeichen in bidirektionalen Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="cf41b-122">Displaying the Caret in Bidirectional Strings</span></span>](displaying-the-caret-in-bidirectional-strings.md)
-   [<span data-ttu-id="cf41b-123">Verwalten der Platzierung von Caretzeichen und Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="cf41b-123">Managing Caret Placement and Hit Testing</span></span>](managing-caret-placement-and-hit-testing.md)
-   [<span data-ttu-id="cf41b-124">Übersetzen des X-Offsets in der Einfügemarke</span><span class="sxs-lookup"><span data-stu-id="cf41b-124">Translating Mouse Hit X Offset to Caret Position</span></span>](translating-mouse-hit-x-offset-to-caret-position.md)

<span data-ttu-id="cf41b-125">**Wörter und Zeichen Cluster**</span><span class="sxs-lookup"><span data-stu-id="cf41b-125">**Words and Character Clusters**</span></span>

-   [<span data-ttu-id="cf41b-126">Verwenden von Zeichen Clustern</span><span class="sxs-lookup"><span data-stu-id="cf41b-126">Using Character Clusters</span></span>](using-character-clusters.md)
-   [<span data-ttu-id="cf41b-127">Verwenden von Wort Break Points</span><span class="sxs-lookup"><span data-stu-id="cf41b-127">Using Word Break Points</span></span>](using-word-break-points.md)
-   [<span data-ttu-id="cf41b-128">Arbeiten mit Beziehungen zwischen Einfügepositionen, Ausrichtungspunkten und Clustern</span><span class="sxs-lookup"><span data-stu-id="cf41b-128">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



