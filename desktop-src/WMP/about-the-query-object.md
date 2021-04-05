---
title: Informationen zum Query-Objekt
description: Informationen zum Query-Objekt
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player, Abfrageobjekt
- Windows Media Player-Objektmodell, Abfrageobjekt
- Objektmodell, Abfrageobjekt
- Windows Media Player ActiveX-Steuerelement, Abfrageobjekt
- ActiveX-Steuerelement, Abfrageobjekt
- Windows Media Player Mobile ActiveX-Steuerelement, Abfrageobjekt
- Windows Media Player Mobile, Abfrageobjekt
- Query-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710793"
---
# <a name="about-the-query-object"></a><span data-ttu-id="dec03-111">Informationen zum Query-Objekt</span><span class="sxs-lookup"><span data-stu-id="dec03-111">About the Query Object</span></span>

<span data-ttu-id="dec03-112">Das **Query** -Objekt stellt eine Verbund Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="dec03-112">The **Query** object represents a compound query.</span></span> <span data-ttu-id="dec03-113">Sie erstellen ein neues, leeres **Abfrage** Objekt durch Aufrufen von *mediacollection*. " **kreatequery**".</span><span class="sxs-lookup"><span data-stu-id="dec03-113">You create a new, empty **Query** object by calling *mediaCollection*.**createQuery**.</span></span> <span data-ttu-id="dec03-114">Nachdem Sie ein **Abfrage** Objekt erstellt haben, können Sie **addcondition** aufzurufen, um der Verbund Abfrage eine Bedingung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dec03-114">After you have created a **Query** object, you can call **addCondition** to add a condition to the compound query.</span></span> <span data-ttu-id="dec03-115">Jeder nachfolgende Rückruf von **addcondition** fügt eine neue Bedingung mithilfe der-und der-Logik an die vorhandene Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="dec03-115">Each subsequent call to **addCondition** appends a new condition to the existing query using AND logic.</span></span>

<span data-ttu-id="dec03-116">Nehmen Sie beispielsweise an, Sie möchten eine Abfrage erstellen, die alle digitalen Medien repräsentiert, bei denen **WM/Genre** den Wert "Jazz" hat und der **Autor** "Jim" enthält.</span><span class="sxs-lookup"><span data-stu-id="dec03-116">For example, suppose you want to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim".</span></span> <span data-ttu-id="dec03-117">Sie können eine Verbund Abfrage erstellen, die diese Bedingungen mithilfe des folgenden JScript-Codes darstellt:</span><span class="sxs-lookup"><span data-stu-id="dec03-117">You could create a compound query to represent these conditions by using the following JScript code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



<span data-ttu-id="dec03-118">Zum Hinzufügen einer Bedingung zu einer Verbund Abfrage mit der-oder-Logik müssen Sie **Query. beginnextgroup** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dec03-118">To add a condition to a compound query using OR logic, you must call **Query.beginNextGroup**.</span></span> <span data-ttu-id="dec03-119">Diese Methode signalisiert, dass die vorherige Bedingungs Gruppe abgeschlossen ist und dass der nächste **addcondition** -Rückruf den Anfang einer neuen Bedingungs Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="dec03-119">This method signals that the previous condition group is completed and that the next call to **addCondition** represents the start of a new condition group.</span></span>

<span data-ttu-id="dec03-120">Beispielsweise können Sie den folgenden Beispielcode verwenden, um eine Abfrage zu erstellen, die alle digitalen Medien repräsentiert, bei denen **WM/Genre** den Wert "Jazz" hat, und der **Autor** "Jim" oder der **Autor** "Dave" enthält:</span><span class="sxs-lookup"><span data-stu-id="dec03-120">For example, to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim" or **Author** contains "Dave", you could use the following example code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



<span data-ttu-id="dec03-121">Um die Verbund Abfrage auszuführen, nennen Sie **mediacollection. getplaylistbyquery**.</span><span class="sxs-lookup"><span data-stu-id="dec03-121">To execute your compound query, call **MediaCollection.getPlaylistByQuery**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dec03-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dec03-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec03-123">**Mediacollection. getplaylistbyquery**</span><span class="sxs-lookup"><span data-stu-id="dec03-123">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="dec03-124">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="dec03-124">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="dec03-125">**Query-Objekt**</span><span class="sxs-lookup"><span data-stu-id="dec03-125">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 




