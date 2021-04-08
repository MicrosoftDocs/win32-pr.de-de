---
description: Die InputLocale-und keywordlocale-IDs helfen dem Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem Sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifizieren.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Gebiets Schema-bezeichnerargumente (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862180"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="e1778-103">Gebiets Schema-bezeichnerargumente (Windows-Suche)</span><span class="sxs-lookup"><span data-stu-id="e1778-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="e1778-104">Die `inputlocale` `keywordlocale` Bezeichner und unterstützen das Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e1778-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="e1778-105">Dabei handelt es sich nicht immer um die gleichen Sprachcode Bezeichner (LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch MUI-Pakete für weitere Sprachen umfasst.</span><span class="sxs-lookup"><span data-stu-id="e1778-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="e1778-106">InputLocale identifiziert die LCID für die Sprache, die Benutzer in Ihre Suchabfrage eingeben, während keywordlocale die LCID identifiziert, die die Suchmaschine für Schlüsselwörter verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1778-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="e1778-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="e1778-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e1778-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e1778-108">Example</span></span>](#example)
-   [<span data-ttu-id="e1778-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1778-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="e1778-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e1778-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="e1778-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1778-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1778-112">Die ersten Schritte mit Parameter-Value Argumenten</span><span class="sxs-lookup"><span data-stu-id="e1778-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="e1778-113">Crumb-Argument</span><span class="sxs-lookup"><span data-stu-id="e1778-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="e1778-114">Syntax Argument</span><span class="sxs-lookup"><span data-stu-id="e1778-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="e1778-115">Stackedby-Argument</span><span class="sxs-lookup"><span data-stu-id="e1778-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="e1778-116">Unterabfrage Argument</span><span class="sxs-lookup"><span data-stu-id="e1778-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



