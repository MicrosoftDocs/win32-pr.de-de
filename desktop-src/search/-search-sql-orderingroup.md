---
description: Die Order in Group-Klausel wird in Verbindung mit der Group on-Anweisung verwendet, die Resultsets in Gruppen zurückgibt.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: Order in Group-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342949"
---
# <a name="order-in-group-clause"></a><span data-ttu-id="e9e6c-103">Order in Group-Klausel</span><span class="sxs-lookup"><span data-stu-id="e9e6c-103">ORDER IN GROUP Clause</span></span>

<span data-ttu-id="e9e6c-104">Die Order in Group-Klausel wird in Verbindung mit der [Group on](-search-sql-group-on-over.md) -Anweisung verwendet, die Resultsets in Gruppen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-104">The ORDER IN GROUP clause is used in conjunction with the [GROUP ON](-search-sql-group-on-over.md) statement, which returns result sets in groups.</span></span> <span data-ttu-id="e9e6c-105">Mit der Order in Group-Klausel können Sie jede zurückgegebene Gruppe auf andere Weise sortieren.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-105">The ORDER IN GROUP clause enables you to sort each returned group in a different way.</span></span> <span data-ttu-id="e9e6c-106">Wenn Sie z. b. nach System. Kind gruppieren, können Sie alle Dokumente nach System.Doc-Nummer sortieren. Lastauthor, alle Musikdateien nach System. Music. albumartist und alle e-Mails nach System. Message. FromName.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-106">If you group on System.Kind, for example, you can then sort all documents by System.Document.LastAuthor, all music files by System.Music.AlbumArtist, and all emails by System.Message.FromName.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e6c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9e6c-107">Syntax</span></span>

<span data-ttu-id="e9e6c-108">Im folgenden finden Sie die Syntax der Order in Group-Klausel:</span><span class="sxs-lookup"><span data-stu-id="e9e6c-108">The following is the syntax of the ORDER IN GROUP clause:</span></span>


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



<span data-ttu-id="e9e6c-109">Der gruppennamensspezifizierer ist ein Bereich oder ein bekannter Wert aus der Gruppenspalte, wie in der Group on-Anweisung angegeben.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-109">The group name specifier is a range or known value from the group column, as specified in the GROUP ON statement.</span></span> <span data-ttu-id="e9e6c-110">Zu den bekannten Werten für System. Photo. Isospeed zählen z. b. "ISO-100", "ISO-200" usw.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-110">For example, known values for System.Photo.ISOSpeed would include 'ISO-100', 'ISO-200', and so on.</span></span> <span data-ttu-id="e9e6c-111">Ein Bereich für System. Photo. DateTaken würde "2006-1-1" und "2007-1-1" für eine Anweisung wie "Group" in System. itemdate \[ "2006-1-1", "2007-1-1" enthalten \] .</span><span class="sxs-lookup"><span data-stu-id="e9e6c-111">A range for System.Photo.DateTaken would include '2006-1-1' and '2007-1-1' for a statement like GROUP ON System.ItemDate \['2006-1-1', '2007-1-1'\].</span></span>

<span data-ttu-id="e9e6c-112">Der Spalten Spezifizierer muss eine gültige Spalte sein, die entweder in der Gruppe on oder der SELECT-Anweisung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-112">The column specifier must be a valid column specified in either the GROUP ON or the SELECT statement.</span></span> <span data-ttu-id="e9e6c-113">Sie können mehr als eine Spalte einschließen, getrennt durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-113">You can include more than one column, separated by commas.</span></span> <span data-ttu-id="e9e6c-114">Wenn Sie z. b. System. Photo. Isospeed gruppieren, können Sie alle ISO-100-Fotos zuerst nach "System. Photo. shutterspeed" und dann nach "System. Photo. Aperture" sortieren.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-114">For example, if you group on System.Photo.ISOSpeed, you can sort all ISO-100 photos, first by System.Photo.ShutterSpeed, and then by System.Photo.Aperture.</span></span>

<span data-ttu-id="e9e6c-115">Der optionale richtungsspezifizierer kann entweder ASC für aufsteigend (niedrig zu hoch) oder für absteigend (hoch bis niedrig) sein.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-115">The optional direction specifier can be either ASC for ascending (low to high) or DESC for descending (high to low).</span></span> <span data-ttu-id="e9e6c-116">Wenn Sie keinen richtungsspezifizierer angeben, wird der Standardwert aufsteigend verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-116">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="e9e6c-117">Wenn Sie mehr als eine Spalte angeben, aber nicht alle Richtungen angeben, wird die von Ihnen angegebene Richtung zuletzt auf jede aufeinander folgende Spalte angewendet, bis Sie die Richtung explizit ändern.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-117">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each successive column until you explicitly change the direction.</span></span>

<span data-ttu-id="e9e6c-118">Bereiche oder Werte, die nicht explizit in einer Order Group in-Klausel angegeben sind, werden in aufsteigender Reihenfolge nach den Werten in der Spalte Gruppieren nach sortiert.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-118">Ranges or values that are not explicitly specified in an ORDER GROUP IN clause are sorted in ascending order by the values in the GROUP ON column.</span></span>

## <a name="examples"></a><span data-ttu-id="e9e6c-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9e6c-119">Examples</span></span>

<span data-ttu-id="e9e6c-120">Im folgenden Beispiel werden die Ergebnisse nach der System. Kind-Eigenschaft gruppiert.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-120">The following example groups results by the System.Kind property.</span></span> <span data-ttu-id="e9e6c-121">Die Abfrage würde die Gruppe "Program" nach dem Namen der Anwendung und der Gruppe "Music" nach Albumtitel und Nachverfolgen der Nummer sortieren.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-121">The query would order the 'program' group by the application name and the 'music' group by album title and track number.</span></span> <span data-ttu-id="e9e6c-122">Die **null** -Gruppe wird nach dem Elementnamen geordnet.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-122">The **NULL** group would be ordered by the item name.</span></span> <span data-ttu-id="e9e6c-123">Alle anderen Gruppen würden nach dem Element Datum geordnet.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-123">All other groups would by ordered by the item date.</span></span>


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



<span data-ttu-id="e9e6c-124">Im folgenden Beispiel werden die Ergebnisse nach der System. itemdate-Eigenschaft gruppiert. Anschließend werden die einzelnen Gruppen nach Element-URL, Art oder Name sortiert.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-124">The following example groups results by the System.ItemDate property, and then sorts each group by item URL, kind, or name.</span></span>


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



<span data-ttu-id="e9e6c-125">Die Ergebnisse der vorhergehenden Abfrage werden in fünf Gruppen zurückgegeben und entsprechend der Beschreibung in der folgenden Tabelle sortiert.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-125">The results of the preceding query would be returned in five groups and sorted as described in the following table.</span></span>



| <span data-ttu-id="e9e6c-126">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="e9e6c-126">Group</span></span>    | <span data-ttu-id="e9e6c-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9e6c-127">Description</span></span>                                               | <span data-ttu-id="e9e6c-128">Sortiert nach:</span><span class="sxs-lookup"><span data-stu-id="e9e6c-128">Sorted by</span></span>                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="e9e6c-129">MinValue</span><span class="sxs-lookup"><span data-stu-id="e9e6c-129">MINVALUE</span></span> | <span data-ttu-id="e9e6c-130">Elemente mit Datumsangaben vor 2006-1-1</span><span class="sxs-lookup"><span data-stu-id="e9e6c-130">Items with dates before 2006-1-1</span></span>                          | <span data-ttu-id="e9e6c-131">Sortiert nach der Element-URL in aufsteigender Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e9e6c-131">Sorted by the item's URL, in ascending order</span></span> |
| <span data-ttu-id="e9e6c-132">2006-1-1</span><span class="sxs-lookup"><span data-stu-id="e9e6c-132">2006-1-1</span></span> | <span data-ttu-id="e9e6c-133">Elemente mit Datumsangaben auf oder nach 2006-1-1, aber vor 2007-1-1</span><span class="sxs-lookup"><span data-stu-id="e9e6c-133">Items with dates on or after 2006-1-1 but before 2007-1-1</span></span> | <span data-ttu-id="e9e6c-134">Sortiert nach Element Datum in aufsteigender Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e9e6c-134">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="e9e6c-135">2007-1-1</span><span class="sxs-lookup"><span data-stu-id="e9e6c-135">2007-1-1</span></span> | <span data-ttu-id="e9e6c-136">Elemente mit Datumsangaben auf oder nach 2007-1-1, aber vor 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="e9e6c-136">Items with dates on or after 2007-1-1 but before 2008-1-1</span></span> | <span data-ttu-id="e9e6c-137">Sortiert nach Kind-Wert in aufsteigender Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e9e6c-137">Sorted by kind value, in ascending order</span></span>     |
| <span data-ttu-id="e9e6c-138">2008-1-1</span><span class="sxs-lookup"><span data-stu-id="e9e6c-138">2008-1-1</span></span> | <span data-ttu-id="e9e6c-139">Elemente mit Datumsangaben auf oder nach 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="e9e6c-139">Items with dates on or after 2008-1-1</span></span>                     | <span data-ttu-id="e9e6c-140">Sortiert nach Element Datum in aufsteigender Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e9e6c-140">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="e9e6c-141">**NULL**</span><span class="sxs-lookup"><span data-stu-id="e9e6c-141">**NULL**</span></span> | <span data-ttu-id="e9e6c-142">Elemente ohne Wert in der System. itemdate-Spalte</span><span class="sxs-lookup"><span data-stu-id="e9e6c-142">Items with no value in the System.ItemDate column</span></span>         | <span data-ttu-id="e9e6c-143">Sortiert nach Elementname in aufsteigender Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="e9e6c-143">Sorted by item name, in ascending order</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="e9e6c-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9e6c-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e9e6c-145">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="e9e6c-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9e6c-146">Gruppieren nach... Über... An</span><span class="sxs-lookup"><span data-stu-id="e9e6c-146">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
</dt> <dt>

[<span data-ttu-id="e9e6c-147">Order By-Klausel</span><span class="sxs-lookup"><span data-stu-id="e9e6c-147">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> </dl>

 

 



