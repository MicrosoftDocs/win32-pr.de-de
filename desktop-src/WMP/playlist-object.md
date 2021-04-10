---
title: Wiedergabelisten Objekt
description: Das Wiedergabelisten Objekt bietet eine Möglichkeit, Medienelemente in einer Liste zu organisieren, um eine einfache Bearbeitung mithilfe der folgenden Eigenschaften und Methoden zu ermöglichen.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Wiedergabelisten Objekt-Fenster Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037762"
---
# <a name="playlist-object"></a><span data-ttu-id="d90ae-104">Wiedergabelisten Objekt</span><span class="sxs-lookup"><span data-stu-id="d90ae-104">Playlist Object</span></span>

<span data-ttu-id="d90ae-105">Das **Wiedergabe** Listen Objekt bietet eine Möglichkeit, Medienelemente in einer Liste zu organisieren, um eine einfache Bearbeitung mithilfe der folgenden Eigenschaften und Methoden zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d90ae-105">The **Playlist** object provides a way to organize media items in a list for easy manipulation by using the following properties and methods.</span></span>

<span data-ttu-id="d90ae-106">Das **Wiedergabe** Listen Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d90ae-106">The **Playlist** object supports the following properties.</span></span>



| <span data-ttu-id="d90ae-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d90ae-107">Property</span></span>                                      | <span data-ttu-id="d90ae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d90ae-108">Description</span></span>                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="d90ae-109">AttributeCount</span><span class="sxs-lookup"><span data-stu-id="d90ae-109">attributeCount</span></span>](playlist-attributecount.md) | <span data-ttu-id="d90ae-110">Ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d90ae-110">Retrieves the number of attributes associated with the playlist.</span></span> |
| [<span data-ttu-id="d90ae-111">AttributeName</span><span class="sxs-lookup"><span data-stu-id="d90ae-111">attributeName</span></span>](playlist-attributename.md)   | <span data-ttu-id="d90ae-112">Ruft den Namen eines durch einen Index angegebenen Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="d90ae-112">Retrieves the name of an attribute specified by an index.</span></span>        |
| [<span data-ttu-id="d90ae-113">count</span><span class="sxs-lookup"><span data-stu-id="d90ae-113">count</span></span>](playlist-count.md)                   | <span data-ttu-id="d90ae-114">Ruft die Anzahl der Elemente in der Wiedergabeliste ab.</span><span class="sxs-lookup"><span data-stu-id="d90ae-114">Retrieves the number of items in the playlist.</span></span>                   |
| [<span data-ttu-id="d90ae-115">name</span><span class="sxs-lookup"><span data-stu-id="d90ae-115">name</span></span>](playlist-name.md)                     | <span data-ttu-id="d90ae-116">Gibt den Namen der Wiedergabeliste an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="d90ae-116">Specifies or retrieves the name of the playlist.</span></span>                 |



 

<span data-ttu-id="d90ae-117">Das **Wiedergabe** Listen Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="d90ae-117">The **Playlist** object supports the following methods.</span></span>



| <span data-ttu-id="d90ae-118">Methode</span><span class="sxs-lookup"><span data-stu-id="d90ae-118">Method</span></span>                                  | <span data-ttu-id="d90ae-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d90ae-119">Description</span></span>                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d90ae-120">appendItem</span><span class="sxs-lookup"><span data-stu-id="d90ae-120">appendItem</span></span>](playlist-appenditem.md)   | <span data-ttu-id="d90ae-121">Fügt ein Medien Element am Ende der Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="d90ae-121">Adds a media item to the end of the playlist.</span></span>                                                          |
| <span data-ttu-id="d90ae-122">**Löschen**</span><span class="sxs-lookup"><span data-stu-id="d90ae-122">**clear**</span></span>                               | <span data-ttu-id="d90ae-123">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d90ae-123">Reserved for future use.</span></span>                                                                               |
| [<span data-ttu-id="d90ae-124">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="d90ae-124">getItemInfo</span></span>](playlist-getiteminfo.md) | <span data-ttu-id="d90ae-125">Ruft den Wert eines Wiedergabelisten Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="d90ae-125">Retrieves the value of a playlist attribute.</span></span>                                                           |
| [<span data-ttu-id="d90ae-126">insertItem</span><span class="sxs-lookup"><span data-stu-id="d90ae-126">insertItem</span></span>](playlist-insertitem.md)   | <span data-ttu-id="d90ae-127">Fügt ein Medien Element an der angegebenen Position in die Wiedergabeliste ein.</span><span class="sxs-lookup"><span data-stu-id="d90ae-127">Inserts a media item into the playlist at the specified location.</span></span>                                      |
| [<span data-ttu-id="d90ae-128">isidentical</span><span class="sxs-lookup"><span data-stu-id="d90ae-128">isIdentical</span></span>](playlist-isidentical.md) | <span data-ttu-id="d90ae-129">Ruft einen Wert ab, der angibt, ob das angegebene **Wiedergabe** Listen Objekt mit dem aktuellen-Objekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="d90ae-129">Retrieves a value indicating whether the supplied **Playlist** object is identical to the current one.</span></span> |
| [<span data-ttu-id="d90ae-130">item</span><span class="sxs-lookup"><span data-stu-id="d90ae-130">item</span></span>](playlist-item.md)               | <span data-ttu-id="d90ae-131">Ruft das Medien Element am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="d90ae-131">Retrieves the media item at the specified index.</span></span>                                                       |
| [<span data-ttu-id="d90ae-132">"muveitem"</span><span class="sxs-lookup"><span data-stu-id="d90ae-132">moveItem</span></span>](playlist-moveitem.md)       | <span data-ttu-id="d90ae-133">Ändert die Position eines Elements in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="d90ae-133">Changes the location of an item in the playlist.</span></span>                                                       |
| [<span data-ttu-id="d90ae-134">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="d90ae-134">removeItem</span></span>](playlist-removeitem.md)   | <span data-ttu-id="d90ae-135">Entfernt das angegebene Element aus der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="d90ae-135">Removes the specified item from the playlist.</span></span>                                                          |
| [<span data-ttu-id="d90ae-136">"Einstellungs Element"</span><span class="sxs-lookup"><span data-stu-id="d90ae-136">setItemInfo</span></span>](playlist-setiteminfo.md) | <span data-ttu-id="d90ae-137">Gibt den Wert eines Wiedergabelisten Attributs an.</span><span class="sxs-lookup"><span data-stu-id="d90ae-137">Specifies the value of a playlist attribute.</span></span>                                                           |



 

<span data-ttu-id="d90ae-138">Der Zugriff auf das **Wiedergabe** Listen Objekt erfolgt über die folgenden Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="d90ae-138">The **Playlist** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="d90ae-139">Object</span><span class="sxs-lookup"><span data-stu-id="d90ae-139">Object</span></span>                                              | <span data-ttu-id="d90ae-140">Eigenschaft oder Methode</span><span class="sxs-lookup"><span data-stu-id="d90ae-140">Property or method</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d90ae-141">Rom</span><span class="sxs-lookup"><span data-stu-id="d90ae-141">Cdrom</span></span>](cdrom-object.md)                           | [<span data-ttu-id="d90ae-142">Abspielen</span><span class="sxs-lookup"><span data-stu-id="d90ae-142">playlist</span></span>](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d90ae-143">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="d90ae-143">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="d90ae-144">[GetAll](mediacollection-getall.md), [getbyalbum](mediacollection-getbyalbum.md), [getbyattribute](mediacollection-getbyattribute.md), [getbyauthor](mediacollection-getbyauthor.md), [getbygenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span><span class="sxs-lookup"><span data-stu-id="d90ae-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span></span> |
| [<span data-ttu-id="d90ae-145">Player</span><span class="sxs-lookup"><span data-stu-id="d90ae-145">Player</span></span>](player-object.md)                         | <span data-ttu-id="d90ae-146">[currentwiedergabe](player-currentplaylist.md), [newwiedergabe](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="d90ae-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="d90ae-147">Playlistarray</span><span class="sxs-lookup"><span data-stu-id="d90ae-147">PlaylistArray</span></span>](playlistarray-object.md)           | [<span data-ttu-id="d90ae-148">item</span><span class="sxs-lookup"><span data-stu-id="d90ae-148">item</span></span>](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d90ae-149">Playlistcollection</span><span class="sxs-lookup"><span data-stu-id="d90ae-149">PlaylistCollection</span></span>](playlistcollection-object.md) | [<span data-ttu-id="d90ae-150">neue</span><span class="sxs-lookup"><span data-stu-id="d90ae-150">newPlaylist</span></span>](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

<span data-ttu-id="d90ae-151">Da es sich um die gängigste Zugriffsmethode handelt, ist der *Player*. **currentwiedergabe** wird zur Veranschaulichung in den Abschnitten der Referenz Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="d90ae-151">Because it is the most common means of access, *player*.**currentPlaylist** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="d90ae-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d90ae-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90ae-153">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="d90ae-153">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




