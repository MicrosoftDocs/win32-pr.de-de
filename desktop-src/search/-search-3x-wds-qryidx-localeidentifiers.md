---
description: Grundlegendes zu den Argumenten inputlocale und keywordlocale in Windows Search, wodurch die Suchmaschine die richtigen Wörteraufschlüsseler verwenden kann.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Gebietsschemabezeichnerargumente (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403753"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="a845b-103">Gebietsschemabezeichnerargumente (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="a845b-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="a845b-104">Die `inputlocale` `keywordlocale` Bezeichner und unterstützen die Suchmaschine dabei, die richtigen Wörteraufschlüsseler zu verwenden, indem sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der Schlüsselwörter der erweiterten Abfragesyntax identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a845b-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="a845b-105">Dabei handelt es sich nicht immer um die gleichen Sprachcodebezeichner (Language Code Identifiers, LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch PACKS für weitere Sprachen enthält.</span><span class="sxs-lookup"><span data-stu-id="a845b-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="a845b-106">Inputlocale identifiziert die LCID für die Sprache, in der Benutzer ihre Suchabfrage eingeben, während keywordlocale die LCID identifiziert, die die Suchmaschine für Schlüsselwörter verwendet.</span><span class="sxs-lookup"><span data-stu-id="a845b-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="a845b-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="a845b-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a845b-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a845b-108">Example</span></span>](#example)
-   [<span data-ttu-id="a845b-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a845b-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="a845b-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a845b-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="a845b-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a845b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a845b-112">Erste Schritte mit Parameter-Value Argumenten</span><span class="sxs-lookup"><span data-stu-id="a845b-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="a845b-113">ARGUMENTS-Argument</span><span class="sxs-lookup"><span data-stu-id="a845b-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="a845b-114">SYNTAX-Argument</span><span class="sxs-lookup"><span data-stu-id="a845b-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="a845b-115">STACKEDBY-Argument</span><span class="sxs-lookup"><span data-stu-id="a845b-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="a845b-116">SUBQUERY-Argument</span><span class="sxs-lookup"><span data-stu-id="a845b-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



