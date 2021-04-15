---
description: Sie können die Sprache angeben, die in Such Abfragen verwendet wird.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Angeben von Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525478"
---
# <a name="specifying-languages"></a><span data-ttu-id="c4013-103">Angeben von Sprachen</span><span class="sxs-lookup"><span data-stu-id="c4013-103">Specifying Languages</span></span>

<span data-ttu-id="c4013-104">Sie können die Sprache angeben, die in Such Abfragen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4013-104">You can specify the language used in search queries.</span></span> <span data-ttu-id="c4013-105">Sowohl der frei Text als auch der enthält Prädikate in der WHERE-Klausel unterstützen die Angabe einer Sprache.</span><span class="sxs-lookup"><span data-stu-id="c4013-105">Both the FREETEXT and CONTAINS predicates in the WHERE clause support specifying a language.</span></span> <span data-ttu-id="c4013-106">Sie können die Abfragesprache angeben, indem Sie einen numerischen Sprachcode Bezeichner (LCID) im enthält-oder frei Text Prädikat bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c4013-106">You can indicate the query language by providing a numeric language code identifier (LCID) in the CONTAINS or FREETEXT predicate.</span></span> <span data-ttu-id="c4013-107">Diese LCID gibt an, welche Wörter Trennung zum Analysieren der Abfrage Zeichenfolge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4013-107">This LCID specifies which word breaker to use to parse the query string.</span></span> <span data-ttu-id="c4013-108">Es verwendet die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="c4013-108">It uses the following syntax:</span></span>


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



<span data-ttu-id="c4013-109">Weitere Informationen finden Sie in der Syntax für die Prädikate " [enthält](-search-sql-contains.md) " und "frei [Text](-search-sql-freetext.md) ".</span><span class="sxs-lookup"><span data-stu-id="c4013-109">For more information, see the syntax for the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates.</span></span>

 

 



