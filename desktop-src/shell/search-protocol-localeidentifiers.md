---
description: Die InputLocale-und keywordlocale-IDs helfen dem Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem Sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifizieren.
title: Gebiets Schema-bezeichnerargumente (die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218061"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="74096-103">Gebiets Schema-bezeichnerargumente (die Windows-Shell)</span><span class="sxs-lookup"><span data-stu-id="74096-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="74096-104">Die `inputlocale` `keywordlocale` Bezeichner und unterstützen das Suchmodul dabei, die richtigen Wörter Trennungen zu verwenden, indem die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der von erweiterten Abfrage Syntax Schlüsselwörter identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="74096-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="74096-105">Dabei handelt es sich nicht immer um die gleichen Sprachcode Bezeichner (LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch mehrsprachige Benutzeroberflächen Pakete (MUI) für weitere Sprachen enthalten.</span><span class="sxs-lookup"><span data-stu-id="74096-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="74096-106">Der `inputlocale` identifiziert die LCID für die Sprache, die Benutzer in die Suchabfrage eingeben, während der die `keywordlocale` LCID identifiziert, die die Such-Engine für Schlüsselwörter verwendet.</span><span class="sxs-lookup"><span data-stu-id="74096-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="74096-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="74096-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="74096-108">Argument Informationen</span><span class="sxs-lookup"><span data-stu-id="74096-108">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="74096-109">Mindestens Betriebs System</span><span class="sxs-lookup"><span data-stu-id="74096-109">Minimum Operating System</span></span> | <span data-ttu-id="74096-110">Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="74096-110">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



