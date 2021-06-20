---
description: Machen Sie sich mit den Argumenten inputlocale und keywordlocale auf der Windows Shell-Benutzeroberfläche aus, die der Suchmaschine helfen, die richtigen Wörterschalter zu verwenden.
title: Locale Identifier Arguments (The Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 34eab39e7ed956bf68048d9ce5861c12eedbbe7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403593"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="7646b-103">Locale Identifier Arguments (The Windows Shell)</span><span class="sxs-lookup"><span data-stu-id="7646b-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="7646b-104">Die Bezeichner und unterstützen die Suchmaschine dabei, die richtigen Wörterschalter zu verwenden, indem sie die Sprache der vom Benutzer eingegebenen Abfragen und die Sprache der `inputlocale` `keywordlocale` Schlüsselwörter für erweiterte Abfragesyntax identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7646b-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="7646b-105">Dabei handelt es sich nicht immer um dieselben Sprachcodebezeichner (Language Code Identifiers, LCIDs), da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch mehrsprachige Benutzeroberfläche-Pakete (COD) für weitere Sprachen enthält.</span><span class="sxs-lookup"><span data-stu-id="7646b-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="7646b-106">Identifiziert die LCID für die Sprache, in die Benutzer ihre Suchabfrage eingeben, während die LCID identifiziert, die die `inputlocale` `keywordlocale` Suchmaschine für Schlüsselwörter verwendet.</span><span class="sxs-lookup"><span data-stu-id="7646b-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="7646b-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7646b-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="7646b-108">Argumentinformationen</span><span class="sxs-lookup"><span data-stu-id="7646b-108">Argument Information</span></span>



|                              | <span data-ttu-id="7646b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="7646b-109">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="7646b-110">**Mindestbetriebssystem**</span><span class="sxs-lookup"><span data-stu-id="7646b-110">**Minimum Operating System**</span></span> | <span data-ttu-id="7646b-111">Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="7646b-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



