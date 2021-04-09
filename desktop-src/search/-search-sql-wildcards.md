---
description: Das enthält-Prädikat unterstützt die Verwendung des Sternchen ( \* ) als Platzhalter Zeichen zum Darstellen von Wörtern und Ausdrücken. Das Sternchen kann nur am Ende des Worts oder Ausdrucks hinzugefügt werden. Wenn das Sternchen vorhanden ist, wird der Modus für die Präfix Übereinstimmung aktiviert.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Verwenden von Platzhalter Zeichen im enthält-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128525"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a><span data-ttu-id="a7cc0-105">Verwenden von Platzhalter Zeichen im enthält-Prädikat</span><span class="sxs-lookup"><span data-stu-id="a7cc0-105">Using Wildcard Characters in the CONTAINS Predicate</span></span>

<span data-ttu-id="a7cc0-106">Das enthält-Prädikat unterstützt die Verwendung des Sternchen ( \* ) als Platzhalter Zeichen zum Darstellen von Wörtern und Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-106">The CONTAINS predicate supports the use of the asterisk (\*) as a wildcard character to represent words and phrases.</span></span> <span data-ttu-id="a7cc0-107">Das Sternchen kann nur am Ende des Worts oder Ausdrucks hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-107">You can add the asterisk only at the end of the word or phrase.</span></span> <span data-ttu-id="a7cc0-108">Wenn das Sternchen vorhanden ist, wird der Modus für die Präfix Übereinstimmung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-108">The presence of the asterisk enables the prefix-matching mode.</span></span> <span data-ttu-id="a7cc0-109">In diesem Modus werden Übereinstimmungen zurückgegeben, wenn in der Spalte das angegebene Suchwort gefolgt von NULL oder mehr anderen Zeichen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-109">In this mode, matches are returned if the column contains the specified search word followed by zero or more other characters.</span></span> <span data-ttu-id="a7cc0-110">Wenn ein Ausdruck bereitgestellt wird, werden Übereinstimmungen erkannt, wenn die Spalte alle angegebenen Wörter mit 0 (null) oder mehr anderen Zeichen nach dem letzten Wort enthält.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-110">If a phrase is provided, matches are detected if the column contains all the specified words with zero or more other characters following the final word.</span></span>

## <a name="examples"></a><span data-ttu-id="a7cc0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7cc0-111">Examples</span></span>

<span data-ttu-id="a7cc0-112">Im ersten Beispiel werden Dokumente mit einem beliebigen Wort in der Dateiname-Spalte, beginnend mit "Serv", abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-112">The first example matches documents that have any word in the FileName column beginning with "serv".</span></span> <span data-ttu-id="a7cc0-113">Beispiele für übereinstimmende Wörter sind "Server", "Server" und "Service".</span><span class="sxs-lookup"><span data-stu-id="a7cc0-113">Example matching words include "server", "servers", and "service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



<span data-ttu-id="a7cc0-114">Im zweiten Beispiel werden Dokumente mit einem beliebigen Ausdruck in der Dateiname-Spalte abgeglichen, der mit "Comp" beginnt und in dem das nächste Wort mit "Serv" beginnt.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-114">The second example matches documents with any phrase in the FileName column that begins with "comp" and in which the next word begins with "serv".</span></span> <span data-ttu-id="a7cc0-115">Beispiele für übereinstimmende Wörter sind "Comp Server", "Comp Servers" und "Comp Service".</span><span class="sxs-lookup"><span data-stu-id="a7cc0-115">Example matching words include "comp server", "comp servers", and "comp service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



<span data-ttu-id="a7cc0-116">Das Sternchen funktioniert nur für Präfix Vergleiche und kann nur am Ende des Worts oder Ausdrucks eingefügt werden. Es funktioniert nicht für Suffixvergleiche.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-116">The asterisk works only for prefix-matching and can be placed only at the end of the word or phrase; it does not work for suffix-matching.</span></span> <span data-ttu-id="a7cc0-117">Die folgende Syntax ist ungültig und entspricht nicht den Dokumenten mit einem Wort in der Dateiname-Spalte, die mit "Service" enden.</span><span class="sxs-lookup"><span data-stu-id="a7cc0-117">The following syntax is not valid and does not match documents with any word in the FileName column ending with "serve".</span></span>


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a><span data-ttu-id="a7cc0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7cc0-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a7cc0-119">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="a7cc0-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7cc0-120">Frei Text Prädikat</span><span class="sxs-lookup"><span data-stu-id="a7cc0-120">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="a7cc0-121">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="a7cc0-121">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



